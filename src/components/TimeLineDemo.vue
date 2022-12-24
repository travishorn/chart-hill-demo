<script setup>
import { ref, computed } from "vue";

const inputData = ref([
  { id: 0, date: "2019-01-01", value:  45 },
  { id: 1, date: "2020-01-01", value: 136 },
  { id: 2, date: "2021-01-01", value: 233 },
  { id: 3, date: "2022-01-01", value: 400 },
  { id: 4, date: "2023-01-01", value: 635 },
]);

const data = computed(() => {
  return inputData.value.map((point) => {
    return {
      ...point,
      date: new Date(point.date),
    };
  });
});

const lineColor = ref("#1f77b4");
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 30px;">
    <h1 style="text-align: center; margin-bottom: 0;">Time Line</h1>

    <div style="background-color: white; border-radius: 10px; padding: 20px;">
      <ch-time-line :data="data" :lineColor="lineColor" />
    </div>

    <div style="display: flex; justify-content: space-between; gap: 10px;">
      <div style="width: 100%; display: flex; flex-direction: column;">
        <table>
          <thead>
            <tr>
              <th
                style="font-weight: normal; text-align: left; font-size: 12px;"
              >
                Date
              </th>
              <th
                style="font-weight: normal; text-align: left; font-size: 12px;"
              >
                Value
              </th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="point in inputData" :key="point.id">
              <td>
                <input type="date" v-model="point.date" />
              </td>
              <td>
                <input type="number" v-model="point.value" />
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div style="display: flex; flex-direction: column;">
        <label for="lineColor" style="font-size: 12px;">Line color</label>
        <input id="lineColor" type="color" v-model="lineColor" />
      </div>
    </div>
  </div>
</template>
