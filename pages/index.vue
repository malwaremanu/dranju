<template>
  <div class="select-none min-h-screen">
    <Header />
    <br />

    <Whoami />

    <Megafooter />

  </div>
</template>

<script>
import Header from '../components/header.vue'
import Whoami from '~/components/whoami.vue';
import Megafooter from '~/components/megafooter.vue';

export default {
  name: 'IndexPage',
  components: { Header, Whoami, Megafooter },
}
</script>
