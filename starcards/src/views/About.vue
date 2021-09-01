<template>
  <div class="about">
    <AboutIntro />
  </div>
</template>

<script>
// @ is an alias to /src
import AboutIntro from '@/components/sections/AboutIntro.vue';

export default {
  name: 'About',
  components: {
    AboutIntro,
  },
};
</script>

<style lang="scss" scoped>
  // @import '@/assets/_style.scss';
</style>
