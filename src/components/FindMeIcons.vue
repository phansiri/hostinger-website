<template>
  <div class="row justify-center q-pa-md q-gutter-sm">
    <q-btn
      rounded
      color="purple"
      target="_blank"
      href="https://github.com/phansiri"
      ><q-icon :name="fabGithub"
    /></q-btn>

    <q-btn rounded color="green" target="_blank" href="https://www.marines.mil/"
      ><q-icon :name="fasPersonMilitaryRifle"
    /></q-btn>

    <q-btn
      rounded
      color="purple"
      target="_blank"
      href="https://www.linkedin.com/in/litthideth-phansiri-6b79b098/"
      ><q-icon :name="fabLinkedinIn"
    /></q-btn>
  </div>
</template>

<script>
import {
  fabGithub,
  fabLinkedinIn,
  fasPersonMilitaryRifle,
} from "@quasar/extras/fontawesome-v6";

export default {
  created() {
    this.fabGithub = fabGithub;
    this.fabLinkedinIn = fabLinkedinIn;
    this.fasPersonMilitaryRifle = fasPersonMilitaryRifle;
  },
};
</script>
