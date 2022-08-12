<template>
  <div class="lg:flex gap-3 items-center">
    <div class="lg:w-1/4 flex flex-col items-center gap-4">
      <img
        src="https://www.devdigital.com/media/blog/News_262.jpg"
        alt=""
        class="lg:w-2/3 p-2"
      />

      <center class="flex items-center gap-2">
        <div
          @click="kam"
          class="
            flex-none
            hover:bg-gray-900
            bg-gray-200
            hover:text-white
            rounded-full
            p-1
            cursor-pointer
          "
        >
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
              d="M15 19l-7-7 7-7"
            ></path>
          </svg>
        </div>

        <div
          @click="jyada"
          class="
            flex-none
            hover:bg-gray-900
            bg-gray-200
            hover:text-white
            rounded-full
            p-1
            cursor-pointer
          "
        >
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
              d="M9 5l7 7-7 7"
            ></path>
          </svg>
        </div>
      </center>
    </div>
    <div class="lg:w-3/4">
      <div class="bg-white p-4 flex items-center">
        
          <center>
            <img :src="actual_pic" alt="" class="max-h-80" />
          </center>
        
      </div>
    </div>
  </div>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'

export default {
  data() {
    return {
      count: '1',
      line: '',
      actual_pic: '~/assets/screenshot_review/1.png',
      i: 2,
    }
  },
  name: 'MyComponent',
  components: { VueSlickCarousel },

  mounted() {
    // setTimeout(() => {  this.details() }, 1000);

    setInterval(this.details(), 1000)
  },

  methods: {
    getImgUrl(pet) {
      var images = require.context(
        '~/assets/screenshot_review',
        false,
        /\.png$/
      )
      return images('./' + pet + '.png')
    },
    // async details() {
    //     let headersList = {
    //     "Authorization": "Basic bWFsd2FyZW1hbnU6TWFudUBoYXJwZXIx",
    //     "Content-Type": "application/json"
    //     }

    //     let bodyContent = JSON.stringify({
    //         "operation": "sql",
    //         "sql": "select * from anju.reviews"
    //     });

    //     let response = await fetch("https://po-manu.harperdbcloud.com", {
    //         method: "POST",
    //         body: bodyContent,
    //         headers: headersList
    //     });

    //     let data = await response.json();
    //     console.log(data);
    //     this.reviews = data
    // },

    details() {
      // this.line = '~/assets/screenshot_review/' + this.i + '.png'
      // console.log(i)

      console.log(this.i)
      if (this.i == 47) {
        this.i = 1
      } else {
        this.i += 1
      }

      this.actual_pic = this.getImgUrl(this.i)
    },

    kam() {
      console.log(this.i)
      if (this.i == 1) {
        this.i = 47
      } else {
        this.i -= 1
      }

      this.actual_pic = this.getImgUrl(this.i)
    },

    jyada() {
      console.log(this.i)
      if (this.i == 47) {
        this.i = 1
      } else {
        this.i += 1
      }

      this.actual_pic = this.getImgUrl(this.i)
    },
  },
}
</script>

<style>
* {
  box-sizing: border-box;
}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

/* Hide the images by default */
.mySlides {
  display: none;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* The dots/bullets/indicators */
.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active,
.dot:hover {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}
</style>