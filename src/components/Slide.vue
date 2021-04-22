<template>
    <section class="wrapper">
        <carrusel-slide class="wrapper__carrusel" v-for="slide in items" :key="slide.id" >
            <img class="wrapper__img" :src="slide.bg_image" :alt="slide.title">
        </carrusel-slide>
    </section>
</template>

<script>
import allSlides from '../assets/data/slides.json'

export default {
    name: 'Slide',

    computed: {
        items() {
            return allSlides.map((slide) => {
                return slide
            })
        }
    }
}
</script>

<style lang="scss">

    .wrapper {
        width: 100vw;
        height: 20vh;
        overflow: hidden;

        .wrapper__carrusel {
            width: inherit;
            height: inherit;

            /* animation: change 20s infinite alternate; */

            .wrapper__img {
                width: inherit;
                height: inherit;
                object-fit: cover;
            }
        }

    }


@keyframes change {
    0% { margin-left: 0; }
    20% { margin-left: 0; }

    25% { margin-left: -100%; }
    45% { margin-left: -100%; }

    50% { margin-left: -200%; }
    70% { margin-left: -200%; }

    75% { margin-left: -300%; }
    100% { margin-left: -300%; }
}

</style>