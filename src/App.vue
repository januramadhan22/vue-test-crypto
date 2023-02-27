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
  return fetch("https://api.pintu.co.id/v2/trade/price-changes")
    .then((response) => response.json())
    .then((data) => console.log(data.payload));
};

onMounted(() => {
  getDatas();
});
</script>

<template @click="search()">
  <Navbar />

  <header class="w-full flex justify-between items-center px-14 mt-5">
    <h1 class="text-3xl font-bold font-sans">
      Harga Crypto dalam Rupiah Hari Ini
    </h1>
    <div class="relative">
      <div
        @click="search"
        class="px-4 py-2 flex items-center gap-4 text-lg text-gray-600 bg-gray-100 w-96 rounded-lg group cursor-pointer relative"
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
        <p>Cari aset di Pintu...</p>
      </div>

      <!-- Open Search -->
      <div
        :class="[
          openSearch
            ? `flex absolute w-full bg-white h-72 top-0 left-0 shadow-md border rounded-lg p-4 z-40`
            : `hidden`,
        ]"
      >
        <form
          class="px-4 py-2 h-fit flex items-center gap-4 text-lg text-gray-600 bg-gray-100 w-96 rounded-lg group cursor-pointer"
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
      </div>
    </div>
  </header>

  <TopMovers />

  <div class="px-14 space-y-4">
    <TabVue />
    <Table />
  </div>

  <div class="px-14 space-y-8 py-8">
    <CryptoDesc />
    <MoreDesc />
  </div>

  <Footer />

  <FloatContent />
</template>

<style scoped></style>
