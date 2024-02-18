<script setup>
import ImageOpener from '@/components/ImageOpener.vue'
import ImageContainer from '@/components/ImageContainer.vue'
</script>

<template>
  <main class="flex flex-row main-content">
    <ImageContainer v-if="imageIsOpen"/>
    <ImageOpener v-if="!imageIsOpen" @click="openImage"/>
  </main>
</template>

<script>

export default {
  data() {
    return {
      imageIsOpen: false
    }
  },
  methods: {
    openImage() {
      console.log('opening image')
      this.imageIsOpen = true
      console.log('image opened')
    }
  }
}

</script>
