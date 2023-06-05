<script>
import { store } from './store';
import axios from 'axios';
import HeadComponent from './components/HeadComponent.vue';
import MainComp from './components/MainComp.vue';

export default {
  components: {
    HeadComponent,
    MainComp
  },
  data() {
    return {
      store,
    }
  },
  methods: {
    getPlaingCards() {
      axios.get(store.apiURL)
        .then(res => {
          store.playCardList = res.data.data;
          console.log(store.playCardList);
        })
        .catch(err => {
          console.log(err);
        })
    }
  },
  created() {
    this.getPlaingCards();
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
