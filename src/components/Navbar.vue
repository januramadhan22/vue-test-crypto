<script>
import { ref } from "vue";

export default {
  setup() {
    let open = ref(false);

    const menuOpen = () => {
      open.value = !open.value;
    };
    return { open, menuOpen };
  },
};
</script>

<template>
  <div
    class="w-full px-5 md:px-14 py-8 flex justify-between items-center relative"
  >
    <button>
      <img
        src="https://bitcoinindonesia.net/wp-content/uploads/2020/06/logo-pintu-crypto-700x149.png"
        alt="Pintu"
        class="w-20"
      />
    </button>

    <!-- Desktop View -->
    <div class="hidden lg:flex items-center text-lg font-normal font-sans">
      <!-- Fitur -->
      <div class="px-10 group cursor-pointer relative dropdown">
        <span class="group-hover:opacity-40">Fitur</span>
        <div
          class="w-96 p-4 rounded-md shadow-lg absolute -left-4 bg-white transition ease-in menu"
        >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Harga Cryptocurrency
            <span class="text-sm text-gray-400 font-normal"
              >Pantau harga Bitcoin dan aset crypto lainnya</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Earn
            <span class="text-sm text-gray-400 font-normal"
              >Simpan aset crypto, dapatkan bunga tiap jam</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Biaya Transaksi
            <span class="text-sm text-gray-400 font-normal"
              >Lihat biaya trading, tarik Rupiah, dan kirim aset crypto</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >OTC
            <span class="text-sm text-gray-400 font-normal"
              >Layanan personal dengan harga khusus untuk transaksi dengan
              jumlah besar</span
            ></a
          >
        </div>
      </div>

      <!-- PTU -->
      <a class="px-10 hover:opacity-40 cursor-pointer">PTU</a>

      <!-- Edukasi -->
      <div class="px-10 group cursor-pointer relative dropdown">
        <span class="group-hover:opacity-40">Edukasi</span>
        <div
          class="w-96 p-4 rounded-md shadow-lg absolute -left-4 bg-white transition ease-in menu"
        >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Tentang
            <span class="text-sm text-gray-400 font-normal"
              >Jelajahi dunia crypto bersama Pintu</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Pintu Academy
            <span class="text-sm text-gray-400 font-normal"
              >Kumpulan artikel untuk bantu kamu memahami crypto dengan lebih
              gampang</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >FAQ
            <span class="text-sm text-gray-400 font-normal"
              >Informasi seputar crypto dan cara menggunakan aplikasi
              Pintu</span
            ></a
          >
        </div>
      </div>

      <!-- Ikuti Kami -->
      <div class="px-10 group cursor-pointer relative dropdown">
        <span class="group-hover:opacity-40">Ikuti Kami</span>
        <div
          class="w-96 p-4 rounded-md shadow-lg absolute -left-4 bg-white transition ease-in menu z-50"
        >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Telegram
            <span class="text-sm text-gray-400 font-normal"
              >@pintuindonesia</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Twitter
            <span class="text-sm text-gray-400 font-normal">@pintuID</span></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Instagram
            <span class="text-sm text-gray-400 font-normal">@pintu_id</span></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Youtube
            <span class="text-sm text-gray-400 font-normal"
              >Pintu - Aplikasi Jual Beli Cryptocurrency</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Facebook
            <span class="text-sm text-gray-400 font-normal"
              >pintucrypto</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Discord
            <span class="text-sm text-gray-400 font-normal"
              >pintuindonesia</span
            ></a
          >
        </div>
      </div>

      <!-- Blog & News -->
      <div class="px-10 group cursor-pointer relative dropdown">
        <span class="group-hover:opacity-40">Blog & News</span>
        <div
          class="w-96 p-4 rounded-md shadow-lg absolute -left-4 bg-white transition ease-in menu z-50"
        >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Pintu Blog
            <span class="text-sm text-gray-400 font-normal"
              >Kumpulan artikel crypto, keuangan, dan informasi terbaru terkait
              Pintu.</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Pintu News
            <span class="text-sm text-gray-400 font-normal"
              >Temukan update berita terkini tentang crypto, blockchain, hingga
              NFT!</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Pintu Press Kit
            <span class="text-sm text-gray-400 font-normal"
              >Temukan logo resmi, foto, dan kumpulan press release Pintu untuk
              materi promosi di sini.</span
            ></a
          >
        </div>
      </div>

      <!-- Karier -->
      <div class="px-10 group cursor-pointer relative dropdown">
        <span class="group-hover:opacity-40">Karier</span>
        <div
          class="w-96 p-4 rounded-md shadow-lg absolute -right-4 bg-white transition ease-in menu z-50"
        >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Karier
            <span class="text-sm text-gray-400 font-normal"
              >Temukan pekerjaan impianmu di sini.</span
            ></a
          >
          <a
            href="#"
            class="flex flex-col gap-2 font-medium text-left p-4 hover:bg-blue-50 rounded-lg"
            >Karier Engineering
            <span class="text-sm text-gray-400 font-normal"
              >Bergabung dengan tim engineering kami menciptakan platform
              blockchain yang canggih.</span
            ></a
          >
        </div>
      </div>
    </div>

    <!-- Mobile View -->
    <button @click="menuOpen()" class="block lg:hidden">
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
          d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
        />
      </svg>
    </button>

    <div
      class="w-full min-h-screen shadow bg-white fixed top-0 left-0 z-50 -translate-y-[1000px] opacity-0 transition ease-in duration-300 flex flex-col divide-y items-start"
      :class="[open && `opacity-100 translate-y-[0.1px]`]"
    >
      <!-- Header -->
      <header class="w-full px-6 py-10 flex justify-between items-center">
        <button>
          <img
            src="https://bitcoinindonesia.net/wp-content/uploads/2020/06/logo-pintu-crypto-700x149.png"
            alt="Pintu"
            class="w-20"
          />
        </button>
        <button @click="menuOpen()">
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
      </header>

      <!-- Fitur -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          Fitur
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
              d="M19.5 8.25l-7.5 7.5-7.5-7.5"
            />
          </svg>
        </button>
      </div>

      <!-- PTU -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          PTU
        </button>
      </div>

      <!-- Edukasi -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          Edukasi
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
              d="M19.5 8.25l-7.5 7.5-7.5-7.5"
            />
          </svg>
        </button>
      </div>

      <!-- Ikuti Kami -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          Ikuti Kami
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
              d="M19.5 8.25l-7.5 7.5-7.5-7.5"
            />
          </svg>
        </button>
      </div>

      <!-- Blog & News -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          Blog & News
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
              d="M19.5 8.25l-7.5 7.5-7.5-7.5"
            />
          </svg>
        </button>
      </div>

      <!-- Karier -->
      <div class="w-full p-6 flex flex-col">
        <button class="w-full flex justify-between items-center text-lg">
          Karier
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
              d="M19.5 8.25l-7.5 7.5-7.5-7.5"
            />
          </svg>
        </button>
      </div>
    </div>
  </div>
</template>
