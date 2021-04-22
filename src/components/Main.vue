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

       .main__h1 {
           text-align: center;
           font-size: 1rem;
       }

       .main__section {
           display: grid;
           width: 75vw;
           margin: auto;
           grid-template-columns: repeat( 3, 1fr);

           .main__article-first-child {

               .main__img {
                
               }

               .main__name {

               }

               .main__price {
                   
               }

               .main__buy {
                   background-color: black;
                   color: white;
                   font-size: 0.8rem;
               }
           }
           
           .main__article-second-child {

               grid-column-start: 2;
               grid-column-end: 4;
               grid-row-start: 2;

               .main__article-second-child-img {
                    height: 15vh;
                    width: 25vw;
                }

            }

            .main__article-third-child {
                grid-column-start: 1;
                grid-column-end: 3;
                grid-row-start: 4;

                .main__article-third-child-img {
                    height: 15vh;
                    width: 25vw;
               }
            }
        } 
    }

</style>