<template>
  <q-layout view="hHh Lpr fFf">
    <!-- hHh lpR fFf -->
    <!-- hHh Lpr fFf -->

    <q-header class="bg-primary text-white">
      <q-toolbar>
        <q-space />
        <q-tabs v-for="link in routerLinks" :key="link.name" shrink>
          <q-route-tab :to="link.to" :name="link.name" :label="link.label" />
        </q-tabs>
        <q-toolbar-title>
          <q-toggle
            class="absolute-right"
            color="blue"
            dark
            v-model="toggleMode"
            icon="mode_night"
          />
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer reveal>
      <q-toolbar>
        <footer-section></footer-section>
      </q-toolbar>
    </q-footer>

    <!-- place QPageScroller at end of page -->
    <q-page-scroller
      position="bottom-right"
      :scroll-offset="150"
      :offset="[18, 18]"
    >
      <q-btn fab icon="keyboard_arrow_up" color="accent" />
    </q-page-scroller>
  </q-layout>
</template>

<script>
import { ref } from "vue";
import { useQuasar } from "quasar";
import FooterSection from "@/components/FooterSection.vue";

export default {
  name: "LayoutDefault",
  components: {
    FooterSection,
  },
  data() {
    return {
      toggleMode: true,
      routerLinks: [
        {
          to: "/",
          icon: "home",
          name: "home",
          label: "Home",
        },
        {
          to: "/about",
          icon: "lock",
          name: "about",
          label: "About",
        },
        {
          to: "/work",
          icon: "work",
          name: "work",
          label: "Work",
        },
      ],
      $q: useQuasar().dark.set(true),
    };
  },
  watch: {
    toggleMode() {
      this.$q.dark.set(this.toggleMode);
    },
  },
  setup() {
    return {
      leftDrawerOpen: ref(false),
    };
  },
};
</script>

<style lang="scss" scoped>
.header-tool {
  background-color: #1a2238;
  opacity: 0.92;
}
</style>
