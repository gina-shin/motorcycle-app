<template>
  <v-app>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
  export default {
    name: 'App',

    components: {
    },
  }
</script>

<style lang="scss">
  @import './styles/colors.scss';
  @import './styles/typography.scss';

  #app {
    font-family: 'Merriweather', serif;
    font-size: 16px;
    color: var(--black);
  }

</style>
