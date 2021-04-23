<template>
    <header class="header">
        <nav class="header__nav">

            <ul class="header__ul">
                <li>
                    <figcaption class="header__figcaption">
                        <router-link to="/">
                            <img class="header__logo" src="../assets/logo.png" alt="Logotipo de Neoshop" title="Neoshop" />
                        </router-link>
                    </figcaption>
                </li>

                <li>
                    <span class="header__icon"><i class="fas fa-shopping-cart"></i></span>
                </li>

                <li>
                    <span class="header__icon"><i class="fas fa-user"></i></span>
                </li>

                <li>
                    <span class="header__icon"><i class="fas fa-box-open"></i></span>
                </li>
            </ul>
        </nav>
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

    .header__nav {
        height: inherit;
        width: inherit;
    }

    .header__ul {
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