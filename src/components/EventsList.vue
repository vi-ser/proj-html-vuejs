<script>
import EventItem from '../components/EventItem.vue'
import { store } from '../store';


export default {
    name: 'EventsList',

    components: {
        EventItem,
    },

    data() {
        return {
            store,
        }
    },
}
</script>

<template>
    <div class="events d-flex">

        <div class="left d-flex align-items-center justify-content-center">
            <div class="events-container">

                <span class="text-uppercase oswald-medium">made with love</span>
                <h2 class="text-uppercase oswald-medium">
                    delish pizza deals </h2>

                <ul class="event-list">
                    <EventItem v-for="currentEvent in store.event" :event="currentEvent"></EventItem>
                </ul>

            </div>
        </div>

        <div class="right d-flex justify-content-center align-items-center">
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

.events {

    margin-bottom: $smallMargin;

    .left {
        width: 50%;
        background-image: url('/img/cielostellato.PNG');
        padding: 0 200px 0 100px;
        color: $text;

        span {
            color: $primaryDark;
            font-size: .8em;
        }

        h2 {
            font-size: 2em;
            margin-bottom: 65px;
            padding: 0;
            color: white;
        }

    }

    .right {
        width: 50%;
        height: 750px;
        background-image: url('/img/h3-img-5a.jpg');
        background-size: cover;
        background-position: center;

        img {
            width: 370px;
        }
    }


}
</style>