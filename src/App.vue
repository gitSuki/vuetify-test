<script setup>
import SideBar from './components/SideBar.vue'
import ImageGallery from './components/ImageGallery.vue'

import { ref } from 'vue'

const isGrayscale = ref(false)
function toggleGrayscale(newValue) {
  isGrayscale.value = newValue
}
</script>

<template>
  <v-app>
    <side-bar @selectColorOption="toggleGrayscale"></side-bar>
    <v-main>
      <image-gallery :isGrayscale="isGrayscale"></image-gallery>
    </v-main>
  </v-app>
</template>