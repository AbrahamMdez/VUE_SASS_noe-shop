<template>
    <!-- ESTA ES LA FORMA ITERANDO EL JSON -->

    <!-- <section class="wrapper">
        <carrusel-slide class="wrapper__carrusel" v-for="slide in items" :key="slide.id" >
            <img class="wrapper__img" :src="slide.bg_image" :alt="slide.title">
        </carrusel-slide>
    </section> -->

    <section class="slider">
        <ul class="slider__container">
            <li class="slider__component">
                <img class="slider__img" src="https://www.futboltotal.com.mx/wp-content/uploads/2020/07/vans-1.jpg" alt="imagen de persona usando un monopatin">
            </li>

            <li>
                <img class="slider__img" src="https://gmedia.playstation.com/is/image/SIEPDC/tony-hawks-pro-skater-1-2-screen-13-ps4-en-08jul20?$native$" alt="imagen de skatepark">
            </li>

            <li>
                <img class="slider__img" src="https://i.ytimg.com/vi/KtxpjifbDHQ/maxresdefault.jpg" alt="imagen de surfista">
            </li>
                
            <li>
                <img class="slider__img" src="https://www.academy.com/content/dam/academysports/promotional-assets/2019/brands/vans/vans_hero_updated.jpg" alt="varias imagenes de personas publicitando vans">
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

    /* LAS CLASES DE EJEMPLO ITERANDO EL JSON */
    /* .wrapper {
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
    } */

    .slider {
        width: 100vw;
        height: 15vh;
        overflow: hidden;

        .slider__container {
            display: flex;
            width: 100vw;
            height: inherit;
            animation: change 20s infinite alternate linear;

            .slider__component {
                width: inherit;
                height: inherit;

                .slider__img {
                    width: inherit;
                    height: inherit;
                    object-fit: cover;
                }
                
            }
        }
    }

    @keyframes change {

        0% { margin-left: 0; }
        20% { margin-left: 0; }

        25% { margin-left: -100; }
        45% { margin-left: -100; }

        50% { margin-left: -200; }
        70% { margin-left: -200; }

        75% { margin-left: -300; }
        100% { margin-left: -300; }
    }

</style>