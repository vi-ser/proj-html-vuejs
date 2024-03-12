<script>
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import PizzeData from './assets/pizzas.json';

export default {

  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },

  data() {
    return {
      store,
      pizzas: PizzeData.pizzas,
    }
  },

  methods: {
  },

  created() {
    this.store.pizza = PizzeData.pizzas;
  },
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>

</template>

<style lang="scss"></style>
