<script setup>
import IntroComponent from '@/views/folio/IntroComponent.vue'
import AboutComponent from '@/views/folio/AboutComponent.vue'
import PowersComponent from '@/views/folio/PowersComponent.vue'
// import ExperiencesComponent from '@/views/folio/ExperiencesComponent.vue'
import ProjectComponent from '@/views/folio/ProjectComponent.vue'
import OtherProjects from '@/views/folio/OtherProjects.vue'
import ContactComponent from '@/views/folio/ContactComponent.vue'
</script>

<template>
  <div class="main">
      <IntroComponent />
      <AboutComponent />
      <PowersComponent />
      <!-- <ExperiencesComponent /> -->
      <ProjectComponent />
      <OtherProjects />
      <ContactComponent />
    </div>
</template>
