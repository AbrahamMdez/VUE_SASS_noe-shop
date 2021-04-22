import Footer from '@/components/Footer.vue';
<template>
    <footer class="footer">
        <figurecaption class="footer__figurecaption">
            <img class="footer__figurecaption__img" src="../assets/logo.png" alt="Neoshop" title="Neoshop" />
        </figurecaption>
        
        <p>Prueba técnica para candidatos</p>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style lang="scss">

    .footer {
        height: 10vh;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

</style>