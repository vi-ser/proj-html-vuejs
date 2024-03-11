<script>
export default {
    name: 'AppFooter',
}
</script>

<template>
    <footer class="d-flex">
        <div class="footer-left"></div>
        <div class="footer-right">
        </div>
    </footer>


</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

footer {

    height: 640px;

    .footer-left {
        width: 50%;
        background-image: url('/img/cielostellato.PNG');
        padding: 125px 50px 35px;
    }

    .footer-right {
        width: 50%;
        background-image: url('/img/footer-img-1.jpg');
        background-size: cover;
        background-position: center;
    }
}
</style>