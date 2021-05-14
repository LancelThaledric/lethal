<template>
  <Header/>
  <router-view/>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
}

html {
  font-size: 16px; // rem definition
}

body {
  margin: 0;
  font-size: 14px;
}

p {
  line-height: 1.75rem;
}

#app { /* #app tag is include in @/public/index.html */
  font-family: 'Montserrat', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #111;

  display: flex; flex-direction: column;
}

a {
  color: #c02;
  text-decoration: none;

  &:hover {
    color: #e00;
  }
}

h1, h2, h3, h4, h5, h6 {
  font-family: "Poiret One", cursive;
  font-size: 2em;
  font-weight: normal;
  margin-left: 6rem;
}
</style>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';

import Header from '@/components/Header.vue';

@Options({
  components: {
    Header
  }
})
export default class HelloWorld extends Vue {}
</script>