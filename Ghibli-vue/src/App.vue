<template>
  <div id="app">
    <Logo />
    <Card v-bind:movies="movies" />
  </div>
</template>

<script>
import Logo from './components/Logo';
import Card from './components/Card';
import axios from 'axios';

export default {
  name: 'app',
  components: {
    Logo,
    Card
  },
  data() {
    return {
      movies: []
    }
  },
  created() {
    axios.get(`https://ghibliapi.herokuapp.com/films/`)
    .then(res => this.movies = res.data)
    .catch(err => console.log(err));
  }
}
</script>

<style>
* {
  box-sizing: border-box;
}

html {
    background:-webkit-gradient(linear, left top, right bottom, from(#24C6DC), to(#514A9D));
    background:-webkit-linear-gradient(top left, #24C6DC, #514A9D);
    background:-o-linear-gradient(top left, #24C6DC, #514A9D);
    background:linear-gradient(to bottom right, #24C6DC, #514A9D);
    font-family: 'Nunito', 'sans-serif';
}

#app {
  max-width: 1200px;
  margin: 0 auto;
}

.container {
  display: flex;
  flex-wrap: wrap;
}
</style>
