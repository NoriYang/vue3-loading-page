<script setup>
import { ref } from 'vue'
import LoadingPage from './components/LoadingPage.vue';

const loadingFlag = ref(true)
function closeLoadingPage() {
  setTimeout(() => {
    loadingFlag.value = false
  }, 1500)
}
</script>

<template>
  <div>
    <div v-if="loadingFlag">
      <LoadingPage @closeHandler="closeLoadingPage" />
    </div>
    <div>
      <h1>HelloWorld</h1>
    </div>
  </div>
</template>

<style scoped>

</style>
