<template>
  <ul v-if="vehicles.length">
    <li v-for="(vehicles, index) in vehicles" :key="index" class="card">
      <div class="card__img-wrapper">
        <div class="card__img-power"></div>
      </div>
      <div class="card__info">
        <h2 class="card__info-name">{{ vehicles.name }}</h2>
        <div class="card__info-stats">
          <p>Weight: {{ vehicles.mass }}kg</p>
          <p>Height: {{ vehicles.height }}cm</p>
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
  name: 'VehicleCards',
  components: {
    LoadingDiv,
  },
  created() {},
  data() {
    return {
      vehicles: [],
    };
  },
  mounted() {
    this.fetchVehicles();
  },
  methods: {
    fetchVehicle() {
      axiosClient.get('vehicles')
        .then(({ data }) => {
          this.vehicles = data.results;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<style lang="scss" scoped></style>
