<template>
  <div>
    <p>{{ msg }}</p>
    <p v-text="msg"></p>
    <p v-text="htmlStr"></p>
    <p v-html="htmlStr"></p>
    <p v-pre>{{ msg 안녕하세요.}}</p>
    <p v-once>{{ msg }} !!!</p>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const msg = ref('안녕하세요.')
    const htmlStr = ref('<h2>안녕!</h2>')
    return {
      msg,
      htmlStr,
    }
  },
}
</script>

<style lang="scss" scoped></style>
