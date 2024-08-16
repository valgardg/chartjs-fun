<template>
    <Bar :data="data" :options="options" />
</template>

<script lang="ts">
import {
    Chart as ChartJS,
    Title,
    Tooltip,
    Legend,
    BarElement,
    CategoryScale,
    LinearScale
} from 'chart.js'
import { Bar } from 'vue-chartjs'

ChartJS.register(CategoryScale, LinearScale, BarElement, Title, Tooltip, Legend)

const data = [
    { month: 'January', count: 1560 },
    { month: 'February', count: 3270 },
    { month: 'March', count: 1890 },
    { month: 'April', count: 1302 },
    { month: 'May', count: 1580 },
  ];

export default {
    name: 'App',
    components: {
    Bar
    },
    data() {
        return {
            data: {
                labels: data.map(row => row.month),
                datasets: [
                    {
                        label: 'Spending per month',
                        data: data.map(row => row.count)
                    }
                ]
                },
            options: {
                responsive: true
            }
        }
    }
}
</script>