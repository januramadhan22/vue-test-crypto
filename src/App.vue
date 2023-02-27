<script setup>
import Navbar from "./components/Navbar.vue";
import FloatContent from "./components/FloatContent.vue";
import TopMovers from "./components/TopMovers.vue";
import TabVue from "./components/dashboard/Tab.vue";
import Table from "./components/dashboard/Table.vue";
import CryptoDesc from "./components/about/CryptoDesc.vue";
import MoreDesc from "./components/about/MoreDesc.vue";
import Footer from "./components/Footer.vue";
import { onMounted, ref } from "vue";

const cryptosData = ref([]);
let openSearch = ref(false);

const search = () => {
  openSearch.value = !openSearch.value;
};

const getDatas = async () => {
  return fetch("https://api.pintu.co.id/v2/wallet/supportedCurrencies")
    .then((response) => response.json())
    .then((datas) => (cryptosData.value = datas.payload));
};

onMounted(() => {
  getDatas();
});
</script>

<template @click="search()">
  <Navbar />

  <header class="w-full flex justify-between items-center px-8 md:px-14 mt-5">
    <h1 class="text-xl md:text-3xl font-bold font-sans">
      Harga Crypto dalam Rupiah Hari Ini
    </h1>
    <div class="relative">
      <div
        @click="search"
        class="px-0 py-0 md:px-4 md:py-2 flex items-center gap-4 text-lg text-gray-600 bg-transparent md:bg-gray-100 w-fit md:w-96 rounded-lg group cursor-pointer relative"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
          />
        </svg>
        <p class="hidden md:block">Cari aset di Pintu...</p>
      </div>

      <!-- Open Search -->
      <div
        :class="[
          openSearch
            ? ` flex flex-col gap-2 absolute w-96 md:w-full bg-white h-96 top-0 right-0  shadow-md border rounded-lg p-4 z-40`
            : `hidden`,
        ]"
      >
        <form
          class="w-full px-4 py-2 h-fit flex items-center gap-4 text-lg text-gray-600 bg-gray-100 rounded-lg group cursor-pointer"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-8 h-8 text-xl"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M21 21l-5.197-5.197m0 0A7.5 7.5 0 105.196 5.196a7.5 7.5 0 0010.607 10.607z"
            />
          </svg>
          <input
            placeholder="Cari aset di Pintu..."
            class="bg-transparent w-full focus:outline-none"
          />
          <button @click="search()">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6 text-2xl"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </form>

        <!-- List Currency -->
        <div class="w-full flex flex-col overflow-y-scroll">
          <div
            v-for="crypto in cryptosData"
            :key="index"
            class="cursor-pointer w-full px-4 py-3 flex items-center justify-between rounded-md hover:bg-gray-100"
          >
            <span
              class="flex items-center gap-2 font-medium text-lg text-gray-800"
            >
              <img :src="crypto.logo" alt="" class="w-4" />
              {{ crypto.name }}</span
            >
            <span class="text-lg text-gray-500">{{
              crypto.currencySymbol
            }}</span>
          </div>
        </div>
      </div>
    </div>
  </header>

  <TopMovers />

  <div class="px-8 md:px-14 space-y-4">
    <TabVue />
    <Table />
  </div>

  <div class="px-8 md:px-14 space-y-8 py-8">
    <CryptoDesc />
    <MoreDesc />
  </div>

  <Footer />

  <FloatContent />
</template>

<style scoped></style>
