<script>
import OffersItem from '../components/OffersItem.vue'
import PeopleCarousel from '../components/PeopleCarousel.vue'
import PartnersItem from '../components/PartnersItem.vue'
import PizzaCarousel from '../components/PizzaCarousel.vue'

export default {
    name: 'AppMain',

    components: {
        OffersItem,
        PeopleCarousel,
        PartnersItem,
        PizzaCarousel,
    }

}
</script>

<template>
    <OffersItem></OffersItem>
    <PeopleCarousel></PeopleCarousel>
    <PartnersItem></PartnersItem>
    <PizzaCarousel></PizzaCarousel>
</template>

<style lang="scss"></style>