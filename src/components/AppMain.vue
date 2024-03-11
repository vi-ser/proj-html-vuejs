<script>
import OffersItem from '../components/OffersItem.vue'
import PeopleCarousel from '../components/PeopleCarousel.vue'
import PartnersItem from '../components/PartnersItem.vue'

export default {
    name: 'AppMain',

    components: {
        OffersItem,
        PeopleCarousel,
        PartnersItem,
    }

}
</script>

<template>
    <OffersItem></OffersItem>
    <PeopleCarousel></PeopleCarousel>
    <PartnersItem></PartnersItem>
</template>

<style lang="scss"></style>