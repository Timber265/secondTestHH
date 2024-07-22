<script>
export default {
  name: "vCard"
}
</script>

<template>
  <div style="--bs-border-opacity: .5; width: 100%; height: 100%;"
       class="card__item p-2 border border-2 border-warning rounded-5 ">
    <div style="overflow: hidden" class="card__item-image rounded-5">
      <img style="width: 100%" src="/image/photo.png" alt="">
    </div>
    <div class="card__item-info">
      <h3 class="fs-6 text-black fw-bold">Без слов</h3>
      <div>
        <div class="d-flex align-items-start gap-2">
          <div style="max-width: 70px; width: 100%">
            <img style="width: 100%; object-fit: contain; display: block" class="" src="/image/smallPhoto.png" alt="">
          </div>
          <div style="height: 100%; display: flex;flex-direction: column;justify-content: space-between">
            <h2 class="fs-6 m-0">Настя Ивлеева Вячеславовна</h2>
            <p class="text-warning mb-0">проверенно <span> <img src="/icons/check.png" alt=""></span></p>
          </div>
        </div>

        <div class="d-flex align-items-center justify-content-between gap-1 mb-3">
          <h2 class="fs-6 m-0">Редкость:</h2>
          <p class="border border-warning border-3 py-1 px-3 rounded-3 text-black fw-regular m-0">уникальная</p>
        </div>
        <div class="d-flex align-items-center justify-content-between gap-1">
          <h2 class="fs-6">Цена:</h2>
          <p class="bg-warning rounded-3 py-1 px-4">от 500 ₽</p>
        </div>
        <div class="d-flex justify-content-center">
          <button style="width: 80%" class="border-0 bg-warning rounded-4 py-2 fw-bold">Купить</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>