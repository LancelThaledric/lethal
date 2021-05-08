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

  &:hover {
    color: #e00;
  }
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