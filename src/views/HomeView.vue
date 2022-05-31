<template>
  <q-page>
    <HeroSection />
    <MainDesc />
  </q-page>
</template>

<script>
// @ is an alias to /src
import HeroSection from "@/components/HeroSection.vue";
import MainDesc from "@/components/MainDesc.vue";

import { useMeta } from "quasar";
import { ref } from "vue";

export default {
  name: "HomeView",
  components: {
    HeroSection,
    MainDesc,
  },
  setup() {
    const title = ref("Lit | Home");
    useMeta(() => {
      return {
        title: title.value,
      };
    });
    function setAnotherTitle() {
      title.value = "Another title";
    }

    return {
      setAnotherTitle,
    };
  },
};
</script>
