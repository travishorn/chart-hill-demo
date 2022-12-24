<script setup>
import GaugeDemo from "./components/GaugeDemo.vue";
import TimeLineDemo from "./components/TimeLineDemo.vue";
</script>

<template>
  <div style="font-family: sans-serif; max-width: 600px; margin: 0 auto; padding: 20px; display: flex; flex-direction: column; gap: 80px;">
    <GaugeDemo />
    <TimeLineDemo />
  </div>
</template>

<style>
body {
  background-color: #F0F0F0;
}
</style>