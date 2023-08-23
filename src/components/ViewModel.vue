<template>
  <div>
    <MyFancyView v-model:text="text" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import MyFancyView from "./MyFancyView.vue";

const text = ref("");
</script>
