<template>
  <q-page class="flex flex-center">
    <h2>{{ msg }}</h2>
    <!-- <p v-for="n in 15" :key="n">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit nihil
      praesentium molestias a adipisci, dolore vitae odit, quidem consequatur
      optio voluptates asperiores pariatur eos numquam rerum delectus commodi
      perferendis voluptate?
    </p> -->
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
