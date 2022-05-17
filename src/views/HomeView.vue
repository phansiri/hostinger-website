<template>
  <q-page>
    <HeroSection />
  </q-page>
  <q-page>
    <MainDesc />
  </q-page>
</template>

<script>
// @ is an alias to /src
import HeroSection from "@/components/HeroSection.vue";
import MainDesc from "@/components/MainDesc.vue";

export default {
  name: "HomeView",
  components: {
    HeroSection,
    MainDesc,
  },
};
</script>
