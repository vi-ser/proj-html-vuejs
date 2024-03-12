<script>
export default {
    name: 'HoursItem',

    props: {
        hour: Object,
    }
}
</script>

<template>
    <li>
        <span class="working-day oswald-medium text-uppercase">{{ hour.day }}</span><br>
        <span class="working-hours">{{ hour.working_hour }}</span>
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {
    margin-bottom: 25px;

    span {
        color: $textLight;
        font-size: .8em;
    }

    .working-day {
        color: $accent;
    }

    &:first-of-type .working-hours {
        color: $primary;
    }
}
</style>