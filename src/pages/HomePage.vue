<template>
  <div
    class="tw-flex tw-flex-col tw-justify-center tw-items-center md:tw-flex md:tw-grid-cols-2 xl:tw-grid xl:tw-grid-cols-2 tw-max-w-7xl tw-mx-auto xl:tw-relative tw-px-5 xl:tw-px-0 xl:tw-my-12"
  >
    <div class="tw-flex">
      <CountDown date="2021/11/26 13:46:00 UTC"></CountDown>
    </div>

    <div
      class=""
    >
      <img class="" src="../assets/eg1.png" alt="" />
    </div>
  </div>

  <div id="collection" class="tw-py-10 tw-text-center tw-my-10">
    <div class="heading-3 tw-text-3xl">
      <strong>COLLECTION</strong>
    </div>
  </div>
  <div class="tw-max-w-7xl tw-mx-auto tw-py-10 tw-px-5 xl:tw-px-0">
    <div class="tw-flex tw-justify-center tw-items-center">
      <SwiperCaro></SwiperCaro>
    </div>
  </div>

  <div id="about" class="tw-py-10 tw-text-center">
    <div class="heading-3 tw-text-3xl">
      <strong>ABOUT</strong>
    </div>
  </div>

  <div class="tw-max-w-7xl tw-mx-auto tw-pt-10 tw-px-5 xl:tw-px-0">
    <div class="about">
      <div class="tw-flex tw-flex-col tw-gap-2 tw-pt-3">
        <div class="tw-text-center tw-text-black tw-text-3xl">
          “Skeleton Syndicate“
        </div>
        <div
          class="tw-text-black tw-text-xl tw-py-3 tw-leading-relaxed tw-text-center"
        >
          Establish project treasury and offer staking in first week Introduce
          "Graveyard Service" and Additional Deadlist Perks Weekly
          Giveaways/Raffles of NFTs, ADA, and Whitelists Future Collaborations
          with reputable projects in the space Constantly underpromise and
          overdeliver for holders
        </div>
      </div>
    </div>
  </div>

  <div id="roadmap" class="tw-py-10 tw-text-center">
    <div class="heading-3 tw-text-3xl">
      <strong>ROADMAP</strong>
    </div>
  </div>
  <div class="tw-flex tw-justify-center">
    <div class="tw-max-w-7xl tw-mx-auto tw-pt-10 tw-px-5 xl:tw-px-0">
      <q-timeline :layout="layout" color="tw-gray-500">
        <q-timeline-entry class="tw-font-extrabold tw-text-lg">
          <template #title>
            <div class="tw-text-2xl tw-font-extrabold tw-text-left eggscolor">
              Phase - 1 | Skeleton Syndicate
            </div>
          </template>
          <div class="tw-font-medium tw-text-black tw-text-lg">
            <ul
              class="tw-list-disc tw-list-inside tw-text-xl tw-leading-relaxed tw-text-justify"
            >
              <li>Establish project treasury and offer staking in first week.</li>
              <li>Introduce "Graveyard Service" and Additional Deadlist Perks.</li>
              <li>Weekly Giveaways/Raffles of NFTs, ADA, and Whitelists.</li>
              <li>Future Collaborations with reputable projects in the space.</li>
              <li>Constantly underpromise and overdeliver for holders.</li>
            </ul>
          </div>
        </q-timeline-entry>

        <q-timeline-entry class="tw-font-extrabold tw-text-lg">
          <template #title>
            <div
              class="tw-text-black tw-text-2xl tw-font-extrabold tw-text-left eggscolor"
            >
              Phase 2 | The Fall Drop
            </div>
          </template>
          <div class="tw-font-medium tw-text-black tw-text-lg">
            <ul
              class="tw-list-disc tw-list-inside tw-text-xl tw-leading-relaxed tw-text-justify"
            >
              <li>Coming Soon</li>
            </ul>
          </div>
        </q-timeline-entry>

        <q-timeline-entry class="tw-font-extrabold tw-text-lg">
          <template #title>
            <div
              class="tw-text-black tw-text-2xl tw-font-extrabold tw-text-left eggscolor"
            >
              Phase - 3 | The Winter Drop
            </div>
          </template>
          <div class="tw-font-medium tw-text-black tw-text-lg">
            <ul
              class="tw-list-disc tw-list-inside tw-text-xl tw-leading-relaxed tw-text-justify"
            >
              <li>Coming Soon</li>
            </ul>
          </div>
        </q-timeline-entry>
        <q-timeline-entry class="tw-font-extrabold tw-text-lg">
          <template #title>
            <div
              class="tw-text-black tw-text-2xl tw-font-extrabold tw-text-left eggscolor"
            >
              Phase - 4 | The Spring Drop
            </div>
          </template>
          <div class="tw-font-medium tw-text-black tw-text-lg">
            <ul
              class="tw-list-disc tw-list-inside tw-text-xl tw-leading-relaxed tw-text-justify"
            >
              <li>Coming Soon</li>
            </ul>
          </div>
        </q-timeline-entry>

        <q-timeline-entry class="tw-font-extrabold tw-text-lg tw-text-black">
          <template #title>
            <div
              class="tw-text-black tw-text-2xl tw-font-extrabold tw-text-left eggscolor"
            >
              Phase - 5 | Launch
            </div>
          </template>
        </q-timeline-entry>
      </q-timeline>
    </div>
  </div>
</template>

<script setup>
import CountDown from "../components/CountDown.vue";
import SwiperCaro from "src/components/SwiperCaro.vue";
import { ref } from "vue";

const layout = ref("dense");
</script>

<style lang="scss" scoped></style>
