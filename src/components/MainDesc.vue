<template>
  <section class="main-desc-section q-pt-xl p-pxp-md">
    <h2 class="row justify-center text-weight-regular q-pt-xl">Who Am I</h2>
    <div class="q-pa-md row items-start q-gutter-md justify-center">
      <q-card flat bordered class="my-card">
        <q-card-section class="text-center">
          Experienced technologist and military leader with over 20 years of
          proven expertise.
        </q-card-section>

        <q-separator inset />

        <q-card-section class="">
          <ul>
            I consistently collaborate with assemble dynamic, high-impact teams
            dedicated to researching, conceiving, and crafting information
            technology solutions that benefit individuals, institutions, and
            society as a whole.
          </ul>
          <ul>
            My innate talent and unwavering passion drive me to unearth
            innovative answers to intricate challenges while effectively
            utilizing information technology to achieve objectives.
          </ul>
          <ul>
            I am a hands-on leader endowed with an intimate understanding of
            technology, tools, and the people who make it happen.
          </ul>
        </q-card-section>
        <q-separator inset />

        <q-card-section class="text-center">
          <q-btn round color="blue" href="mailto:lit+website@phansiri.com"
            ><q-icon :name="fasEnvelopeOpenText"
          /></q-btn>
        </q-card-section>
      </q-card>
    </div>
  </section>
</template>

<script>
import { fasEnvelopeOpenText } from "@quasar/extras/fontawesome-v6";
export default {
  created() {
    this.fasEnvelopeOpenText = fasEnvelopeOpenText;
  },
};
</script>

<style lang="scss" scoped>
.main-desc-section {
  // background-color: #bdbdbd;
  height: 100vh;
}
</style>
