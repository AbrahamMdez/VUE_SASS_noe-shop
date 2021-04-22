<template>
    <main class="main">
        <h1 class="main__h1">PRODUCTOS</h1>

        <section class="main__section">
            <article v-for="product in items" :key="product.id" class="main__article-first-child">
                <img :src="product.image" :alt="hola" class="main__img">
                <h5 class="main__name">{{product.name}}</h5>
                <p class="main__price">{{product.price}}</p>
                <a class="main__buy" :href="product.button_link">{{product.button_text}}</a>
            </article>

            <article class="main__article-second-child">
                <img class="main__article-second-child-img" src="../assets/cta/cta1.jpg" alt="">
            </article>

            <article class="main__article-third-child">
                <img class="main__article-third-child-img" src="../assets/cta/cta2.jpg" alt="">
            </article>
        </section>
    </main>
</template>

<script>
import products from '../assets/data/products.json'

export default {
    name: 'Main',

    computed: {
        items() {
            return products.map((product) => {
                return product
            })
        }
    }
}
</script>

<style lang="scss" scoped>

    .main {
        height: 75vh;
        width: 100vw;

        .main__h1 {
            text-align: center;
            font-size: 1rem;
            padding: 1vh;
        }

        .main__section {
            width: inherit;
            height: 70.5vh;
            width: 75vw;
            margin: auto;
            display: grid;
            grid-template-columns: repeat( 3, 25vw);
            grid-template-rows: repeat(4, 13vh);

            .main__article-first-child {
                display: grid;
                grid-template-areas: "s s"
                                    "t p"
                                    "b b";
                grid-template-columns: repeat(2, 20vw 5vw);
            }

            .main__img {
                grid-area: s;
                height: 5vh;
                width: 12vw;
                align-self: center;
                justify-self: center;
            }

            .main__name {
                grid-area: t;
                font-size: 0.5rem;
                align-self: center;
                justify-self: center;
            }

            .main__price {
                grid-area: p;
                font-size: 0.5rem;
                align-self: center;
                justify-self: center;
                background-color: var(--color-price);
            }

            .main__buy {
                grid-area: b;
                font-size: 0.5rem;
                align-self: center;
                justify-self: center;
                background-color: var(--color-button);
                color: var(--text-color);
            }
        }

        .main__article-second-child {
            grid-column-start: 2;
            grid-column-end: 4;
            grid-row-start: 2;

            .main__article-second-child-img {
                height: 28vw;
                width: 50vw;
                object-fit: cover;
                object-position: bottom center;
            }
        }

        .main__article-third-child {
            grid-column-start: 1;
            grid-column-end: 3;
            grid-row-start: 4;

            .main__article-third-child-img {
                height: 13vh;
                width: 50vw;
                object-fit: cover;
                object-position: bottom center;
            }
        }
    }
    

</style>