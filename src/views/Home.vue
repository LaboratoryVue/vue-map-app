<template>
  <div class="home">
    <div class="home__map"></div>
    <div class="home__nav">
      <nav class="navigation">
        <a @click="onSelect('moscow')" class="navigation__item" href="#">moscow</a>
        <a @click="onSelect('petersberg')" class="navigation__item" href="#">petersberg</a>
      </nav>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home',
  methods: {
    onSelect(value) {
      console.log(value)
    }
  }
}
</script>

<style lang="scss" scoped>
  .home {
    display: flex;
    // width: 1280px;
    width: 100%;
    height: 720px;
    margin: 0 auto;

    &__map {
      width: 920px;
      height: 100%;
      background-color: black;
    }

    &__nav {
      width: 360px;
      height: 100%;
      background-color: rgba(255,0,0, 0.1);
    }

    & .navigation {
      display: flex;
      flex-direction: column;
      padding: 60px 30px;

      &__item {
        text-transform: uppercase;
        color: black;
        margin-bottom: 1rem;

        &:last-child {
          margin-bottom: 0;
        }

        &:hover,
        &:active {
          color: green;
        }
      }
    }
  }
</style>
