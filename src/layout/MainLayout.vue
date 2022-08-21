<template>
  <the-navbar></the-navbar>
  <the-sidebar></the-sidebar>
  <div class="container with-nav">
    <app-message />
    <router-view />
  </div>
</template>

<script>
import AppMessage from '../components/ui/AppMessage'
import TheSidebar from '@/components/TheSidebar.vue'
import TheNavbar from "../components/TheNavbar"
export default {
  components: {
    TheNavbar,
    AppMessage,
    TheSidebar
  }
}
</script>

<style scoped>

</style>