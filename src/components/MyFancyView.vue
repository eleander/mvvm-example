<template>
  <div>
    <input v-model="data" />
    <p>{{ data }}</p>
  </div>
</template>

<script setup lang="js">
import {computed} from "vue"
// This defines the prop: "text"
const props = defineProps(["text"])
// This defines the custom event "update:text"
const emit = defineEmits(["update:text"])

// VueUse Style
// const data = useVModel(props, 'data', emit)

// GENERIC VUE STYLE
// This creates a computed property that is bound to the prop "text"
// If "text" changes via v-model, it fires a custom event to the ViewModel
// To change the state of "text"
const data = computed({
  // getter: gets the prop
  get() {
    return props.text
  },
  // setter: fires a custom event to change the prop
  set(newValue) {
    emit("update:text", newValue)
  }
})
</script>

<style></style>
