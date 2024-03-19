<template>
    <div class="about">
      <TestVuex></TestVuex>
    </div>
  </template>
  
  <script>
  import TestVuex from '@/components/TestVuex.vue'
  
  export default {
    name: 'StoreView',
    components: {
      TestVuex
    }
  }
  </script>