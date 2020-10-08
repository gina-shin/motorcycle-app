<template>
  <v-card
    class="bike-card"
  >
    <h1>{{ bike.model }}</h1>
    <img :src="getModelImage(bike.model)" :alt="bike.model" />
    <div
      class="bike-stats"
    >
      <h3>Color: {{bike.color}}</h3>
      <h3>Year: {{bike.year}}</h3>
      <h3>Power: {{bike.power}}</h3>
      <h3>Displacement: {{bike.displacement}}</h3>
    </div>
    <div
      class="bike-description"
    >
      <h2>Description</h2>
      {{ bike.description }}
    </div>
  </v-card>
</template>

<script>
export default {
  props: {
    bike: {
      type: Object,
      required: true,
    },
  },
  
  methods: {
    getModelImage(model) {
      return require(`@/assets/${model}.png`)
    }
  },
}
</script>

<style lang="scss">
  .bike-card {
    margin: 0 1em;
    padding: 1em;
  }

  .bike-description {
    margin: 1em 0;  
  }
</style>