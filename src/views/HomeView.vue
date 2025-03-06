<script setup lang="ts">
import {ref} from 'vue'

const lineChartSeries = ref([
  {
    name:'Sales',
    data:[30,40,35,60,76,10,45]
  }
])

const lineChartOptions = ref({
  xaxis:{
    categories:['a','b','c','d','e','f','g']
  }
})

</script>

<template>
  <main>
    <div class="flex flex-col gap-16 p-24 items-center bg-gray-700">
      <h2>text </h2>
    <div class="w-1/3 bg-white rounded-xl p-4 " >
    <h2 class="text-x1 font-semibold"> Teste de graficos</h2>
    <apexCharts 
      type="line"
      :series="lineChartSeries"
      :options="lineChartOptions"
       />

    </div>
  </div>
  </main>
</template>

<style>
</style>
