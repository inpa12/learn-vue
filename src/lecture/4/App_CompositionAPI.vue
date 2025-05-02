<template>
  <div>
    <h2>반응형 메시지</h2>
    <p>{{ reactiveMessage }}</p>
    <button v-on:click="addReactiveMessage">Add Message</button>
    <h2>일반 메시지</h2>
    <p>{{ normalMessage }}</p>
  </div>
</template>

<script>
import { onBeforeMount, onMounted, ref } from 'vue'
export default {
  setup() {
    console.log('setup()')
    const reactiveMessage = ref('Hello Reactive Message!')
    const addReactiveMessage = () => {
      reactiveMessage.value = reactiveMessage.value + '!'
    }
    const normalMessage = 'Hello Normal Message!'

    onMounted(() => {
      console.log('onMounted')
    })
    onBeforeMount(() => {
      console.log('onBeforeMounted')
    })

    return {
      reactiveMessage,
      addReactiveMessage,
      normalMessage,
    }
  },
}
</script>

<style lang="scss" scoped></style>
