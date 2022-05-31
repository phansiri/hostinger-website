<template>
  <q-page class="q-pa-lg">
    <h2 class="q-mt-none">Work</h2>
    <project-module></project-module>
  </q-page>
</template>

<script>
import { useMeta } from "quasar";
import { ref } from "vue";
import ProjectModule from "@/components/ProjectModule.vue";
export default {
  components: {
    ProjectModule,
  },
  setup() {
    const title = ref("Lit | Work");
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
