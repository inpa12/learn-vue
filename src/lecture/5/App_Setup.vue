<template>
  <div>
    <p>{{ counter }}</p>
    <button @click="increment">Click!</button>
    <p>{{ message }}</p>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  setup() {
    const counter = ref(0)
    const message = ref('Hello Vue3')
    const increment = () => {
      counter.value++
    }
    return {
      counter,
      message,
      increment,
    }
  },
}
</script>

<style lang="scss" scoped></style>
