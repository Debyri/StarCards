<template>
  <div class="home__intro">
    <h1 class="home__intro-header">star cards</h1>
    <p class="home__intro-subheader">finally out</p>
  </div>
</template>

<script>
export default {
  name: 'HomeIntro',
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
.home__intro {
  @include flexCenter;
  flex-direction: column;
  color: $main;
  &-header {
    @include starCardsHeader;
  }
  &-subheader {
    font-size: 20px;
    margin-top: 30px;
    text-transform: capitalize;
    font-family: 'Norwester';
  }
}
</style>
