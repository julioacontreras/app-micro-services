<template>
  <div class="app-new-project">
    <alert
      typeAlert = "info"
      title = "Info"
      message = "Made with Vue3"
      :isVisible="isVisible"   
      @close="close"   
    ></alert>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import './assets/style/main.scss'
import alert from './components/alert/alertComponent.vue'

const isVisible = ref(true) 

function close () {
  isVisible.value = false
}
</script>
