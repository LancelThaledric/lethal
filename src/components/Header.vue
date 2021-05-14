<template>
  <header class="lt-header">
    <div class="lt-header-blur-0">
      <div class="lt-header-inner">
        <router-link to="/" class="lt-logo">Le Thal'</router-link>
        <ul class="lt-nav"></ul>
      </div>
    </div>
  </header>
  <div class="lt-header-spacer" />
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({})
export default class LTHeader extends Vue {}
</script>

<style scoped lang="scss">
@import "@/ui/gradient.scss";

.lt-header {
  position: fixed;
  width: 100%;
  background: rgba(#fff, 0.95);
  z-index: 100;

  &::before {
    content: "";
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    height: 6rem;
    @include quad-easing-gradient(to top, rgba(#fff, 0.95));
  }
}
.lt-header-inner {
  display: flex;

  margin: 3rem auto 1rem;
  width: 80%;
}
.lt-header-blur-0 {
  backdrop-filter: blur(10px);
	display: flex;
}

.lt-logo {
  font-size: 3rem;
  font-family: "Poiret One", cursive;
  color: inherit;
  text-decoration: inherit;
}

.lt-header-spacer {
  height: 15rem;
}
</style>