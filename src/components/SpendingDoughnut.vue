<template>
    <div class="d-flex flex-column justify-content-center align-items-center">
        <p>January</p>
        <Doughnut :data="data" :options="options" />
    </div>
</template>

<script lang="ts">
import { Chart as ChartJS, ArcElement, Tooltip, Legend } from 'chart.js'
import { Doughnut } from 'vue-chartjs'
import * as chartConfig from '../chartConfigs/spendingCategories'

ChartJS.register(ArcElement, Tooltip, Legend)

export default {
    name: 'App',
    components: {
        Doughnut
    },
    data() {
        return chartConfig
    }
}
</script>