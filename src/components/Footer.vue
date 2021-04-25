<template>
    <footer class="footer">
        <figcaption class="footer__figurecaption">
            <img class="footer__figurecaption__img" src="../assets/logo.png" alt="Neoshop" title="Neoshop" />
        </figcaption>
        
        <p class="footer__description">Prueba técnica para candidatos</p>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style lang="scss" scoped>

    .footer {
        height: 10vh;
        display: flex;
        flex-direction: column;
        align-items: center;

        .footer__figurecaption__img,
        .footer__description {
            height: 2vh;
            font-size: 0.5rem;
        }
    }

</style>