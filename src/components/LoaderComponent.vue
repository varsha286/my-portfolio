<script setup>
import { ref, onMounted } from 'vue'
import { useLoader } from '../stores/loader'

const loaderStore = useLoader()

const loader = ref(null)

function complete() {
  setTimeout(() => {
    loaderStore.changeLoading(false)
  }, 1000) // Adjust this delay to match your desired animation speed
}

onMounted(() => {
  // Optional: Additional initialization logic if needed
})
</script>

<template>
  <div
    ref="loader-container"
    class="loader-container"
  >
    <!-- Use img tag to include SVG -->
    <img
      ref="loader"
      src="../assets/Varsha_loader.svg"
      alt="Loading..."
      class="loader-image"
      @load="complete"
    />
  </div>
</template>

<style scoped>
.loader-container {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  background-color: var(--appbg); /* Ensure background color is consistent */
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 1;
  transition: opacity 1s ease-in-out; /* Adjust duration to slow down fade-in/out */
}

.loader-container.hidden {
  opacity: 0; /* Make loader invisible */
}

.loader-image {
  width: 450px; /* Adjust size as needed */
  height: auto; /* Maintain aspect ratio */
}
</style>
