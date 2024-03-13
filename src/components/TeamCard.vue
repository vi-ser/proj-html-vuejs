<script>
export default {
    name: 'TeamCard',

    props: {
        team: Object,
    }
}
</script>

<template>
    <li>
        <img :src="team.img" :alt="team.name">
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {
    width: calc(100% / 4);

    img {
        width: 100%;
    }
}
</style>