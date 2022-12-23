<script setup>
import { ref } from "vue";
const min = ref(20);
const max = ref(40);
const value = ref(35);
const barColor = ref("#106cde");
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 30px;">
    <h1 style="text-align: center; margin-bottom: 0;">Gauge</h1>

    <div style="background-color: white; border-radius: 10px; padding: 20px;">
      <ch-gauge :min="min" :max="max" :value="value" :barColor="barColor" />
    </div>

    <div style="display: flex; justify-content: space-between; gap: 10px;">
      <div style="display: flex; flex-direction: column;">
        <label for="min" style="font-size: 12px;">Minimum</label>
        <input style="width: 100%;" id="min" type="number" v-model="min" />
      </div>

      <div style="display: flex; flex-direction: column;">
        <label for="value" style="font-size: 12px;">Value</label>
        <input style="width: 100%;" id="value" type="number" v-model="value" />
      </div>

      <div style="display: flex; flex-direction: column;">
        <label for="max" style="font-size: 12px;">Maximum</label>
        <input style="width: 100%;" id="max" type="number" v-model="max" />
      </div>

      <div style="display: flex; flex-direction: column;">
        <label for="barColor" style="font-size: 12px;">Bar color</label>
        <input style="width: 100%;" id="barColor" type="color" v-model="barColor" />
      </div>
    </div>
  </div>
</template>
