<template>
  <q-page>
    <div class="row main-hero-section justify-center">
      <div class="col-xs-12 col-sm-6 col-md-6">
        <h2 class="row justify-center text-weight-regular q-pt-xl">
          Lit Phansiri
        </h2>
        <type-writer
          class="row justify-center text-weight-regular q-pb-xl"
          :words="[
            'Software Engineer',
            'DevSecOps Engineer',
            'Innovator',
            'Leader',
          ]"
        >
        </type-writer>
        <div class="row justify-center">
          <div class="q-gutter-lg">
            <q-badge transparent>Father</q-badge>
            <q-badge color="red" transparent>Marine</q-badge>
            <q-badge transparent>Husband</q-badge>
          </div>
        </div>
        <div class="row justify-center q-pt-xl">
          <q-btn
            flat
            to="/about"
            class="main-hero-button q-py-sm q-px-xl"
            color="primary"
            label="find out more"
          >
          </q-btn>
        </div>
        <find-me-icons />
      </div>
    </div>
    <div class="col-xs-12 col-sm-6 col-md-6">
      <q-card class="my-card">
        <q-parallax
          class="main-hero-image"
          :speed="1.7"
          src="@/assets/lit-avatar.jpeg"
        >
        </q-parallax>
      </q-card>
    </div>
  </q-page>
</template>

<script>
import TypeWriter from "./TypeWriter.vue";
import FindMeIcons from "@/components/FindMeIcons.vue";
export default {
  components: { TypeWriter, FindMeIcons },
  setup() {},
};
</script>

<style scoped>
.main-hero-section {
  height: 100vh;
}
.main-hero-image {
  opacity: 0.7;
}
</style>
