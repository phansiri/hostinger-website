<template>
  <q-page class="flex flex-center bg-grey-4">
    <!-- <img
      alt="Quasar logo"
      src="../assets/logo.svg"
      style="width: 200px; height: 200px"
    /> -->
    <h2>{{ msg }}</h2>
  </q-page>
</template>

<style></style>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>
