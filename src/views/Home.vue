<template>
  <div
    class="home"
  >
    <v-card
      class="bike-list"
    >
      <v-list
        width="200"
        rounded
      >
        <v-list-item
          v-for="(bike, index) in bikes"
          :key="index"
          @click="selectedBike = bike"
        >
          {{ bike.model }}
        </v-list-item>
      </v-list>
    </v-card>
    <BikeCard
      :bike="selectedBike"
    />
  </div>
</template>

<script>
  import BikeCard from '../components/BikeCard'

  export default {
    components: {
      BikeCard
    },

    data() {
      return {
        bikes: this.$store.state.bikes,
        selectedBike: null,
      }
    }
  }
</script>

<style lang="scss">
  .home {
    display: flex;

    padding: 10em;
    margin: auto;
    height: 100%;
  }
</style>