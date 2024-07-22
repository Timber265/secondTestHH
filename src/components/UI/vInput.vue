<script>
export default {
  name: "vInput"
}
</script>

<template>
  <div class="vInput">
    <input style="width: 100%" class="py-2 px-5 border border-2 rounded-5 d-flex align-items-center fs-6"
           placeholder="Поиск..."/>
  </div>
</template>

<style scoped>
.vInput {
  position: relative;
}
.vInput:before {
  content: url("/icons/search.svg");
  display: block;
  position: absolute;
  transform: translate(0, -50%);
  top: 50%;
  left: 15px;
  z-index: 1;
}
</style>