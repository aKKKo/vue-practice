<template>
  <div class="sidebar" @click="close" v-if="sidebar">
    <span class="sidebar-close" @click="close">&times;</span>
    <div class="sidebar-content">
      <p>Какое-то ооооооооооочень длинное сообщение, что бы симитировать большой размер текста, хотя по настоящему никакой смысловой нагрузки он не несет.</p>
    </div>
  </div>
</template>

<script>
import { computed } from 'vue'
import { useStore } from 'vuex'

export default {
  setup() {
    const store = useStore()

    const sidebar = computed(() => store.state.sidebar)

    return {
      sidebar,
      close: () => store.commit('closeSidebar')
    }
  }
}
</script>

<style scoped>

</style>