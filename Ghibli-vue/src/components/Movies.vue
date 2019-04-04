<template>
    <div>
        <h3>{{movie.title}}</h3>
        <p>{{movie.description}}</p>
    </div>
</template>

<script>
export default {
    name: 'Movies',
    props: ["movies"]
}
</script>

<style scoped>
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


