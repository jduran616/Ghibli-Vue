<template>
    <div class="container">
        <div class="card" v-bind:key="movie.id" v-for="movie in movies">
            <h1>{{movie.title}}</h1>
            <p>{{movie.description}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Card",
    props: ["movies"]
}
</script>

<style scoped>
    .card {
        margin: 1rem;
        border: 1px solid rgb(103, 63, 126)#EEEEEE;
        border-radius: 1rem;
        background: rgb(179, 111, 145);
        overflow: hidden;
        box-shadow: 2px 4px 25px rgba(0, 0, 0, 0.3);
    }

    .card:hover {
        box-shadow: 2px 8px 45px rgba(95, 21, 105, 0.3);
        transform: translate3D(0, -2px, 0);
    }

    @media screen and (min-width: 600px) {
        .card {
            flex: 1 1 calc(50% - 2rem);
        }
    }

    @media screen and (min-width: 900px) {
        .card {
            flex: 1 1 calc(33% - 2rem);
        }
    }

    h1 {
        text-align: center;
        margin: 0 0 2rem 0;
        padding: 1rem 2rem;
        font-size: 1.5rem;
    }

    p {
        line-height: 1.5rem;
        padding: 0 1.5rem 1.5rem;
        color: rgb(77, 20, 62);
    }
</style>
