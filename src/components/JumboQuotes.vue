<script>
import { store } from '../store';
import QuoteItem from '../components/QuoteItem.vue'

export default {
    name: 'JumboQuotes',

    data() {
        return {
            store,
            activeIndex: 0,
            autoplayTimer: null,
        }
    },

    components: {
        QuoteItem,
    },

    methods: {
        changeQuote(index) {
            this.activeIndex = index;
        },

        prevQuote() {
            this.activeIndex--;
            if (this.activeIndex < 0) {
                this.activeIndex = this.store.quote.length - 1;
            }
        },

        nextQuote() {
            this.activeIndex++;
            if (this.activeIndex > this.store.quote.length - 1) {
                this.activeIndex = 0;
            }
        },

        startAutoplay() {
            this.autoplayTimer = setInterval(this.nextQuote, 5000);
        },
    },

    mounted() {
        this.changeQuote(0);

        this.startAutoplay();
    }

}
</script>

<template>
    <div id="jumbo-quotes" class="d-flex flex-column text-center">
        <img class="quote" src="/svg/quotes.svg" alt="Quotes background">
        <QuoteItem v-for="(currentQuote, index) in store.quote" :key="index" :quote="currentQuote"
            v-show="index === activeIndex" />
        <div class="control">
            <i v-for="(currentQuote, index) in store.quote" :key="index" @click="changeQuote(index)"
                :class="{ 'fa-solid fa-circle': true, 'active': index === activeIndex }"></i>
        </div>
        <img @click="prevQuote()" class="slide-prev" src="/svg/prev.svg" alt="">
        <img @click="nextQuote()" class="slide-next" src="/svg/next.svg" alt="">
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

#jumbo-quotes {
    background-image: url('/img/h3-testimonials-bckgrnd.jpg');
    margin-bottom: $smallMargin;
    width: 100%;
    padding: 105px 0 120px;
    position: relative;

    .quote {
        height: 55px;
        margin-bottom: 55px;
    }

    .control {
        margin-top: 30px;

        display: flex;
        justify-content: center;
        gap: 5px;

        i {
            font-size: .5em;
            color: $accentLight;

            &.active {
                color: $accent;
            }
        }
    }

    .slide-prev {
        position: absolute;
        top: 50%;
        left: 0;
        height: 100px;
        transform: translateY(-50%);
        cursor: pointer;

    }

    .slide-next {
        position: absolute;
        top: 50%;
        right: 0;
        height: 100px;
        transform: translateY(-50%);
        cursor: pointer;
    }
}
</style>