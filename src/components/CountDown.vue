<template>
  <div
    class="
      tw-bg-opacity-60
      tw-bg-[#82909a]
      tw-w-full
      tw-rounded-lg
      tw-px-10
      tw-mt-4
      tw-py-3
      tw-flex
      tw-flex-col
    "
    style="align-items: center; justify-content: center"
  >
    <div
      class="
        tw-text-center tw-text-2xl
        md:tw-text-4xl
        tw-my-1 tw-font-extrabold tw-text-[#16445c]
      "
    >
      Public Mint
    </div>
    <!-- <div
      class="
        tw-grid tw-z-40 tw-grid-cols-2
        sm:tw-grid-cols-4
        tw-bg-white tw-rounded-lg tw-py-1
        lg:tw-py-4
        tw-px-6
        lg:tw-mt-10
        tw-justify-center
        sm:tw-divide-x-2
        tw-divide-[#270302]
      "
    >
      <div
        class="
          tw-text-center
          tw-flex
          tw-flex-col
          tw-justify-center
          tw-px-4
         tw-text-[#5B8ED3]
        "
      >
        <p class="tw-text-base md:tw-text-3xl tw-font-extrabold">
          {{ control(days) }}
        </p>
        <small class="tw-text-xs tw-font-extrabold">Days</small>
      </div>
      <div
        class="
          tw-text-center
          tw-flex
          tw-flex-col
          tw-justify-center
          tw-px-4
          tw-text-[#5B8ED3]
        "
      >
        <p class="tw-text-base md:tw-text-3xl tw-font-extrabold">
          {{ control(hours) }}
        </p>
        <small class="tw-text-xs tw-font-extrabold">Hours</small>
      </div>
      <div
        class="
          tw-text-center
          tw-flex
          tw-flex-col
          tw-justify-center
          tw-px-4
          tw-text-[#5B8ED3]
        "
      >
        <p class="tw-text-base md:tw-text-3xl tw-font-extrabold">
          {{ control(minutes) }}
        </p>
        <small class="tw-text-xs tw-font-extrabold">Minutes</small>
      </div>
      <div
        class="
          tw-text-center
          tw-flex
          tw-flex-col
          tw-justify-center
          tw-px-4
          tw-text-[#5B8ED3]
        "
      >
        <p class="tw-text-base md:tw-text-3xl tw-font-extrabold">
          {{ control(seconds) }}
        </p>
        <small class="tw-text-xs tw-font-extrabold">Seconds</small>
      </div>
    </div> -->
     <div class="tw-bg-white  tw-text-[#16445c] tw-font-extrabold tw-rounded-lg tw-flex tw-items-center tw-py-1 lg:tw-py-4 tw-px-6 lg:tw-mt-10 tw-justify-center">
      <div class="md:tw-px-10 lg:tw-py-0 tw-py-2 tw-text-base">1ST January 2023</div>
    </div>
    <div class="tw-flex tw-justify-center tw-my-4 tw-items-center lg:tw-mt-10 ">
      <a
        href="https://discord.gg/GHK6tUKy"
        class="
          tw-rounded-full
          tw-text-base
          tw-px-8
          tw-py-2
          tw-bg-[#16445c]
          tw-text-white
          tw-font-medium
          hover:tw-bg-white hover:tw-text-[#16445c]
        "
        >MINT ON DISCORD</a
      >
    </div>
  </div>

  <q-dialog v-model="openMintModal" persistent>
    <q-card style="width: 500px; max-width: 80vw">
      <q-card-section>
        <div class="text-h6 text-center">
          <span>Mint Summer Eggs Beach Club</span>
          <q-btn
            round
            flat
            dense
            icon="close"
            class="float-right"
            color="grey-8"
            v-close-popup
            @click="cancelMint()"
          ></q-btn>
        </div>
      </q-card-section>
      <q-separator inset></q-separator>
      <q-card-section class="q-pt-none">
        <q-form class="q-gutter-md">
          <q-list>
            <q-item>
              <q-item-section>
                <div
                  class="
                    tw-flex tw-flex-col
                    sm:tw-flex-row
                    tw-gap-3
                    md:tw-gap-8
                    tw-justify-center tw-items-center tw-my-8 tw-text-lg
                    md:tw-text-4xl
                  "
                >
                  <q-select
                    filled
                    v-model="selected"
                    label="Select"
                    :options="options"
                    style="width: 250px"
                    behavior="menu"
                  />
                </div>
                <div
                  class="
                    tw-flex tw-justify-center tw-my-3 tw-text-base
                    md:tw-text-4xl
                  "
                >
                  You will be purchasing {{ selected }}
                </div>
              </q-item-section>
            </q-item>
          </q-list>
        </q-form>
      </q-card-section>
      <q-card-actions align="center">
        <q-btn label="Mint" @click="openPaymentWindow()" color="blue" />
      </q-card-actions>
    </q-card>
  </q-dialog>
</template>

<script setup>
import { ref, computed, defineProps, onMounted, watch } from "vue";
const openmintbutton = ref(false);
const time = ref(900);
const timer = ref(null);
const selected = ref(1);
const openMintModal = ref(false);
const options =[1,2,3,5,8,10]
const now = ref(Math.trunc(new Date().getTime() / 1000));
const props = defineProps({
  date: {
    type: String,
  },
});
onMounted(() => {
  window.setInterval(() => {
    now.value = Math.trunc(new Date().getTime() / 1000);
  }, 1000);
});
const dateInMilliseconds = computed(() => {
  return Math.trunc(Date.parse(props.date) / 1000);
});
const seconds = computed(() => {
  return (dateInMilliseconds.value - now.value) % 60;
});
const minutes = computed(() => {
  return Math.trunc((dateInMilliseconds.value - now.value) / 60) % 60;
});
const hours = computed(() => {
  return Math.trunc((dateInMilliseconds.value - now.value) / 60 / 60) % 24;
});
const days = computed(() => {
  return Math.trunc((dateInMilliseconds.value - now.value) / 60 / 60 / 24);
});
function control(value) {
  if (value < 0) {
    return "00";
  }
  if (value.toString().length <= 1) {
    return `0${value}`;
  }
  return value;
}
function cancelMint() {
  selected.value = 1;
  openMintModal.value = false;
  clearInterval(timer.value);
  time.value = 900;
}
watch(
  [days, hours, minutes, seconds],
  (
    [newdays, newhours, newminutes, newsecons],
    [prevdays, prevhours, prevminutes, prevseconds]
  ) => {
    if (seconds.value < 0) {
      openmintbutton.value = true;
    }
  }
);
function openPaymentWindow() {
  const paymentUrl = `https://payment.nft-maker.io/?p=f23237676083425fab8b46f810936fc3&c=${selected.value}`;
  window.open(paymentUrl, "", "width=500,height=700");
}
</script>

<style lang="scss" scoped></style>
