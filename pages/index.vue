<template>
  <div>
    <Header />
    <br />

    <div>
      <div class="text-2xl font-semibold">Dr Anju Choudhary</div>
      <img src="~/assets/dr_anju.jpeg" alt="" class="w-28 rounded-md" />
    </div>

  
    <Appointment />

    <Footer />

  </div>
</template>

<script>
import Header from '../components/header.vue'
import Appointment from '../components/appointment.vue'
import Footer from '../components/footer.vue'
export default {
  name: 'IndexPage',
  components: { Header, Appointment, Footer },
}
</script>
