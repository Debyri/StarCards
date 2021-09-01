<template>
  <div>
    <p>Stand By</p>
  </div>
</template>

<script>
export default {
  name: 'LoadingDiv',
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
    font-family: 'Star Jedi';
    src: url('/fonts/starjedi/Starjedi.ttf');
}
div {
  height: 100vh;
  background-image: url(../../assets/img/loading-bg.jpeg);
  @include flexCenter;
  @include bgPosition;
}
p {
  font-family: 'Star Jedi';
  color: $main;
  @media screen and (min-width: 400px) {
    font-size: 40px;
  }
}
</style>
