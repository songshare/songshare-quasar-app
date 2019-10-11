<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-full.svg"
    >
    <div class="row">
      <test />
      <test />
    </div>
  </q-page>
</template>

<script>
import Test from '../components/Test'

export default {
  name: 'PageIndex',
  components: {
    'test': Test
  }
}
</script>
