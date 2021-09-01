<template>
  <nav class="app-nav-wrapper">
          <ul class="nav-list">
              <li class="nav-list__item">
                <router-link class="nav-list__router-link" to="/">Home</router-link>
              </li>
              <li class="nav-list__item">
                <router-link class="nav-list__router-link" to="/about">About</router-link>
              </li>
              <li class="nav-list__item">
                <router-link class="nav-list__router-link" to="/ComingSoon">
                 Coming Soon
                </router-link>
              </li>
          </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar',
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style lang="scss" scoped>
  @import '@/assets/styles/_style.scss';
  @font-face {
  font-family: 'Norwester';
  src: url('../../assets/fonts/norwester/norwester.otf');
  }
  .nav-list {
    display: flex;
    flex-wrap: wrap;
    font-family: 'Norwester';

    &__item {
      list-style: none;
      font-size: 18px;
      padding: 10px 10px;
      color: $main;
      text-shadow: 0 0 20px rgba($main, 0);
      @include textShadowHover;
    }

    &__router-link {
      text-decoration: none;
      color: $main;
    }
  }
</style>
