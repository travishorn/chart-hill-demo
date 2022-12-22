<script setup>
import { ref } from "vue";
const min = ref(20);
const max = ref(40);
const value = ref(35);
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 30px;">
    <h1 style="text-align: center; margin-bottom: 0;">Gauge</h1>

    <div style="background-color: white; border-radius: 10px; padding: 20px;">
      <ch-gauge :min="min" :max="max" :value="value" barColor="mediumseagreen" />
    </div>

    <div style="display: flex; justify-content: space-between;">
      <div style="display: flex; flex-direction: column;">
        <label for="min" style="font-size: 12px;">Minimum</label>
        <input id="min" type="number" v-model="min" />
      </div>

      <div style="display: flex; flex-direction: column;">
        <label for="value" style="font-size: 12px;">Value</label>
        <input id="value" type="number" v-model="value" />
      </div>

      <div style="display: flex; flex-direction: column;">
        <label for="max" style="font-size: 12px;">Maximum</label>
        <input id="max" type="number" v-model="max" />
      </div>
    </div>
  </div>
</template>
