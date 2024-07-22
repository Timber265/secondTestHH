<script>
import VHeader from "./components/vHeader.vue";
import VFilter from "./components/vFilter.vue";
import VOutputCard from "./components/vOutputCard.vue";
import VFooter from "./components/vFooter.vue";
export default {
  name: "App",
  components: {VFooter, VOutputCard,  VFilter, VHeader},
}
</script>

<template>
  <v-header />
  <v-filter />
  <v-output-card />
  <v-footer />
</template>

<style scoped>

</style>
