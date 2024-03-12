<script>
import OffersItem from '../components/OffersItem.vue'
import PeopleCarousel from '../components/PeopleCarousel.vue'
import PartnersItem from '../components/PartnersItem.vue'
import PizzaCarousel from '../components/PizzaCarousel.vue'
import EventsList from '../components/EventsList.vue'
import BookItem from '../components/BookItem.vue'

export default {
    name: 'AppMain',

    components: {
        OffersItem,
        PeopleCarousel,
        PartnersItem,
        PizzaCarousel,
        EventsList,
        BookItem,
    }

}
</script>

<template>
    <OffersItem></OffersItem>
    <PeopleCarousel></PeopleCarousel>
    <PartnersItem></PartnersItem>
    <PizzaCarousel></PizzaCarousel>
    <EventsList></EventsList>
    <BookItem></BookItem>
</template>

<style lang="scss"></style>./EventsList.vue