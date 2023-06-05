<script>
import HeadComponent from './components/HeadComponent.vue'
import MainComp from './components/MainComp.vue'

export default {
  components: {
    HeadComponent,
    MainComp
  }
}
</script>

<template>
  <HeadComponent />

  <MainComp />
</template>

<style lang="scss">
@use './styles/general.scss'
</style>
