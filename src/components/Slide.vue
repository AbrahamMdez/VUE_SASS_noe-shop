<template>
    <section class="wrapper">
        <ul class="wrapper__ul" v-for="slide in items" :key="slide.id">
            <li class="wrapper__li">
                <img class="wrapper__img" :src="slide.bg_image" :alt="slide.title">
            </li>
        </ul>
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
        height: 20vh;
    }

</style>