<template>
  <q-layout view="hHh Lpr fFf">
    <!-- hHh lpR fFf -->
    <!-- hHh Lpr fFf -->

    <q-header class="bg-primary text-white">
      <q-toolbar>
        <q-space />
        <q-tabs shrink>
          <q-route-tab to="/" name="Home" label="Home" />
          <q-route-tab to="/about" name="About" label="About" />
          <q-route-tab to="/work" name="Work" label="Work" />
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

    <!-- <q-header class="header-tool">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="leftDrawerOpen = !leftDrawerOpen"
          aria-label="Menu"
          icon="menu"
        />
        <q-toolbar-title>
          <q-item class="absolute-center">Lit</q-item>
        </q-toolbar-title>
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

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      :width="250"
      :breakpoint="600"
    >
      <q-scroll-area
        style="
          height: calc(100% - 150px);
          margin-top: 150px;
          border-right: 1px solid #ddd;
        "
      >
        <q-list
          padding
          v-for="routerLink in routerLinks"
          :key="routerLink.name"
        >
          <div v-if="!toggleMode">
            <q-item :to="routerLink.to" clickable v-ripple>
              <q-item-section avatar>
                <q-icon :name="routerLink.icon" />
              </q-item-section>

              <q-item-section> {{ routerLink.name }} </q-item-section>
            </q-item>
          </div>
          <div v-else>
            <q-item :to="routerLink.to" clickable v-ripple>
              <q-item-section avatar>
                <q-icon :name="routerLink.icon" />
              </q-item-section>
              <q-item-section> {{ routerLink.name }} </q-item-section>
            </q-item>
          </div>
        </q-list>
      </q-scroll-area>

      <q-img
        class="absolute-top"
        src="@/assets/material.png"
        style="height: 150px"
      >
        <div class="absolute-bottom bg-transparent">
          <q-avatar size="56px" class="q-mb-sm">
            <img src="@/assets/lit-avatar.jpeg" />
          </q-avatar>
          <div class="text-weight-bold">Lit Phansiri</div>
          <div>@litphansiri</div>
        </div>
      </q-img>
    </q-drawer> -->

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
        },
        {
          to: "/about",
          icon: "lock",
          name: "about",
        },
        {
          to: "/work",
          icon: "work",
          name: "work",
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
