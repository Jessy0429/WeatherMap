<script setup lang="ts">
import { defineProps, watch } from "vue";

interface WeatherInfoProps {
  pointData:
    | {
        lat: number;
        lng: number;
      }
    | undefined;
  date: string | undefined;
}
const props = defineProps<WeatherInfoProps>();
</script>

<template>
  <div>HelloWorld</div>
</template>

<style scoped lang="scss"></style>
