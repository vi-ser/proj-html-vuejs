<script>
import { store } from '../store';
import TeamCard from '../components/TeamCard.vue';

export default {
    name: 'PeopleCarousel',

    data() {
        return {
            store,
        }
    },

    components: {
        TeamCard,
    }

}
</script>

<template>
    <ul id="carousel" class="d-flex list-unstyled">
        <TeamCard v-for="currentMember in store.team" :team="currentMember"></TeamCard>
    </ul>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#carousel {
    margin-bottom: $smallMargin;
}
</style>