<template>
  <div :style="styleObject">
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Totam rerum placeat at praesentium
    magni eos libero, hic maxime, natus nam odit officia error aliquid nulla quasi illo quo nisi
    minima.
    <button v-on:click="fontSize--">-</button>
    <button v-on:click="fontSize++">+</button>
  </div>
</template>

<script>
import { computed, reactive, ref } from 'vue'

export default {
  setup() {
    // const styleObject = reactive({
    //   color: 'red',
    //   fontSize: '13px',
    // })
    const fontSize = ref(14)

    const styleObject = computed(() => {
      return {
        color: 'red',
        fontSize: fontSize.value + 'px',
      }
    })
    return {
      styleObject,
      fontSize,
    }
  },
}
</script>

<style lang="scss" scoped></style>
