<script setup>
import Navbar from "./components/Navbar.vue";
import FloatContent from "./components/FloatContent.vue";
import TopMovers from "./components/TopMovers.vue";
import TabVue from "./components/dashboard/Tab.vue";
import Table from "./components/dashboard/Table.vue";
import CryptoDesc from "./components/about/CryptoDesc.vue";
import MoreDesc from "./components/about/MoreDesc.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
  <Navbar />

  <header class="w-full flex justify-between items-center px-14 mt-5">
    <h1 class="text-3xl font-bold font-sans">
      Harga Crypto dalam Rupiah Hari Ini
    </h1>
    <div
      class="px-4 py-2 flex items-center gap-4 text-lg text-gray-600 bg-gray-100 w-96 rounded-lg group cursor-pointer"
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
