<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <ExempleModificateur m/>
  </div>
</template>

<script>

import ExempleModificateur from '@/components/ExempleModificateur.vue'

export default {
  name: 'HomeView',
  components: {
    ExempleModificateur
  }
}
</script>
