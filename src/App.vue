<template>
  <component :is='layout'>
    <router-view/>
  </component>
</template>

<script>
import EmptyLayout from '@/layouts/EmprtyLayout.vue'
import MainLayout from '@/layouts/MainLayout.vue'
export default {
  computed: {
    layout() {
      return (this.$route.meta.layout || 'empty') + '-layout'
    }
  },
  components: {
    EmptyLayout, MainLayout
  }
}
</script>

<style>
@import '~materialize-css/dist/css/materialize.min.css';
@import 'assets/index.css';
</style>






