<template>
  <q-page>
    <div class="row main-hero-section justify-center">
      <div class="col-xs-12 col-sm-6 col-md-6">
        <h2 class="row justify-center text-weight-regular q-pt-xl">
          Lit Phansiri
        </h2>
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
      </div>
      <!-- <div class="col-xs-12 col-sm-6 col-md-6">
        <q-card class="my-card">
          <q-parallax class="main-hero-image" src="@/assets/lit-avatar.jpeg">
          </q-parallax>
        </q-card>
      </div> -->
    </div>
  </q-page>

  <!-- <div class="main-hero-section">
    <h1 hidden>Lit Phansiri</h1>
    <h2 class="main-hero-title text-center">
      <q-img
        loading="lazy"
        src="@/assets/lit-avatar.jpeg"
        style="height: 280px; max-width: 300px"
        class="rounded-borders main-hero-img"
      >
      </q-img>

      <br />
      Lit Phansiri
    </h2>

    <h4 class="main-hero-subtitle text-center">
      <div class="q-gutter-lg">
        <q-badge>Marine</q-badge>
        <q-badge>Father</q-badge>
        <q-badge>Husband</q-badge>
      </div>
    </h4>
    <div class="row justify-center">
      <q-btn
        flat
        class="main-hero-button q-py-sm q-px-xl"
        color="primary"
        label="step into his footprint"
      >
      </q-btn>
    </div>
  </div> -->
</template>

<script>
export default {
  setup() {},
};
</script>

<style scoped>
.main-hero-section {
  height: 100vh;
}

/* .main-hero-image {
  height: 100vh;

} */
</style>
