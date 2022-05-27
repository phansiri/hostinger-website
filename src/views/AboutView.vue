<template>
  <div class="q-pa-lg">
    <h2 class="q-mt-none">About Me</h2>
    <div class="q-pa-md row items-start q-gutter-md justify-center">
      <q-card flat bordered class="my-card">
        <q-card-section class="text-center">
          I am currently working in the capacity as a Cyberspace Warfare Officer
          for the United States Marine Corps. With over 19 years of experience
          in software engineering and leadership to help advance the
          institution.
        </q-card-section>

        <q-separator inset />

        <q-card-section class="">
          In my previous role, he was the Cyberspace Warfare Officer for Delta
          Company, 3d Radio Battalion based out of Okinawa, Japan. He is now
          working in the 31st Marine Expeditionary Unit as their Officer In
          Charge. Lit shares his experience in backend and frontend development,
          career-related topics, and innovative appoarch with people seeking
          guidance in the tech industry. He spends his free time tinkering on
          his home lab, reading , hanging out with his daughters, and going on
          travel adventures whenever he is not making content or writing code.
        </q-card-section>
      </q-card>
    </div>
    <p></p>
    <p></p>
  </div>
  <TimeLine />
</template>

<script>
import TimeLine from "@/components/TimeLine.vue";
export default {
  components: {
    TimeLine,
  },
};
</script>
