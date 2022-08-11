<template>
  <div class="select-none min-h-screen">
    <Header />
    <br />

    <Whoami />

    <Quotes />

    <Reviews />
  
    <Appointment />

    <Footer />

  </div>
</template>

<script>
import Header from '../components/header.vue'
import Appointment from '../components/appointment.vue'
import Footer from '../components/footer.vue'
import Whoami from '~/components/whoami.vue';
import Reviews from '~/components/reviews.vue';

export default {
  name: 'IndexPage',
  components: { Header, Appointment, Footer, Whoami, Reviews },
}
</script>
