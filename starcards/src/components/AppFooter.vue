<template>
  <div class="app-footer">
    <Logo />
    <span class="app-footer__copyright">&copy; Star Cards LLC 2021</span>
    <Social />
  </div>
</template>

<script>
import Logo from '@/components/sections/Logo.vue';
import Social from '@/components/sections/Social.vue';

export default {
  name: 'AppFooter',
  components: {
    Logo,
    Social,
  },
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
.app-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 60px;
  background-color: gray;
  background-image: url('../assets/img/footer-bg.jpeg');
  background-position: center;
  background-size: cover;
  &__copyright {
    color: $footer-text-color;
  }
  .app-logo {
    color: $footer-text-color;
    &:hover {
      color: $main;
    }
  }
}
@media screen and (max-width: 400px) {
  .app-footer {
    flex-direction: column;
  }
}
</style>
