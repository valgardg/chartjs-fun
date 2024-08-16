<template>
    <div class="container d-flex flex-column justify-content-start align-items-center main-content mt-5">
        <p class="fs-1">ChartJS fun</p>
        <!-- <BarComponent /> -->
         <div class="doughnut-container">
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
             <SpendingDoughnut />
         </div>
    </div>
</template>

<script setup lang="ts">
import BarComponent from '@/components/BarComponent.vue';
import SpendingDoughnut from '@/components/SpendingDoughnut.vue';
</script>

<style scoped>
.doughnut-container {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    width: 100%;
    height: 60rem;
}
</style>