<template>
  <div class="bgcolor">
    <div
      class="tw-flex tw-flex-col tw-justify-center tw-items-center lg:tw-flex-row lg:tw-justify-between tw-max-w-7xl tw-mx-auto tw-px-5 xl:tw-px-0 tw-py-3"
    >


      <div>
        <img class="logo" src="../assets/logo.png" alt="">
      </div>

      <div class="tw-space-x-4 tw-my-3 lg:tw-space-x-6 tw-items-center tw-flex">
        <router-link
          class="tw-text-xl md:tw-text-2xl eggscolor hover:tw-scale-125 tw-transition-all tw-font-extrabold"
          :to="{name:'Home',hash:'#collection'}"
          >Collection</router-link
        >
        <router-link
          class="tw-text-xl md:tw-text-2xl eggscolor hover:tw-scale-125 tw-transition-all tw-font-extrabold"
          :to="{name:'Home',hash:'#roadmap'}"
          >Roadmap</router-link
        >
        <router-link
          class="tw-text-xl md:tw-text-2xl eggscolor hover:tw-scale-125 tw-transition-all tw-font-extrabold"
          :to="{name:'Home',hash:'#about'}"
          >About</router-link
        >
      </div>
      <div class="tw-space-x-4 tw-my-3 lg:tw-space-x-6 tw-items-center tw-flex tw-z-10">
        <a
          class="tw-text-xl md:tw-text-2xl eggscolor hover:tw-scale-125 tw-transition-all tw-font-extrabold"
          href="https://twitter.com/SkellySyndicate"
          target="_blank"
        >
          <i class="fa-brands fa-twitter"></i>
        </a>
        <a
          class="tw-text-xl md:tw-text-2xl eggscolor hover:tw-scale-125 tw-transition-all tw-font-extrabold"
          href="https://discord.gg/GHK6tUKy"
          target="_blank"
        >
          <i class="fa-brands fa-discord"></i>
        </a>
      </div>
    </div>


    <router-view></router-view>

    <div class="tw-py-10 tw-text-center">
      <div
        class="tw-text-xs md:tw-text-2xl tw-text-black hover:tw-cursor-pointer"
        @click="openTerms = true"
      >
        Terms & Conditions
      </div>
    </div>

    <q-dialog v-model="openTerms" persistent>
      <q-card style="width: 1200px; max-width: 100vw">
        <q-card-section>
          <div class="text-h6 text-center">
            <span>TERMS & CONDITIONS</span>
            <q-btn
              round
              flat
              dense
              icon="close"
              class="float-right"
              color="grey-8"
              v-close-popup
              @click="closeTerms()"
            ></q-btn>
          </div>
        </q-card-section>
        <q-separator inset></q-separator>
        <div
          class="tw-flex tw-justify-center tw-text-base tw-flex-wrap tw-mt-2 tw-px-6 tw-break-normal tw-text-center tw-text-bold"
        >
          <div class="w-1/2 tw-py-3">
            Skeleton Syndicate is a collection of generative artworks (NFTs)
            sun bathing on the Cardano Blockchain. This website is only an
            interface allowing participants to exchange digital collectibles.
            Users are entirely responsible for the safety and management of
            their own private Cardano wallets and validating all transactions
            generated by this website before approval. This website and its
            connected services are provided ???as is??? and ???as available??? without
            warranty of any kind. By using this website you are accepting sole
            responsibility for any and all transactions involving Skeleton Syndicate digital collectibles
          </div>
        </div>
      </q-card>
    </q-dialog>
  </div>
</template>

<script setup>

import { ref } from "vue";

const openTerms = ref(false);
function closeTerms() {
  openTerms.value = false;
}


</script>

<style>
.q-dialog__backdrop {
  backdrop-filter: blur(7px);
}


.logo{
  height: 7rem;
}
</style>
