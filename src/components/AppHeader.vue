<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    status: false,
                },
                {
                    text: "COMICS",
                    status: true,
                },
                {
                    text: "MOVIES",
                    status: false,
                },
                {
                    text: "TV",
                    status: false,
                },
                {
                    text: "GAMES",
                    status: false,
                },
                {
                    text: "COLLECTIBLES",
                    status: false,
                },
                {
                    text: "VIDEOS",
                    status: false,
                },
                {
                    text: "FANS",
                    status: false,
                },
                {
                    text: "NEWS",
                    status: false,
                },
                {
                    text: "SHOP",
                    status: false,
                },

            ]
        }
    }, methods: {
        activeLink(i) {
            if (this.links[i].status === false) {
                this.links[i].status = true;
            } else {
                this.links[i].status = false;
            }
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
                    <li v-for="(link, i) in links" :key="i"><a href="#" :class="link.status ? 'active' : ''"
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
    background: lightblue;

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
                    padding: 43px 0;

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
