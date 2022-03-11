<template>
  <div id="app">
    <div class="promo">
      <div class="promo__left">

        <Burger />

        <div class="promo__menu">
          <ul>
            <li class="promo__menu-item">Подсказки</li>
            <li class="promo__menu-item">Подсказки</li>
            <li class="promo__menu-item promo__menu-item--active">Подсказки</li>
            <li class="promo__menu-item">Подсказки</li>
          </ul>
        </div>
        <div class="promo__scroll">Скрольте вниз</div>
      </div>

      <Logo />

      <div class="promo__sidelink">
        <a href="#">hd.kinopoisk.ru</a>
      </div>

      <h1 class="promo__title">ОНИ ДОЛЖНЫ ЧТО-ТО ЗНАТЬ</h1>

      <div class="promo__slider">
        <div class="swiper">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <p class="swiper-text">
                Для примера мы показали вам его лицо. В первой серии он прячется
                в подвале<br />
                за мониторами, и пусть борода не собьёт вас с толку. Найдите
                героя и нажмите на паузу —<br />
                ему не терпится отдать вам промокод.
              </p>
            </div>
            <div class="swiper-slide">
              <p class="swiper-text">
                Для примера мы показали вам его лицо. В первой серии он прячется
                в подвале<br />
                за мониторами, и пусть борода не собьёт вас с толку. Найдите
                героя и нажмите на паузу —<br />
                ему не терпится отдать вам промокод.
              </p>
            </div>
            <div class="swiper-slide">
              <p class="swiper-text">
                Для примера мы показали вам его лицо. В первой серии он прячется
                в подвале<br />
                за мониторами, и пусть борода не собьёт вас с толку. Найдите
                героя и нажмите на паузу —<br />
                ему не терпится отдать вам промокод.
              </p>
            </div>
          </div>
          <div class="swiper-pagination"></div>

          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>
        </div>
      </div>

      <a href="#" class="promo__btn">Искать промокод</a>

      <div class="promo__backgrounds"></div>
      
    </div>
  </div>
</template>

<script>
import Logo from "@/components/Logo.vue";
import Burger from "@/components/Burger.vue";
import Swiper, { Navigation, Pagination } from "swiper";
import "swiper/swiper.scss";
import "swiper/modules/navigation/navigation.scss";
import "swiper/modules/pagination/pagination.scss";

export default {
  name: "App",
  components: {
    Logo,
    Burger,
  },
  mounted: function () {
    const mySwiper = new Swiper(".swiper", {
      modules: [Navigation, Pagination],
      autoplay: false,
      loop: false,
      draggable: true,

      pagination: {
        el: ".swiper-pagination",
        type: "fraction",
      },

      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev",
      },

      scrollbar: {
        el: ".swiper-scrollbar",
      },
    });
    console.log(mySwiper + 'init');
  },
};
</script>

<style lang="scss">
@import "@/assets/scss/app";
</style>
