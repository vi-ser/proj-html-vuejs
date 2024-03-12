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
    },
};
</script>

<template>
    <div id="carousel-section" class="text-center">
        <span class="text-uppercase oswald-medium">choose your flavor</span>
        <h2 class="text-uppercase oswald-medium">
            the best pizza menu in town
        </h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ut blandit arcu in<br>pretium molesstie. Interdum et
            malesuada fames ac.</p>
    </div>
    <ul id="pizza-carousel" class="d-flex overflow-hidden ">
        <div class="pizza-slider list-unstyled d-flex justify-content-center text-center">
            <PizzaItem v-for="(currentPizza, index) in store.pizza" :key="index" :pizza="currentPizza"></PizzaItem>
        </div>
        <div class="pizza-slider list-unstyled d-flex justify-content-center text-center">
            <PizzaItem v-for="(currentPizza, index) in store.pizza" :key="index" :pizza="currentPizza"></PizzaItem>
        </div>
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


    .pizza-slider {
        padding-bottom: 160px;
        animation: carousel-slide 20s infinite linear;
    }

    @keyframes carousel-slide {
        from {
            transform: translateX(0);
        }

        to {
            transform: translateX(-100%);
        }
    }
}
</style>