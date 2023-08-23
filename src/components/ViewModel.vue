<template>
  <div>
    <MyFancyView v-model:text="text" />
    The Presenters Text is: {{ text }}
  </div>
</template>

<script setup>
import { ref } from "vue";
import MyFancyView from "./MyFancyView.vue";

const text = ref("");

// The equivalent React code is:
// <MyFancyView text={text} setText={newText=> setText(newText)} />
// const [text, setText] = useState("");
</script>
