<template>
  <header class="app-header">
      <Logo />
      <NavBar />
  </header>
</template>

<script>

import NavBar from '@/components/sections/NavBar.vue';
import Logo from '@/components/sections/Logo.vue';

export default {
  name: 'AppHeader',
  components: {
    NavBar,
    Logo,
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/styles/_style.scss';
.app-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 60px;
    background-color: black;
    background-image: url('../assets/img/main-bg.jpeg');
    background-attachment: fixed;
    border-bottom: 2px solid $main;
}
@media screen and (max-width: 400px) {
  .app-header {
    flex-direction: column;
    justify-content: center;
  };
};
</style>
