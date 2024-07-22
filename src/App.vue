<script setup>
import LoaderComponent from '@/components/LoaderComponent.vue'
import SidebarMenu from '@/components/SidebarMenu.vue'
import { onMounted, onBeforeUnmount, computed } from 'vue'
import { useSidebar } from '@/stores/sidebar'
import { useLoader } from '@/stores/loader'
import FooterComponent from '@/components/FooterComponent.vue'
import NavbarComponent from '@/components/NavbarComponent.vue'

import AOS from 'aos'
import 'aos/dist/aos.css'

const sidebarStore = useSidebar()
const loaderStore = useLoader()

const isLoading = computed(() => loaderStore.getLoaderState())

onMounted(() => {
  // Initialize AOS (Animate On Scroll)
  AOS.init()

  // Add event listeners
  document.querySelector('.overlay')?.addEventListener('click', () => {
    sidebarStore.closeSidebar()
  })

  document.querySelectorAll('.link').forEach((link) => {
    link.addEventListener('click', () => {
      sidebarStore.closeSidebar()
    })
  })
})

// Clean up event listeners
onBeforeUnmount(() => {
  document.querySelector('.overlay')?.removeEventListener('click', () => {
    sidebarStore.closeSidebar()
  })

  document.querySelectorAll('.link').forEach((link) => {
    link.removeEventListener('click', () => {
      sidebarStore.closeSidebar()
    })
  })
})
</script>

<template>
  <LoaderComponent :class="{'hidden': !isLoading}" />
  <div class="content" v-if="!isLoading">
    <NavbarComponent />
    <RouterView/>
    <FooterComponent />
  </div>
  <SidebarMenu />
</template>

<style scoped>
/* Add any specific styles needed for the layout */
</style>
