<template>
  <div
    class="
      md:flex
      items-center
      justify-between
      bg-gray-900
      p-2
      text-white
    "
  >
    <div class="flex items-center gap-3 p-2">
      <a href="https://wa.me/919799495295" class="p-2 border rounded-full bg-white">
        <img
          src="~/assets/whatsapp.png"
          class="h-3"
          alt=""
        />
      </a>

      <nuxt-link to="/paytm">
        <div class="p-2 border rounded-full bg-white">
            <img
              src="~/assets/paytm.png"
              class="h-3"
              alt=""
            />
        </div>
      </nuxt-link>
      
      <nuxt-link to="/phonepe">
        <div class="p-2 border rounded-full bg-white">
          <img
            src="~/assets/phonepe.svg"
            class="h-3"
            alt=""
          />
        </div>
      </nuxt-link>      

      <a href="tel:919799594295" class="px-4 py-2 border rounded-full">
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

    <div class="flex items-center gap-2 mr-3 p-2">
      <a href="https://wa.me/919799495295" class="flex items-center gap-2 px-2 py-1 border rounded-full">
        <div>
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"
            ></path>
          </svg>
        </div>

        <div class="pr-2">
          <div>Online Only</div>
          <div class="text-xs uppercase">BY Appointments</div>
        </div>
      </a>

      <a href="tel:919799594295" class="flex items-center gap-2 px-2 py-1 border rounded-full">
        <div>
          <svg
            class="w-6 h-6"
            fill="none"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M16 3h5m0 0v5m0-5l-6 6M5 3a2 2 0 00-2 2v1c0 8.284 6.716 15 15 15h1a2 2 0 002-2v-3.28a1 1 0 00-.684-.948l-4.493-1.498a1 1 0 00-1.21.502l-1.13 2.257a11.042 11.042 0 01-5.516-5.517l2.257-1.128a1 1 0 00.502-1.21L9.228 3.683A1 1 0 008.279 3H5z"
            ></path>
          </svg>
        </div>
        <div class="pr-2">
          <div>Call Now</div>
          <div class="text-xs uppercase">+91-9799495295</div>
        </div>
      </a>
    </div>
  </div>
</template>