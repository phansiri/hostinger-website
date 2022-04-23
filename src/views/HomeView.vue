<template>
  <q-page>
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <HeroSection />
  </q-page>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import HeroSection from "@/components/HeroSection.vue";

export default {
  name: "HomeView",
  components: {
    HeroSection,
  },
};
</script>
