<script setup lang="ts">
import {ref} from 'vue'

const lineChartSeries = ref([
  {
    name:'vendas',
    data:[30,40,35,60,76,10,45]
  }
])

const lineChartOptions = ref({
  xaxis:{
    categories:['a','b','c','d','e','f','g']
  }
})

const barChartSeries = ref([
  {
    name:'lucro',
    data:[30,40,35,60,76,10,45]
  }
])

const barChartOptions = ref({
  xaxis:{
    categories:['a','b','c','d','e','f','g']
  }
})

const pieChartSeries = ref([
30,40,35,60,76,10,45
])

const pieChartOptions = ref({
    labels:['a','b','c','d','e','f','g']
})

</script>

<template>
  <main>
    <div class="flex flex-col gap-16 p-24 items-center bg-gray-700">
      <h2>text </h2>
    <div class="w-1/3 bg-white rounded-xl p-4 " >
    <h2 class="text-x1 font-semibold"> Grafico Linha</h2>
    <apexCharts 
      type="line"
      :series="lineChartSeries"
      :options="lineChartOptions"
       />

    </div>

    <div class="w-1/3 bg-white rounded-xl p-4 " >
    <h2 class="text-x1 font-semibold"> Grafico Barra</h2>
    <apexCharts 
      type="bar"
      :series="barChartSeries"
      :options="barChartOptions"
       />

    </div>

    <div class="w-1/3 bg-white rounded-xl p-4 " >
    <h2 class="text-x1 font-semibold"> Grafico Pizza</h2>
    <apexCharts 
      type="pie"
      :series="pieChartSeries"
      :options="pieChartOptions"
       />

    </div>

    <div class="w-1/3 bg-white rounded-xl p-4 " >
    <h2 class="text-x1 font-semibold"> Grafico Area</h2>
    <apexCharts 
      type="area"
      :series="barChartSeries"
      :options="barChartOptions"
       />

    </div>
  </div>
  </main>
</template>

<style>
</style>
