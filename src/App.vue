<script>
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import LinksData from './assets/links.json';
import PizzeData from './assets/pizzas.json';
import EventData from './assets/events.json';
import RestaurantData from './assets/restaurants.json';
import HourData from './assets/hours.json';


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
      links: LinksData.links,
      restaurants: RestaurantData.restaurants,
      hours: HourData.hours,
    }
  },

  methods: {
  },

  created() {
    this.store.pizza = PizzeData.pizzas;
    this.store.event = EventData.events;
    this.store.link = LinksData.links;
    this.store.restaurant = RestaurantData.restaurants;
    this.store.hour = HourData.hours;
  },
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
</template>

<style lang="scss"></style>
