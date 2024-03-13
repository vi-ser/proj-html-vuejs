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
        <div class="front-card">
            <img :src="team.img" :alt="team.name">
        </div>
        <div class="back-card d-flex justify-content-center align-items-center">
            <div class="info-container d-flex flex-column justify-content-center align-items-center">
                <span class="team-name text-white text-uppercase oswald-medium">{{ team.name }}</span>
                <span class="team-job text-white">{{ team.profession }}</span>
                <div class="links d-flex">
                    <a v-for="currentLink in team.social_links" :key="currentLink.platform" :href="currentLink.link"
                        target="_blank"><i :class="'fab ' + currentLink.platform"></i></a>
                </div>

            </div>

        </div>
    </li>
</template>

<style lang="scss" scoped>
@use '../styles/general' as *;
@use '../styles/_variables' as *;

li {
    width: calc(100% / 4);
    position: relative;

    .front-card {

        img {
            width: 100%;
        }

    }

    .back-card {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background-image: url('/img/pattern.png');
        opacity: 0;

        .info-container {
            height: 70%;
            width: 70%;
            background-color: $primary;
            transition: transform 0.3s ease;


            .team-name {
                font-size: 1.2em;
            }

            .team-job {
                font-size: .8em;
                margin-bottom: 10px;
            }

            .links {
                gap: 20px;

                a {
                    text-decoration: none;
                    color: white;
                    font-size: .8em;
                }
            }
        }
    }

    &:hover .back-card {
        opacity: 1;
    }

    &:hover .back-card .info-container {
        transform: scale(1.2);
    }
}
</style>