<template>
  <div class="intro__wrapper">
    <div class="intro__header-wrapper">
      <h2 class="intro__header">
        star cards
      </h2>
      <p class="intro__subheader">Exited to meet first of our SW Characters?</p>
    </div>
    <section class="intro__body">
      <div class="intro__body-paragraph">
        <span class="intro__body-headings">Learn The Rules:</span>
        <p class="intro__body-lore">Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Ipsam nam dolor quae assumenda, quaerat rerum nemo
          nostrum est dolores magni incidunt asperiores ut
          distinctio eaque tempora labore error rem quisquam vero
          laborum natus consequuntur perferendis sunt debitis?
          Voluptas dolorum,
          quos sed quidem numquam iusto, animi tenetur reiciendis voluptatem ex perspiciatis!
        </p>
      </div>
      <div class="intro__body-paragraph">
        <span class="intro__body-headings">Get to know the Characters:</span>
        <div class="people-cards__slider">
          <PeopleCardsSlider />
        </div>
      </div>
      <div class="intro__body-paragraph">
        <span class="intro__body-headings">Rare Cards:</span>
        <p class="intro__body-lore">Lorem ipsum dolor sit amet consectetur adipisicing elit.
          Ipsam nam dolor quae assumenda
        </p>
      </div>
    </section>
  </div>
</template>

<script>

import PeopleCardsSlider from '@/components/sections/PeopleCardsSlider.vue';

export default {
  name: 'AboutIntro',
  components: {
    PeopleCardsSlider,
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
.intro {
  &__wrapper {
    padding: 50px;
  }
  &__header {
    @include starCardsHeader;
    &-wrapper {
      @include flexCenter;
      flex-direction: column;
    }
  }
  &__subheader {
    @include introSubheader;
    color: $main;
  }
}
.intro__body {
  &-paragraph {
    margin-top: 30px;
    color: #ffffff;
  }
  &-headings {
    @include norwesterFont;
    color: $main;
  }
  &-lore {
    margin-top: 15px;
  }
}
</style>
