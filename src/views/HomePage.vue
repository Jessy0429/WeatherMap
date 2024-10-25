<template>
  <div class="home">
    <!--    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />-->
    <ToolBar @update="updateSelectedDate" />
    <Map @update="updateSelectedPoint" />
    <WeatherInfoCard
      :date="selectedDate || undefined"
      :pointData="selectedPoint || undefined"
    ></WeatherInfoCard>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import Map from "@/components/Map.vue";
import ToolBar from "@/components/ToolBar.vue";
import WeatherInfoCard from "@/components/WeatherInfoCard.vue";

interface PointProps {
  lat: number;
  lng: number;
}

const selectedDate = ref<string>();
const selectedPoint = ref<PointProps>();

const updateSelectedDate = (val: string) => {
  selectedDate.value = val;
};
const updateSelectedPoint = (val: PointProps) => {
  selectedPoint.value = val;
};
</script>
