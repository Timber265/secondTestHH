<script>
import VInput from "./UI/vInput.vue";

export default {
  name: "vHeader",
  components: {VInput}
}
</script>

<template>
  <div class="header">
    <div class="container">
      <div class="align-items-center d-flex gap-3 justify-content-between">
        <div class="d-flex align-items-center gap-3 flex-grow-1">
          <div class="header__logo">
            <img style="width: 100%" src="/image/headerLogo/лого.png" alt="">
          </div>
          <div class="header-search" style="max-width: 575px; width: 100%">
            <v-input/>
          </div>
        </div>
        <div class="header__avatar">
          <img src="/image/avatar.png" alt="">
        </div>
        <div class="burgermenu">
          <img src="/image/burger.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.burgermenu {
  display: none;
}

.header-search {
  position: relative;
}

.header__avatar {
  position: relative;
}

.header__avatar:before {
  content: url("/icons/tringle.svg");
  position: absolute;
  top: 50%;
  right: -30px;
  transform: translate(-50%, -50%);
}

@media (max-width: 580px) {
  .header-search {
    display: none;
  }

  .header__avatar {
    display: none;
  }

  .burgermenu {
    display: block;
  }
}
</style>