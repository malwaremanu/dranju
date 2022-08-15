<template>
  <div>
    <VueSlickCarousel
      :arrows="true"
      :dots="true"
      v-bind="settings"
      autoplay="True"
    >
      <div class="">
        <img src="~/assets/caras/1.jpg" />
      </div>

      <div class="">
        <img src="~/assets/caras/2.jpg" />
      </div>

      <div class="">
        <img src="~/assets/caras/3.png" />
      </div>
    </VueSlickCarousel>
  </div>
</template>
 
<script>
import VueSlickCarousel from 'vue-slick-carousel'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  name: 'MyComponent',
  data() {
    return {
      settings: {
        dots: true,
        dotsClass: 'slick-dots custom-dot-class',
        edgeFriction: 0.35,
        infinite: true,
        speed: 500,
        slidesToShow: 1,
        slidesToScroll: 1,
      },
    }
  },
  components: { VueSlickCarousel },
}
</script> 