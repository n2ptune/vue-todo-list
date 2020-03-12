<template>
  <div id="app">
    <Header />
    <router-view class="pt-16" />
  </div>
</template>

<script>
import Header from '@/components/layouts/Header.vue'

export default {
  components: {
    Header
  }
}
</script>
