<script setup>
import HeaderSection from '../../components/HeaderSection.vue';

</script>

<template>
    <section class="powers mb-10 sm:mb-20" data-aos="fade-up" data-aos-duration="1000">
        <HeaderSection :title="'My Superpowers'" />
        <div class="techs flex flex-wrap gap-10">
            <img title="HTML" src="/images/stacks/html.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="CSS" src="/images/stacks/css.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Javascript" src="/images/stacks/js.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="React" src="/images/stacks/react.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Vue.js" src="/images/stacks/vue.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Node" src="/images/stacks/sql.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Node" src="/images/stacks/python.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Node Package Manager" src="/images/stacks/npm.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Tailwind Css" src="/images/stacks/tailwindcss.svg" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
            <img title="Visual Studio Code" src="/images/stacks/vscode.png" alt="" class="tech mb-10 w-[18%] sm:w-24 object-contain">
        </div>
    </section>
</template>