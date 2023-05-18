<script setup>
import OrderBook from './components/OrderBook.vue'
import CenterChart from './components/CenterChart.vue'
import TopBar from "./components/TopBar.vue";
</script>

<template>
  <div class="dark:bg-slate-800 dark:text-white">

    <div class="grid grid-cols-12">
      <!-- bars -->
      <div class="col-span-12 grid grid-cols-12">
        <div class="col-span-9">
            <TopBar/>
        </div>
        <div class="col-span-3">search</div>
      </div>

      <!-- left area  -->
      <div class="col-span-3 ">
      <OrderBook/>
      </div>

      <!-- center area  -->
      <div class="col-span-6">
          <CenterChart/>
      </div>

      <!-- right-area  -->
      <div class="col-span-3">right</div>
    </div>
  </div>
  <!-- <HelloWorld msg="Vite + Vue" /> -->
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
