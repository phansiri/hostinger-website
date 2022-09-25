<template>
  <section class="main-desc-section q-pt-xl p-pxp-md">
    <h2 class="row justify-center text-weight-regular q-pt-xl">Who Am I</h2>
    <div class="q-pa-md row items-start q-gutter-md justify-center">
      <q-card flat bordered class="my-card">
        <q-card-section class="text-center">
          Qualified technologist and military leader with more than 19 years of
          experience.
        </q-card-section>

        <q-separator inset />

        <q-card-section class="">
          <ul>
            Continues to work with and builds high energy, high value teams to
            study, design and develop information technology solutions for the
            good of people, organizations, and society.
          </ul>
          <ul>
            Talented and passionate for finding creative solutions to complex
            problems while developing information technology to meet goals.
          </ul>
          <ul>
            Hands on leader with an intimate knowledge of technology, tools, and
            people.
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
