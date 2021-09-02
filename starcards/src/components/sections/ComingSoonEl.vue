<template>
<div class="wrapper">
  <div class="glitch">
    <span class="absolute">stay tuned</span>
    <span>stay tuned</span>
    <span class="absolute">stay tuned</span>
  </div>
</div>
</template>

<script>
export default {
  name: 'ComingSoonEl',
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
.wrapper {
  height: 90vh;
  color: white;
  position: relative;
  @include flexCenter;
}
.glitch {
  position: relative;
  font-size: 6rem;
  @include starJediFont;
  text-shadow:
    0.05em 0 0 rgba(255, 0, 0, 0.75),
    -0.025em -0.05em 0 rgba(0, 255, 0, 0.75),
    0.025em 0.05em 0 rgba(0, 0, 255, 0.75);
  animation: glitch 500ms infinite;

  @media screen and (max-width: 400px) {
      font-size: 2rem;
  }
}

.absolute {
  position: absolute;
  top: 0px;
  left: 0;
}
.absolute:first-of-type {
  animation: glitch 650ms infinite;
  clip-path: polygon(0 0, 100% 0, 100% 50%, 0 50%);
  transform: translate(-0.05em, -0.025em);
}
.absolute:last-of-type {
  animation: glitch 375ms infinite;
  clip-path: polygon(0 60%, 100% 60%, 100% 100%, 0 100%);
  transform: translate(0.05em, 0.015em);
  opacity: 0.8;
}

@keyframes glitch {
  0% {
    text-shadow:
    0.05em 0 0 rgba(255, 0, 0, 0.75),
    -0.025em -0.05em 0 rgba(0, 255, 0, 0.75),
    0.025em 0.05em 0 rgba(0, 0, 255, 0.75);
  }
  14% {
    text-shadow:
    0.05em 0 0 rgba(255, 0, 0, 0.75),
    -0.025em -0.05em 0 rgba(0, 255, 0, 0.75),
    0.025em 0.05em 0 rgba(0, 0, 255, 0.75);
  }
  15% {
    text-shadow:
    -0.05em -0.025em 0 rgba(255, 0, 0, 0.75),
    0.025em 0.025em 0 rgba(0, 255, 0, 0.75),
    -0.05em -0.05em 0 rgba(0, 0, 255, 0.75);
  }
  49% {
    text-shadow:
    -0.05em -0.025em 0 rgba(255, 0, 0, 0.75),
    0.025em 0.025em 0 rgba(0, 255, 0, 0.75),
    -0.05em -0.05em 0 rgba(0, 0, 255, 0.75);
  }
  50% {
    text-shadow:
    0.025em 0.05em 0 rgba(255, 0, 0, 0.75),
    0.05em 0 0 rgba(0, 255, 0, 0.75),
    0 -0.05em 0 rgba(0, 0, 255, 0.75);
  }
  99% {
    text-shadow:
    0.025em 0.05em 0 rgba(255, 0, 0, 0.75),
    0.05em 0 0 rgba(0, 255, 0, 0.75),
    0 -0.05em 0 rgba(0, 0, 255, 0.75);
  }
  100% {
    text-shadow:
    -0.025em 0 0 rgba(255, 0, 0, 0.75),
    -0.025em -0.025em 0 rgba(0, 255, 0, 0.75),
    -0.025em -0.05em 0 rgba(0, 0, 255, 0.75);
  }
}
</style>
