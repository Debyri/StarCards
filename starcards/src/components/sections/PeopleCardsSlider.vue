<template>
  <vueper-slides v-if="people.length" :visible-slides="3">
    <vueper-slide v-for="(people, i) in people"
     :key="i" :title="people.name" :content="people.content"
      class="card" style="color: white"
      />
  </vueper-slides>
  <LoadingDiv v-else />
</template>

<script>

import { VueperSlides, VueperSlide } from 'vueperslides';
import 'vueperslides/dist/vueperslides.css';
import axiosClient from '@/plugins/axiosClient';
import LoadingDiv from '@/components/sections/LoadingDiv.vue';

export default {
  name: 'PeopleCards',
  components: {
    LoadingDiv,
    VueperSlides,
    VueperSlide,
  },
  created() {},
  data() {
    return {
      people: [
        {
          content: 'Aloha',
        },
      ],
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
  // @import '@/assets/styles/_card-styles.scss';
</style>
