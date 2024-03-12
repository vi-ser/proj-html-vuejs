<script>
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import PizzeData from './assets/pizzas.json';
import EventData from './assets/events.json';

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
      events: EventData.events,
    }
  },

  methods: {
  },

  created() {
    this.store.pizza = PizzeData.pizzas;
    this.store.event = EventData.events;
  },
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>

</template>

<style lang="scss"></style>
