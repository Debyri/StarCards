<template>
  <div class="home">
  <HomeIntro />
  <PeopleCards class="cards" />
  <!-- <VehicleCards /> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import axiosClient from '@/plugins/axiosClient';
import PeopleCards from '@/components/sections/PeopleCards.vue';
import HomeIntro from '@/components/sections/HomeIntro.vue';
// import VehicleCards from '@/components/sections/VehicleCards.vue';

export default {
  name: 'Home',
  components: {
    PeopleCards,
    HomeIntro,
    // VehicleCards,
  },
  data() {
    return {
    };
  },
  mounted() {
  },
  methods: {
  },
};
</script>

<style lang="scss" scoped>
.home {
  padding: 50px 30px 50px;
}
.cards {
  margin-top: 30px;
}
</style>
