<template>
  <div>
    <TheNav></TheNav>
    <TheView></TheView>
  </div>
</template>

<script>
//import AppCard from './components/AppCard.vue'
import TheNav from './components/TheNav.vue'
import TheView from './components/TheView.vue'
export default {
  components: {
    TheNav,
    TheView,
    //AppCard,
  },
  setup() {
    return {}
  },
}
</script>

<style lang="scss" scoped></style>
