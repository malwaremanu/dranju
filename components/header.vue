<template>
  <div class="md:flex items-center justify-between bg-gray-900 p-2 text-white">
    <div class="px-4 flex items-center gap-3">
      <div>
        <nuxt-link
          to="/"
          class="
            flex
            items-center
            gap-2
            rounded-full
            px-3
            py-2
            border
            hover:bg-gray-800 hover:shadow-lg
            cursor-pointer
          "
        >
          <svg
            class="w-5 h-5"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
            ></path>
          </svg>
          Home
        </nuxt-link>
      </div>
      <div>
        <nuxt-link
          to="/appointment"
          class="
            flex
            items-center
            gap-2
            rounded-full
            px-3
            py-2
            border
            hover:bg-gray-800 hover:shadow-lg
            cursor-pointer
          "
        >
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 8h10M7 12h4m1 8l-4-4H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-3l-4 4z"></path></svg>
          Appointment
        </nuxt-link>
      </div>
    </div>

    <div class="flex items-center gap-3 p-2">
      <a
        href="https://wa.me/919799495295"
        class="p-2 border rounded-full bg-white"
      >
        <img src="~/assets/whatsapp.png" class="h-3" alt="" />
      </a>

      <nuxt-link to="/paytm">
        <div class="p-2 border rounded-full bg-white">
          <img src="~/assets/paytm.png" class="h-3" alt="" />
        </div>
      </nuxt-link>

      <nuxt-link to="/phonepe">
        <div class="p-2 border rounded-full bg-white">
          <img src="~/assets/phonepe.svg" class="h-3" alt="" />
        </div>
      </nuxt-link>

      <a href="tel:919799495295" class="px-4 py-2 border rounded-full">
        <svg
          class="w-4 h-4"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
          ></path>
        </svg>
      </a>
    </div>
  </div>
</template>
