<template>
    <!-- ESTA ES LA FORMA ITERANDO EL JSON -->

    <!-- <section class="wrapper">
        <carrusel-slide class="wrapper__carrusel" v-for="slide in items" :key="slide.id" >
            <img class="wrapper__img" :src="slide.bg_image" :alt="slide.title">
        </carrusel-slide>
    </section> -->

    <section class="slide">

        <input type="radio" id="1" name="img-slide" hidden />
        <input type="radio" id="2" name="img-slide" hidden />
        <input type="radio" id="3" name="img-slide" hidden />
        <input type="radio" id="4" name="img-slide" hidden />

        <ul class="slide__container">
            <li class="slide__component">
                <img class="slide__img" src="https://www.futboltotal.com.mx/wp-content/uploads/2020/07/vans-1.jpg" alt="imagen de persona usando un monopatin">
            </li>

            <li class="slide__component">
                <img class="slide__img" src="https://gmedia.playstation.com/is/image/SIEPDC/tony-hawks-pro-skater-1-2-screen-13-ps4-en-08jul20?$native$" alt="imagen de skatepark">
            </li>

            <li class="slide__component">
                <img class="slide__img" src="https://i.ytimg.com/vi/KtxpjifbDHQ/maxresdefault.jpg" alt="imagen de surfista">
            </li>
                
            <li class="slide__component">
                <img class="slide__img" src="https://www.academy.com/content/dam/academysports/promotional-assets/2019/brands/vans/vans_hero_updated.jpg" alt="varias imagenes de personas publicitando vans">
            </li>
        </ul>

        <ul class="pagination">
            <label class="pagination-item" for="1">
                <img class="pagination-img" src="https://www.futboltotal.com.mx/wp-content/uploads/2020/07/vans-1.jpg" alt="imagen de persona usando un monopatin">
            </label>

            <label class="pagination-item" for="2">
                <img class="pagination-img" src="https://gmedia.playstation.com/is/image/SIEPDC/tony-hawks-pro-skater-1-2-screen-13-ps4-en-08jul20?$native$" alt="imagen de persona usando un monopatin">
            </label>

            <label class="pagination-item" for="3">
                <img class="pagination-img" src="https://i.ytimg.com/vi/KtxpjifbDHQ/maxresdefault.jpg" alt="imagen de persona usando un monopatin">
            </label>

            <label class="pagination-item" for="4">
                <img class="pagination-img" src="https://www.academy.com/content/dam/academysports/promotional-assets/2019/brands/vans/vans_hero_updated.jpg" alt="imagen de persona usando un monopatin">
            </label>
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

    .slide {
        position: relative;
        width: 100vw;
        height: 15vh;
        overflow: hidden;

        .slide__container {
            display: flex;
            transform: translate3d( 0, 0, 0);
            transition: all 600ms;
            animation-name: autoplay;
            animation-duration: 6.5s;
            animation-direction: alternate;
            animation-fill-mode: forwards;
            animation-iteration-count: infinite;

            .slide__component {
                position: relative;
                display: flex;
                flex-direction: column;
                flex-shrink: 0;
                flex-grow: 0;
                width: 100vw;
            }
        }

        .pagination {
            position: absolute;
            bottom: 20px;
            left: 0;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            width: 100vw;

            .pagination-item {
                display: flex;
                flex-direction: column;
                align-items: center;
                border: 2px solid white;
                width: 16px; 
                height: 16px;
                border-radius: 5px;
                overflow: hidden;
                cursor: pointer;
                margin: 0 10px;
                text-align: center;
                transition: all 300ms;

                .pagination-img {
                    display: inline-block;
                    height: 100vw;
                    transform: scale(1);
                    opacity: 0;
                    transition: all 300ms;
                }
            }

            .pagination-item:hover {
                    transform: scale(2);
                }

            .pagination-img:hover {
                opacity: 1;
                transform: scale(1);
            }
        }

        input[id="1"]:checked ~ .slide {
            animation: none;
            transform: translate3d( 0, 0, 0);
        }

        input[id="1"]:checked ~ .pagination .pagination-item[for="1"] {
            background: #fff;
        }

        input[id="2"]:checked ~ .slide {
            animation: none;
            transform: translate3d(calc(-100% * 1), 0, 0);
        }

        input[id="2"]:checked ~ .pagination .pagination-item[for="2"] {
            background: #fff;
        }

        input[id="3"]:checked ~ .slide {
            animation: none;
            transform: translate3d(calc(-100% * 2), 0, 0);
        }

        input[id="3"]:checked ~ .pagination .pagination-item[for="3"] {
            background: #fff;
        }

    @keyframes autoplay {
        25% {
            transform: translate3d(cacl(-100% * 0), 0, 0);
        }

        50% {
            transform: translate3d(cacl(-100% * 1), 0, 0);
        }

        75% {
            transform: translate3d(cacl(-100% * 2), 0, 0);
        }

        100% {
            transform: translate3d(cacl(-100% * 3), 0, 0);
        }
    }
}
</style>