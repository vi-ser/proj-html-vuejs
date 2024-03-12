<script>
export default {
    name: 'NavLink',

    props: {
        link: Object,
    }
}
</script>

<template>
    <li>
        <a :href="link.url">{{ link.name }}</a>
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {

    a {
        text-decoration: none;
        color: white;
        font-size: .8em;
        letter-spacing: 2px;
        padding: 15px;
    }

    &:first-of-type {
        position: relative;
        // margin-left: 75px;
    }

    &:first-of-type::before {
        content: '';
        background-image: url('/svg/svg-0.svg');
        background-size: contain;
        background-repeat: no-repeat;
        position: absolute;
        left: -10px;
        top: 100%;
        transform: translateY(-100%);
        width: 20px;
        height: 15px;
    }

    &:nth-of-type(3) {
        margin-right: 180px;
    }
}
</style>