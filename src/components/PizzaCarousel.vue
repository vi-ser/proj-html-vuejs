<script>
import { store } from '../store';
import PizzaItem from '../components/PizzaItem.vue'

export default {
    name: 'PizzaCarousel',

    components: {
        PizzaItem,
    },

    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <div id="carousel-section" class="text-center">
        <span class="text-uppercase oswald-medium">choose your flavor</span>
        <h2 class="text-uppercase oswald-medium">
            the best pizza menu in town
        </h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut blandit arcu in<br>pretium molesstie. Interdum
            et
            malesuada fames ac.</p>
    </div>
    <ul id="pizza-carousel" class="list-unstyled d-flex justify-content-center overflow-hidden text-center">
        <PizzaItem v-for="currentPizza in store.pizza" :pizza="currentPizza"></PizzaItem>
    </ul>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#carousel-section {
    padding: 105px 160px 0;

    span {
        color: $primary;
    }

    h2 {
        margin-top: 10px;
        margin-bottom: 30px;

    }

    p {
        color: $textLight;
        margin-bottom: 115px;
    }
}

#pizza-carousel {
    gap: 65px;
    padding-bottom: 160px;
}
</style>