<script>
export default {
  name: "vFooter"
}
</script>

<template>
  <div class="footer bg-warning bg-opacity-75 pb-5">
    <div class="container">
      <div class="footer__content d-flex gap-2 justify-content-between pt-5">
        <div class="first-item">
          <div class="mb-2"><img src="/image/footerlogo.png" alt=""></div>
          <ul class="d-flex flex-column gap-2 mb-4">
            <li class="fs-5 text-black">Россия, г. Москва, 119002</li>
            <li class="fs-5 text-black">ул. Арбат 51/1/8А</li>
            <li class="fs-5 text-black">e-mail: info@lionmax.ru</li>
          </ul>
          <div class="">
            <ul class="d-flex gap-3">
              <li><img src="/image/twitter-3%201.png" alt=""></li>
              <li><img src="/image/vk.png" alt=""></li>
            </ul>
          </div>
        </div>
        <div style=" gap: 80px" class="second-item d-flex">
          <div>
            <h5 class="title fw-bold text-black mb-3">NFT</h5>
            <ul class="d-flex flex-column gap-2">
              <li><a href="#">Что такое NFT</a></li>
              <li><a href="#">Создайте NFT
                с нами</a>
              </li>
            </ul>
          </div>
          <div>
            <h5 class="title fw-bold text-black mb-3">Компания</h5>
            <ul class="d-flex flex-column gap-2">
              <li><a href="#">О нас</a></li>
              <li><a href="#">Отправить запрос</a></li>
            </ul>
          </div>

          <div>
            <h5 class="title fw-bold text-black mb-3">Другое</h5>
            <ul class="d-flex flex-column gap-2">
              <li><a href="#">Условия использования</a></li>
              <li><a href="#">Политика конфиденциальности</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="star-logo text-center">
        <img src="/image/star.png" alt="">
      </div>
    </div>
  </div>
</template>

<style scoped>

.footer {
  position: relative;
}

.footer:before {
  content: "";
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 50%;
  border-radius: 20%;
  transform: translate(-50%, -50%);
  background-color: #FDD446;
  filter: blur(300px);
  z-index: -1;
}

ul {
  padding: 0;
  margin: 0;
}

li {
  color: black;
  font-weight: 500;
}

.star-logo {
  position: relative;
}

.star-logo::before {
  content: "";
  position: absolute;
  width: 100%;
  height: 2px;
  top: 37%;
  left: 0;
  background-color: black;
}

.star-logo::after {
  content: "@ tnft.ru Company, Inc";
  position: absolute;
  bottom: 35px;
  right: 0;
}

a {
  color: inherit;
  text-decoration: none;
}

@media (max-width: 1000px) {
  .first-item {
    display: none;
  }
  .star-logo::after {
    left: 0;
    top: 100%;
  }
}@media (max-width: 580px) {
  .second-item {
    gap: 5px !important;
    flex-direction: column;
  }
  .title {
    display: none;
  }
  .star-logo::after {
    display: none;
  }
  .star-logo::before {
    display: none;
  }
  .star-logo {
    display: none;
  }
}
</style>