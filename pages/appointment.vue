<template>
  <div class="select-none min-h-screen">
    <Header />
    <br />

    <Appointment />

    <Reviews />
    <Footer />

  </div>
</template>

<script>
import Header from '../components/header.vue'
import Footer from '~/components/footer.vue';
import Appointment from '~/components/appointment.vue';

export default {
  name: 'Appointments',
  components: { Header, Footer, Appointment },
}
</script>
