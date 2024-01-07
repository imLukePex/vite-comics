<script>
export default {
    name: "AppHeader",
    data() {
        return {
            activeMenu: 1,

            links: [
                {
                    text: "CHARACTERS"
                },
                {
                    text: "COMICS"
                },
                {
                    text: "MOVIES"
                },
                {
                    text: "TV"
                },
                {
                    text: "GAMES"
                },
                {
                    text: "COLLECTIBLES"
                },
                {
                    text: "VIDEOS"
                },
                {
                    text: "FANS"
                },
                {
                    text: "NEWS"
                },
                {
                    text: "SHOP"
                },

            ]
        }
    }, methods: {
        activeLink(i) {
            this.activeMenu = i;
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <!-- logo principale -->
            <div class="logo-box">
                <a href="#">
                    <img src="/dc-logo.png" alt="dc-logo">
                </a>
            </div>

            <nav>
                <ul>
                    <li v-for="(link, i) in links" :key="i"><a href="#" :class="activeMenu === i ? 'active' : ''"
                            @click="activeLink(i)">{{ link.text
                            }}</a></li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;

header {
    height: 120px;
    width: 100%;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 500;
    background: #ffff;
    box-shadow: 0 4px 5px -4px gray;

    .container {
        @include center();
        height: 100%;
        justify-content: space-between;

        .logo-box {
            width: 80px;
        }

        ul {
            list-style: none;
            @include center();
            justify-content: space-between;

            li {
                padding-left: 25px;

                a {
                    text-decoration: none;
                    color: #000;
                    font-size: 15px;
                    font-weight: 500;
                    padding: 44px 0;

                    &.active,
                    &:hover {
                        color: $primary;
                    }

                    &.active {
                        border-bottom: 5px solid $primary;
                    }

                }
            }

        }
    }
}

// Qui ci andrà l'scss relativo al solo componente
</style>
