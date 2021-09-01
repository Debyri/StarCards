<template>
  <ul v-if="people.length">
    <li v-for="(people, index) in people" :key="index" class="card">
      <div class="card__img-wrapper">
        <div class="card__img-power"></div>
      </div>
      <div class="card__info">
        <h2 class="card__info-name">{{ people.name }}</h2>
        <div class="card__info-stats">
          <p>Weight: {{ people.mass }}kg</p>
          <p>Height: {{ people.height }}cm</p>
        </div>
        <h3 class="logo">SC</h3>
      </div>
    </li>
  </ul>
  <LoadingDiv v-else />
</template>

<script>

import axiosClient from '@/plugins/axiosClient';
import LoadingDiv from '@/components/sections/LoadingDiv.vue';

export default {
  name: 'PeopleCards',
  components: {
    LoadingDiv,
  },
  created() {},
  data() {
    return {
      people: [],
    };
  },
  mounted() {
    this.fetchPeople();
  },
  methods: {
    fetchPeople() {
      axiosClient.get('people')
        .then(({ data }) => {
          this.people = data.results;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<style lang="scss" scoped>
  @import '@/assets/styles/_card-styles.scss';
</style>
