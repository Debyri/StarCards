<template>
  <div class="logo-wrapper">
    <div class="app-logo">star cards<a href="#app" rel="noopener noreferrer"></a></div>
  </div>
</template>

<script>
export default {
  name: 'Logo',
  created() {},
  data() {
    return {};
  },
  props: {},
  methods: {},
};
</script>

<style lang="scss">
  @import '@/assets/styles/_style.scss';
  @font-face {
    font-family: 'Star Jedi Hol';
    src: url('../../assets/fonts/starjedi/Starjhol.ttf');
  }
  .app-logo {
    font-family: 'Star Jedi Hol';
    font-size: 30px;
    color: $main;
    text-align: center;
    @include textShadowHover;
  }
  .logo-wrapper {
    position: relative;

    a {
      @include extendedLink;
    }
  }
</style>
