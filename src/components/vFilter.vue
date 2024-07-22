<script>
import VInput from "./UI/vInput.vue";

export default {
  name: "vFilter",
  components: {VInput},
  data() {
    return {
      viewFilter: {
        openViewFilter: false,
        cost: true,
        category: true,
        typeFile: true,
        typeSale: true,
        nft: true,
        rarely: true
      }
    }
  },
  methods: {
    buttonOpenViewFilter() {
      this.viewFilter.openViewFilter = !this.viewFilter.openViewFilter
    },
    buttonChangeCostStatus() {
      this.viewFilter.cost = !this.viewFilter.cost;
    },
    buttonChangeCategoryStatus() {
      this.viewFilter.category = !this.viewFilter.category;
    },
    buttonChangeTypeStatus() {
      this.viewFilter.typeFile = !this.viewFilter.typeFile;
    },
    buttonChangeSaleStatus() {
      this.viewFilter.typeSale = !this.viewFilter.typeSale;
    },
    buttonChangeNftStatus() {
      this.viewFilter.nft = !this.viewFilter.nft;
    },
    buttonChangeRarelyStatus() {
      this.viewFilter.rarely = !this.viewFilter.rarely;
    },
  }
}
</script>

<template>
  <div class="mb-4">
    <div class="container">
      <div class="searcher-min mb-3" style="width: 100%">
        <v-input/>
      </div>
      <div class="d-flex gap-4 align-items-center justify-content-between mb-2">
        <div class="" style="max-width: 216px; width: 100%">
          <button @click="buttonOpenViewFilter" style="width: 100%!important;" class="filter__button w-auto px-2 py-1 rounded bg-body border-1 text-start fw-medium">
            Фильтры
          </button>
        </div>
        <div class="searcher" style="width: 100%">
          <v-input/>
        </div>
        <div style="max-width: 235px; width: 100%">
          <select class="rounded p-1" style="width: 100%">
            <option>По умолчанию</option>
            <option>По Дате</option>
            <option>Дешевле</option>
            <option>Дороже</option>
            <option>ПО популярности</option>
          </select>
        </div>
      </div>

      <div class="model" :class="{'hidden': !viewFilter.openViewFilter}" style="position: absolute; z-index: 5; overflow: hidden;">
        <div style="width: 100%"
             class="filter bg-white border border-black border-1 rounded-2 py-3 px-3">
          <div class="filter__wrapper">
            <div style="position: relative; z-index: 100" class="filter__cost overflow-hidden bg-white mb-4">
              <div @click="buttonChangeCostStatus" style="cursor: pointer; position: relative; z-index: 100;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Цена</h3>
                <button class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div style="position: relative; z-index: 10"
                   :class="{'change-view': true, 'hidden': !viewFilter.cost}"
                   class="change-cost bg-white">
                <div style="position: relative; height: 20px" class="d-flex">
                  <span class="triangle-right"></span>
                  <span class="line-between"></span>
                  <span class="triangle-left"></span>
                </div>
                <div class="d-flex align-items-center">
                  <div style="--bs-border-opacity: .6" class="border-bottom border-black border-2"><input
                      style="width: 100%" class="filter-input border-0 mb-2 fw-bold" type="number" placeholder="500 ₽">
                  </div>
                  <div class="border-counter" style="width: 50%;"></div>
                  <div style="--bs-border-opacity: .6" class="border-bottom border-black border-2"><input
                      style="width: 100%" class="filter-input border-0 mb-2 fw-bold" type="number"
                      placeholder="1000000 ₽"></div>
                </div>
              </div>
            </div>

            <div class="filter__category overflow-hidden">
              <div @click="buttonChangeCategoryStatus" style="cursor: pointer; position: relative; z-index: 5;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Категории</h3>
                <button
                    class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div class="mb-4"
                   :class="{'change-view': true, 'hidden': !viewFilter.category}">
                <ul class="m-0 p-0">
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="premium">
                    <label for="premium">Премиум</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">Искусство</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="celebrity">
                    <label for="celebrity">Знаменитости</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="cyberSport">
                    <label for="cyberSport">Киберспорт</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="charity">
                    <label for="charity">Благотворительность</label>
                  </li>
                </ul>
              </div>
            </div>

            <div class="filter__type overflow-hidden">
              <div @click="buttonChangeTypeStatus" style="cursor: pointer; position: relative; z-index: 5;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Типы файлов</h3>
                <button
                    class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div class="mb-4" :class="{'change-view': true, 'hidden': !viewFilter.typeFile}">
                <ul class="m-0 p-0">
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="premium">
                    <label for="premium">Изображения</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">Видео</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="celebrity">
                    <label for="celebrity">Аудио</label>
                  </li>
                </ul>
              </div>
            </div>

            <div class="filter__type overflow-hidden">
              <div @click="buttonChangeSaleStatus" style="cursor: pointer; position: relative; z-index: 5;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Типы продаж</h3>
                <button
                    class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div class="mb-4" :class="{'change-view': true, 'hidden': !viewFilter.typeSale}">
                <ul class="m-0 p-0">
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="premium">
                    <label for="premium">Фикс. цена</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">Аукцион активен</label>
                  </li>
                </ul>
              </div>
            </div>

            <div class="filter__type overflow-hidden">
              <div @click="buttonChangeNftStatus" style="cursor: pointer; position: relative; z-index: 5;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Сеть NFT</h3>
                <button
                    class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div class="mb-4" :class="{'change-view': true, 'hidden': !viewFilter.nft}">
                <ul class="m-0 p-0">
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="premium">
                    <label for="premium">ETH</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">BNB</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">USDC</label>
                  </li>
                </ul>
              </div>
            </div>

            <div class="filter__type overflow-hidden">
              <div @click="buttonChangeRarelyStatus" style="cursor: pointer; position: relative; z-index: 5;"
                   class="d-flex align-items-center justify-content-between bg-white z-4">
                <h3>Редкость</h3>
                <button
                    class="bg-transparent border-0 d-flex align-items-center"><span
                    class="btn-span"></span></button>
              </div>
              <div class="mb-4" :class="{'change-view': true, 'hidden': !viewFilter.rarely}">
                <ul class="m-0 p-0">
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="premium">
                    <label for="premium">Уникальная</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">Редкая</label>
                  </li>
                  <li class="d-flex align-items-center gap-2">
                    <input type="checkbox" id="art">
                    <label for="art">Эпическая</label>
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.model {max-width: 365px; transition: .5s}
.model.hidden {max-width: 0; opacity: 0}
.filter__button {
  position: relative;
}

.filter__button:before {
  content: url("/icons/tringle.svg");
  position: absolute;
  right: 20px;
  top: 50%;
  transform: translateY(-50%);
}

.btn-span {
  position: relative;
}

.btn-span::before {
  content: "";
  position: absolute;
  width: 20px;
  right: 0;
  height: 3px;
  background-color: gold;
}

.filter-input {
  outline: none;
}

.border-counter {
  position: relative;
}

.border-counter::before {
  content: "";
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translateX(-50%);
  background-color: gray;
  width: 40%;
  height: 2px;
}

.line-between {
  content: "";
  position: absolute;
  width: 100%;
  top: 50%;
  right: 0;
  height: 1px;
  background-color: gray;
}

.triangle-left, .triangle-right, .line-between {
  position: relative;
}

.triangle-right::before {
  content: "";
  position: absolute;
  width: 20px;
  height: 20px;
  border: 10px solid transparent; /* Прозрачные границы */
  border-left: 15px solid gold; /* Добавляем треугольник */
  z-index: 1;
}

.triangle-left::before {
  content: "";
  position: absolute;
  width: 20px;
  height: 20px;
  right: 0;
  border: 10px solid transparent; /* Прозрачные границы */
  border-right: 15px solid gold; /* Добавляем треугольник */
  z-index: 1;
}

.change-view {
  position: relative;
  transition: .2s;
}

.change-view.hidden {
  transform: translateY(-100%);
}
.searcher-min {
  display: none;
}

@media (max-width: 580px) {
  .searcher {
    display: none;
  }
  .searcher-min {
    display: block;
  }
}
</style>