<template>
  <q-page class="q-pa-lg">
    <h2 class="q-mt-none">Work</h2>
    <project-module></project-module>
  </q-page>
</template>

<script>
import ProjectModule from "@/components/ProjectModule.vue";
export default {
  components: {
    ProjectModule,
  },
};
</script>
