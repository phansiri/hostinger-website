<template>
  <div class="q-pa-lg">
    <h2 class="q-mt-none">About Me</h2>
    <div class="q-pa-md row items-start q-gutter-md justify-center">
      <q-card flat bordered class="my-card">
        <q-card-section class="text-center">
          I presently serve as a Cyberspace Warfare Officer within the United
          States Marine Corps. My background boasts over 20 years of experience
          in leadership and software engineering, which I am eager to leverage
          to drive progress within the organiazation.
        </q-card-section>

        <q-separator inset />

        <q-card-section class="">
          In my previous role, I worked as the Cyberspace Warfare Officer with
          the 31st Marine Expeditionary Unit based out of Okinawa, Japan. Now I
          am working in the Marine Corps Cyberspace Warfare Group as a
          Cyberspace Warfare Officer. I enjoy imparting my expertise in both
          backend and frontend development, offering insights on career-related
          subjects, and sharing innovative approaches with individuals seeking
          guidance in the tech industry. In my leisure time, you'll often find
          me experiementing with and in my home lab server, engrossed in
          reading, spending quality moments with my two daughters, or embarking
          on exciting travel adventures. These activities fill my life when I'm
          not activity creating content or coding.
        </q-card-section>
      </q-card>
    </div>
    <p></p>
    <p></p>
  </div>
  <TimeLine />
</template>

<script>
import { ref } from "vue";
import { useMeta } from "quasar";
import TimeLine from "@/components/TimeLine.vue";
export default {
  components: {
    TimeLine,
  },
  setup() {
    const title = ref("Lit | About");
    useMeta(() => {
      return {
        title: title.value,
      };
    });
    function setAnotherTitle() {
      title.value = "Another title";
    }
    return {
      setAnotherTitle,
    };
  },
};
</script>
