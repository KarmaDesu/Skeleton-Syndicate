<template>
  <swiper
    :slidesPerView="1"
    :navigation="true"
    :loop="true"
    :breakpoints="{
      '768': {
        slidesPerView: 2,
        spaceBetween: 10,
      },
      '1024': {
        slidesPerView: 5,
        spaceBetween: 10,
      },
    }"
    class="mySwiper"
  >
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/1.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/2.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/3.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/4.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/5.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/6.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/7.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/8.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/9.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/10.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/11.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/12.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/13.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/14.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/15.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/16.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/17.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/18.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/19.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/20.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/21.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/22.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/23.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/24.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/25.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/26.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/27.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/28.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/29.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/30.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/31.png" /></div
    ></swiper-slide>
    <swiper-slide
      ><div class="tw-flex tw-items-center tw-justify-center">
        <img src="../assets/32.png" /></div
    ></swiper-slide>
  </swiper>
</template>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
// import Swiper core and required modules
import SwiperCore, { Pagination, Navigation } from "swiper";
SwiperCore.use([Pagination, Navigation]);
</script>

<style scoped lang="scss"></style>
