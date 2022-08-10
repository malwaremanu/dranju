<template>
  <div class="bg-gray-900">
    <div v-show="!sent">
      <div
        class="
          max-w-7xl
          mx-auto
          py-12
          px-4
          sm:px-6
          lg:py-16 lg:px-8 lg:flex lg:items-center lg:justify-between
        "
      >
        <h2
          class="text-3xl font-extrabold tracking-tight text-white sm:text-4xl"
        >
          <span class="block">Need Appointment ?</span>
          <span class="block text-green-400">Book it now</span>
        </h2>
        <div class="mt-8 md:flex lg:mt-0 lg:flex-shrink-0 gap-3">
          <div class="inline-flex rounded-md shadow p-1">
            <input
              type="text"
              placeholder="Name"
              class="
                px-5
                py-3
                rounded-md
                text-white
                outline-none
                w-full
                bg-gray-600
              "
            />
          </div>

          <div class="inline-flex rounded-md shadow p-1">
            <input
              type="number"
              placeholder="+91-Mobile Number"
              class="
                px-5
                py-3
                rounded-md
                text-white
                outline-none
                w-full
                bg-gray-600
              "
            />
          </div>

          <div class="inline-flex rounded-md shadow p-1">
            <input
              type="date"
              class="
                px-5
                py-3
                rounded-md
                text-white
                outline-none
                w-full
                bg-gray-600
              "
            />
          </div>

          <div class="inline-flex rounded-md shadow p-1">
            <button
              @click="book"
              class="
                inline-flex
                items-center
                justify-center
                px-5
                py-3
                border border-transparent
                text-base
                font-medium
                rounded-md
                text-white
                bg-green-600
                hover:bg-green-700
              "
            >
              Book
            </button>
          </div>
        </div>
      </div>
    </div>

    <div v-show="sent"  class="
          max-w-7xl
          mx-auto
          py-12
          px-4
          sm:px-6
          lg:py-16 lg:px-8 lg:flex lg:items-center lg:justify-between
        ">
      <h2 class="text-3xl font-extrabold tracking-tight text-white sm:text-4xl">
         <span class="block">Appointment Status</span>
        <span class="block text-green-400"> {{ msg }} </span>
        <button class="text-sm uppercase px-4 py-2 border text-green-600 border-green-600 hover:border-green-400 hover:text-green-400 rounded-full" @click="sent = false">Close</button>
      </h2>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
        sent: false,
        msg: 'It has been booked.',
        }
    },
    methods: {
        book() {
        this.sent = true
        },
    },
}
</script>