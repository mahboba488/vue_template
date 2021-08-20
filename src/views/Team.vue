<template>
  <v-container>
    
    <v-row>
      <v-col cols="12" md="8">
        <h1 class="headline mb-2 grey--text">The Income Growth</h1>
        <template>
          <div id="app">
            <GChart
              type="BubbleChart"
              :data="chartData"
              :options="chartOptions"
              style="width: 700px; height: 300px"
            />
          </div>
        </template>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { GChart } from "vue-google-charts";

const gradients = [
  ["#222"],
  ["#42b3f4"],
  ["red", "orange", "yellow"],
  ["purple", "vlolet"],
  ["#00c6ff", "F0F", "#FF0"],
  ["#f72047", "ffd200", "1feaea"],
]
export default {
  
  data() {
    return {
      Picker: new Date.toISOString().substr(0, 10),
      chartData: [
        ["ID", "X", "Y", "In Million"],
        ["", 80, 167, 120],
        ["", 79, 136, 130],
        ["", 78, 184, 50],
        ["", 72, 278, 230],
        ["", 81, 200, 210],
        ["", 72, 170, 100],
        ["", 68, 477, 80],
      ],
      chartOptions: {
        colorAxis: { colors: ["yellow", "red"] },
      },
      showLabels: false,
      lineWidth: 2,
      labelSize: 7,
      redius: 10,
      padding: 8,
      lineCap: "round",
      gradient: gradients[5],
      value: [2, 2, 5, 9, 5, 10, 3, 5, -4, -10, 1, 8, 2, 9, 0],
      gradientDirection: "top",
      gradients,
      fill: false,
      type: "trend",
      autoLineWidth: false,
    };
  },
  components: {
    
    GChart
  },
};
</script>

<style  scoped>
.v-progress-circular {
  margin: 1rem;
}
</style>>

