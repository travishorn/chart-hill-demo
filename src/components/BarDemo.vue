<script setup>
import { ref, computed } from "vue";

const inputData = ref([
  { id: 0, label: "Option A", value:  45 },
  { id: 1, label: "Option B", value: 136 },
  { id: 2, label: "Option C", value: 233 },
]);

/*
 * For some reason, I have to turn the inputData object into an array of objects
 * (instead of an array of proxies. Basically "unreffing" the array) before
 * passing it to the component as a prop.
 * 
 * It would be much nicer to just pass the array in its reffed form.
 * Maybe look into the "reactive" Vue function?
 */
const data = computed(() => {
  return inputData.value.map((point) => {
    return {
      ...point,
    };
  });
});
</script>

<template>
  <div style="display: flex; flex-direction: column; gap: 30px;">
    <h1 style="text-align: center; margin-bottom: 0;">Bar</h1>

    <div style="background-color: white; border-radius: 10px; padding: 20px;">
      <ch-bar :data="data" />
    </div>

    <div style="display: flex; justify-content: space-between; gap: 10px;">
      <div style="width: 100%; display: flex; flex-direction: column;">
        <table>
          <thead>
            <tr>
              <th
                style="font-weight: normal; text-align: left; font-size: 12px;"
              >
                Label
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
                <input type="text" v-model="point.label" />
              </td>
              <td>
                <input type="number" v-model="point.value" />
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>
