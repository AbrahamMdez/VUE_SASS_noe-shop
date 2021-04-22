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

<style lang="scss">

    .main {
       height: 65vh;
       width: 100vw;

       .main__h1 {
           text-align: center;
           font-size: 1rem;
           padding: 1vh;
       }

       .main__section {
           display: grid;
           height: 50vh;
           width: 75vw;
           margin: auto;
           grid-template-columns: repeat( 3, 20vw);
           grid-template-rows: repeat(4, 16vh);

           .main__article-first-child {
               padding: 1vh;
               width: 20vw;
               display: grid;
               grid-template-areas: "s s"
                                    "t p"
                                    "b b";

               .main__img {
                   grid-area: s;
                   height: 10vh;
                   width: 12vw;
                   object-fit: contain;
               }

               .main__name {
                   grid-area: t;
               }

               .main__price {
                   grid-area: p;
                   background-color: var(--color-icons);
                   color: var(--color-text-price);
               }

               .main__buy {
                   grid-area: b;
                   background-color: var(--color-button);
                   color: var(--text-color);
                   font-size: 0.8rem;
                   width: 5vw;
                   align-self: center;
               }
           }
           
           .main__article-second-child {

               grid-column-start: 2;
               grid-column-end: 4;
               grid-row-start: 2;

               .main__article-second-child-img {
                    height: 15vh;
                    width: 40vw;
                    object-fit: cover;   
                }

            }

            .main__article-third-child {
                grid-column-start: 1;
                grid-column-end: 3;
                grid-row-start: 4;

                .main__article-third-child-img {
                    height: 15vh;
                    width: 40vw;
                    object-fit: cover; 
               }
            }
        } 
    }

</style>