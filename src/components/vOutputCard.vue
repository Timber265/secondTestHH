<script>

import VCard from "./vCard.vue";

export default {
  name: "vOutputCard",
  components: {VCard}
}
</script>

<template>
  <div class="container mb-5">
    <div class="card__wrapper">
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
      <v-card/>
    </div>
  </div>
</template>

<style scoped>
.card__wrapper {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 56px;
}

@media (max-width: 1200px) {
  .card__wrapper {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 990px) {
  .card__wrapper {
    grid-template-columns: repeat(2, 1fr);
  }
}

  @media (max-width: 580px) {
    .card__wrapper {
      grid-template-columns: repeat(1, 1fr);
    }
  }
</style>