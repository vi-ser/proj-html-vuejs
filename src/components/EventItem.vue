<script>
export default {
    name: 'EventItem',

    props: {
        event: Object,
    },

}
</script>

<template>
    <li class="d-flex flex-column">
        <div class="menu d-flex justify-content-start gap-4">
            <div class="date d-flex flex-column text-center">
                <span class="day oswald-bold">{{ event.day }}</span>
                <span class="month oswald-medium text-uppercase">{{ event.month }}</span>
            </div>

            <div class="info d-flex flex-column">
                <span class="name text-uppercase oswald-medium">{{ event.name }}</span>
                <span class="location"><i class="fa-solid fa-location-dot"></i> {{ event.location }}</span>
            </div>
        </div>
        <hr style="border: 1px dashed #B7903C; opacity: 1; margin-bottom: 45px;" />
    </li>

</template>


<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {

    &:first-child {
        padding-top: 0;
    }

    &:last-child {
        padding-bottom: 0;

        hr {
            display: none;
        }
    }


    .menu {


        .date {
            .day {
                color: $primaryDark;
                font-size: 2em;
                line-height: 1em;
            }

            .month {
                color: white;
                font-size: .8em;
            }
        }

        .info {
            .name {
                color: white;
                font-size: 1.2em;
            }

            .location {
                color: $primaryDark;
                font-size: .8em;
                margin-bottom: 45px;
            }
        }

    }

}
</style>