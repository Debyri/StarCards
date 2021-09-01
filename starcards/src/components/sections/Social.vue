<template>
  <ul class="social-list">
    <li class="social-list__item">
      <a href="https://www.instagram.com/debyri/" target="blank" class="item-link">
        <font-awesome-icon :icon='["fab", "instagram"]' class="social-list__item-icon" />
      </a>
    </li>
    <li class="social-list__item">
      <a href="https://web.telegram.org" target="blank" class="item-link">
        <font-awesome-icon :icon='["fab", "telegram-plane"]' class="social-list__item-icon" />
      </a>
    </li>
    <li class="social-list__item">
      <a href="https://www.facebook.com/profile.php?id=100001816260202" target="blank" class="item-link">
        <font-awesome-icon :icon='["fab", "facebook-f"]' class="social-list__item-icon" />
      </a>
    </li>
    <li class="social-list__item">
      <a href="https://www.linkedin.com/in/yurii-rohachevskyi-448534115/" target="blank" class="item-link">
        <font-awesome-icon :icon='["fab", "linkedin-in"]' class="social-list__item-icon" />
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Social',
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
.social-list {
  display: flex;
  list-style: none;

  &__item {
    margin: 5px;
    padding: 10px;
    font-size: 1.5em;
    position: relative;
    color: red;
  }
}
.item-link:hover  .social-list__item-icon{
  color: $main;
}
</style>
