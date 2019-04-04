<template>
  <div id="app">
    <div class="container">

    </div>
  </div>
</template>

<script>
import HelloWorld from './components/Logo.vue'
import axios from 'axios';

export default {
  name: 'app',
  components: {
    Logo
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
