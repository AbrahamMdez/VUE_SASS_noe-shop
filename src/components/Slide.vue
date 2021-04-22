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

<style lang="scss" scoped>

    .wrapper {
        width: 100vw;
        height: 15vh;
        overflow: hidden;

        .wrapper__carrusel {
            width: inherit;
            height: inherit;

            .wrapper__img {
                width: inherit;
                height: inherit;
                object-fit: cover;
            }
        }
    }

</style>