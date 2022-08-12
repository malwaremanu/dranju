<template>
  <div>
    <div class="flex flex-col lg:flex-row mx-auto items-center gap-2 mx-auto place-content-center p-3">
      <div class="order-last text-center">
        <div class="text-2xl font-semibold text-gray-700">
          Counselling for your needs
        </div>
        <div class="text-4xl font-semibold">Dr. Anju Choudhary</div>

        <div class="text-sm font-semibold text-gray-500">
          I can help you in Psychotherapy and Mental health.
        </div>

        <div class="flex flex-col lg:flex-row items-center text-left gap-2 p-2 mt-2">
          <a
            href="https://wa.me/919799495295"
            class="
              flex
              items-center
              gap-2
              px-4
              py-2
              border
              rounded-full
              hover:bg-gray-900 hover:text-white
            "
          >
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

          <a
            href="tel:919799594295"
            class="
              flex
              items-center
              gap-2
              px-4
              py-2
              border
              rounded-full
              hover:bg-gray-900 hover:text-white
            "
          >
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

      <div class="relative p-3">
        <img src="~/assets/dr_anju.jpeg" alt="" class="w-52 rounded-md" />
      </div>
    </div>

    <div class="text-center pt-2 text-2xl font-semibold">
      Below are listed only some of the topics we can work on.
    </div>
    <div class="grid lg:grid-cols-4 grid-cols-2 gap-4 container p-6 py-9 mx-auto">
      <div
        v-for="p in psy"
        :key="p"
        class="
          border
          px-6
          py-3
          rounded-xl
          hover:shadow-lg
          shadow-sm
          cursor-pointer
        "
      >
        <div class="text-black text-xl mb-2">
          {{ p.title }}
        </div>
        <div class="text-gray-500 text-sm">
          {{ p.desc }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      psy: [
        {
          title: 'Anxiety',
          desc: 'Anxiety is an emotion characterised by an unpleasent state of inner turnmoil.',
        },
        {
          title: 'Phobia',
          desc: 'A phobia is a type of anxiety disorder defined by a persistent and excessive fear of an object or situation.',
        },
        {
          title: 'Addiction',
          desc: 'Addiction is a biopsychological disorder characterised by repeated use of drugs, or repetitive engagement.',
        },
        {
          title: 'Depression',
          desc: "Depression is a state of low mood and aversion to activity, it can affect a person's thoughts, behaviour, motivation, feelings, and sense of well-being",
        },
      ],
    }
  },
}
</script>