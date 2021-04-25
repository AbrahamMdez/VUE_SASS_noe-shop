<template>
    <header class="header">
        <ul class="header__list">
            <li>
                <figcaption class="header__figcaption">
                    <router-link to="/">
                        <img class="header__logo" src="../assets/logo.png" alt="Logotipo de Neoshop" title="Neoshop" />
                    </router-link>
                </figcaption>
            </li>

            <li>
                <i class="fas fa-shopping-cart header__icon"></i>
            </li>

            <li>
                <i class="fas fa-user header__icon"></i>
            </li>

            <li>
                <i class="fas fa-box-open header__icon"></i>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style lang="scss" scoped>
    .header {
        padding: 1vh;

    .header__list {
        height: inherit;
        width: inherit;
        display: flex;
        justify-content: flex-end;

        .header__logo {
            position: absolute;
            left: 0;
            padding-left: 1vh;
            height: 2vh;
            align-self: flex-start;
        }

        .header__icon {
            font-size: 0.7rem;
            color: var(--color-icons);
            padding-right: 2vh;
        }
    }  
}
</style>