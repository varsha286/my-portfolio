<script setup>
import HeaderSection from '../../components/HeaderSection.vue'
</script>

<template>
  <section class="about min-h-[70vh]" id="about" data-aos="fade-up" data-aos-duration="1000" data-oas-offset="5000px">
    <HeaderSection :title="'About me'" />
    <div class="flex justify-center items-center m-auto">
      <div class="flex-row sm:flex sm:justify-between items-center sm:space-x-3 space-y-7 sm:space-y-0">
        <div class="text sm:w-[60%] space-y-2 text-sm md:text-base text-appgray font-medium">
          <p class="leading-relaxed">
            Hello! I am Varsha P, an aspiring web developer with a passion for building web applications. My journey
            into coding began during my college years, and I've been fascinated by the world of web development ever
            since.
          </p>
          <p class="leading-relaxed">
            I have been learning and working with various technologies, including HTML, CSS, JavaScript, and popular
            frameworks. My goal is to create user-friendly and engaging web experiences that make a difference.
          </p>
          <p class="leading-relaxed">
            Throughout my studies, I have worked on several personal and academic projects that have helped me develop
            my skills. These projects have given me valuable experience in both individual and collaborative settings.
          </p>
          <p class="leading-relaxed">
            Outside of coding, I have a deep love for music, which provides me with inspiration and relaxation. Music is
            an integral part of my life, and it fuels my creativity and enthusiasm for web development.
          </p>
        </div>

      </div>
    </div>
  </section>
</template>

<style scoped></style>
