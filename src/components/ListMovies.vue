<script>
export default {
    name: "ListMovies",
    props: {
        items: Object,
    }
}
</script>

<template>
    <div class="thumb">
        <div class="container-img">
            <img :src="items.thumb" :alt="items.series">
        </div>
        <div class="thumb-title">
            {{ items.series }}
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;

.thumb {
    width: 10vw;
    height: 10vw;
    color: white;
    margin-bottom: 70px;

    .container-img {
        height: 100%;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    .thumb-title {
        margin-top: 18px;
        font-size: 15px;
        text-transform: uppercase;
    }
}

// Qui ci andrà l'scss relativo al solo componente
</style>

