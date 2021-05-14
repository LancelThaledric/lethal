<template>
  <div class="home">
    <section class="lt-feature">
      <div class="text-feature feature-left">
        <h1>Hello !</h1>
        <p>
          Enchanté, je suis Valentin Mourot,
          <a href="https://www.ingenieur-imac.fr/">ingénieur IMAC</a> spécialisé
          en programmation, mais j'ai bien d'autres cartes dans ma manche.
          Parcourez mon site pour en savoir plus !
        </p>
      </div>
      <div class="card-feature feature-right">
        <div class="card-container">
          <img class="lt-card card-profile-1" src="@/assets/card-dummy.png" />
          <img class="lt-card card-profile-2" src="@/assets/card-dummy.png" />
          <img class="lt-card card-profile" src="@/assets/card-dummy.png" />
        </div>
      </div>
    </section>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({})
export default class Home extends Vue {}
</script>

<style lang="scss" scoped>
.lt-feature {
  display: flex;
  margin: auto;
  width: 80%;

  .text-feature {
    flex: 7;
    display: flex;
    flex-direction: column;
  }
  .card-feature {
    flex: 5;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    position: relative;
    height: 6rem;
  }

  .feature-left {
    order: 1;
  }
  .feature-right {
    order: 2;
  }
}

@media (max-width: 768px) {
  // Tablets and smaller
  .lt-feature {
    flex-direction: column;

    .card-feature {
      &.feature-left {
        align-items: center;
      }
      &.feature-right {
        align-items: center;
      }
    }
  }
}

.card-container {
  position: relative;
  height: 6 * 3.5rem;
  align-self: stretch;
  display: flex;
  justify-content: center;
  align-items: center;
}

.lt-card {
  width: 6 * 2.5rem;
  height: 6 * 3.5rem;
  border-radius: 0.08 * 6 * 2.5rem;
  border-width: 0;
  background: silver;
  margin: auto;
  position: absolute;
  box-shadow: rgba(#000, 0.1) 0 0.8rem 2rem;

  &.card-profile {
    transform: scale(1.15) rotate(5deg);
    z-index: 100;
  }
  &.card-profile-1 {
    transform: rotate(-5deg) translate(-3.5rem, 1rem);
    z-index: 100;
  }
  &.card-profile-2 {
    transform: rotate(15deg) translate(3rem, 0);
    z-index: 100;
  }
}

@media (max-width: 1024px) {
  .lt-card {
    width: 4 * 2.5rem;
    height: 4 * 3.5rem;
    border-radius: 0.08 * 4 * 2.5rem;

    &.card-profile {
      transform: scale(1.15) rotate(5deg);
    }
    &.card-profile-1 {
      transform: rotate(-5deg) translate(0.66*(-3.5rem), 0.666rem);
    }
    &.card-profile-2 {
      transform: rotate(15deg) translate(2rem, 0);
    }
  }
}
</style>