<script>
export default {
    name: "AppHeader",
}
</script>

<template>
    <header>
        <!-- logo principale -->
        <div class="logo-box">
            <a href="#">
                <img src="/dc-logo.png" alt="dc-logo">
            </a>
        </div>

        <nav>
            <ul>
                <li>
                    <a href="#">CHARACTERS</a>
                </li>

                <li>
                    <a href="#" class="active">COMICS</a>
                </li>

                <li>
                    <a href="#">MOVIES</a>
                </li>

                <li>
                    <a href="#">TV</a>
                </li>

                <li>
                    <a href="#">GAMES</a>
                </li>

                <li>
                    <a href="#">COLLECTIBLES</a>
                </li>

                <li>
                    <a href="#">VIDEOS</a>
                </li>

                <li>
                    <a href="#">FANS</a>
                </li>

                <li>
                    <a href="#">NEWS</a>
                </li>

                <li>
                    <a href="#">SHOP</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

header {
    height: 140px;
    @include center('horizontal');
    background: lightblue;
    justify-content: space-between;

    ul {
        list-style: none;
        @include center();

        li a {
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;
            transition: background 0.3s;

            &.active,
            &:hover {
                background: lighten($primary, 70%);
            }
        }
    }
}




// Qui ci andrà l'scss relativo al solo componente
</style>
