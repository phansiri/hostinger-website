<template>
  <q-card flat class="text-center q-mx-md">
    <q-img src="@/assets/p1-uw-nrotc.png" />
    <q-card-section>
      <q-separator />
      <div class="text-h6">
        <a href="http://nrotc.washington.edu/" target="_blank">UW NROTC</a>
      </div>
      <div class="text-subtitle2">
        Redesigned website to allow easy update while having a professional
        website. The project was to update their antiquated drupal website to a
        modern design where any user can quickly update without truely
        understand programming.
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
    },
  },
};
</script>
