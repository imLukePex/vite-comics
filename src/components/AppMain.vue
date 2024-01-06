<script>
import ListMovies from './ListMovies.vue'

export default {
    name: "AppMain",
    components: {
        ListMovies,
    },
    data() {
        return {
            thumbs: [
                {
                    "thumb": "https://m.media-amazon.com/images/I/91ytkCTqkEL._AC_UF1000,1000_QL80_.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/51bGFqxJZfL.jpg",
                    "price": "$19.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.washingtonpost.com/news/comic-riffs/wp-content/uploads/sites/15/2017/06/AQM_Cv25_ds.jpg",
                    "price": "$19.99",
                    "series": "Aquaman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://upload.wikimedia.org/wikipedia/it/0/0e/Batgirl_1.jpg",
                    "price": "$19.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://upload.wikimedia.org/wikipedia/it/1/19/Batman_3_variant.jpg",
                    "price": "$19.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://mycomics.it/wp-content/uploads/sites/16/2022/12/FUMBBNEOY0001.jpg",
                    "price": "$19.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://mycomics.it/wp-content/uploads/sites/16/2022/01/FUMBATSUP0017-1.jpg",
                    "price": "$19.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/51galZVEAtL.jpg",
                    "price": "$19.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/41nGyVF7C2L.jpg",
                    "price": "$19.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/51UyCo72BYL.jpg",
                    "price": "$19.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/91uTUXN0sNS._AC_UF1000,1000_QL80_.jpg",
                    "price": "$19.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://m.media-amazon.com/images/I/915qnY5eVdL._AC_UF1000,1000_QL80_.jpg",
                    "price": "$19.99",
                    "series": "Catwoman",
                    "type": "comic book"
                },
            ]
        }
    }
}
</script>

<template>
    <main>
        <div class="jumbotron">
            <div class="container label">
                <div class="label">CURRENT SERIES</div>
            </div>
        </div>
        <div class="container">
            <ListMovies v-for="(item, i) in thumbs" :key="i" :items="item" />
            <a href="#" class="button">LOAD MORE</a>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;
@use '../styles/general.scss' as *;

main {
    background-color: #1c1c1c;

    .jumbotron {
        background-image: url(/jumbotron.jpg);
        height: 430px;
        background-size: cover;
        position: relative;
        margin-bottom: 70px;

        .container.label {
            position: absolute;
            left: 15%;
            bottom: -30px;
            padding-bottom: 0;

            .label {
                background-color: $primary;
                padding: 10px 30px;
                color: #ffff;
                font-size: 25px;
                font-weight: bold;
                border-radius: 5px;
            }
        }
    }

    .container {
        @include space();
        flex-wrap: wrap;
        padding-bottom: 100px;
        position: relative;

        .button {
            background-color: $primary;
            padding: 10px 60px;
            color: white;
            font-size: 14px;
            font-weight: bold;
            border-radius: 5px;
            margin-bottom: 20px;
            text-decoration: none;
            position: absolute;
            left: 50%;
            bottom: 0;
            transform: translate(-50%);
            text-align: center;
        }
    }
}

// Qui ci andrà l'scss relativo al solo componente
</style>

