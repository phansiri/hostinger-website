<template>
  <q-layout view="hHh lpR fFf">
    <q-header reveal elevated class="glossy">
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
          <q-item>Lit Phansiri</q-item>
        </q-toolbar-title>
        <q-toolbar-title>
          <q-toggle
            class="absolute-right"
            color="blue"
            dark
            v-model="toggleMode"
            icon="mode_night"
          />
          <!-- <q-btn @click="toggleDark">Change</q-btn> -->
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
          <q-item :to="routerLink.to" clickable v-ripple>
            <q-item-section avatar>
              <q-icon :name="routerLink.icon" />
            </q-item-section>

            <q-item-section> {{ routerLink.name }} </q-item-section>
          </q-item>
        </q-list>
      </q-scroll-area>

      <q-img
        class="absolute-top"
        src="@/assets/material.png"
        style="height: 150px"
      >
        <div class="absolute-bottom bg-transparent">
          <q-avatar size="56px" class="q-mb-sm">
            <img src="@/assets/boy-avatar.png" />
          </q-avatar>
          <div class="text-weight-bold">Lit Phansiri</div>
          <div>@litphansiri</div>
        </div>
      </q-img>
    </q-drawer>

    <q-footer reveal elevated class="glossy">
      <q-toolbar>
        <footer-section></footer-section>
      </q-toolbar>
    </q-footer>

    <q-page-container>
      <router-view />
      <!-- place QPageScroller at end of page -->
      <q-page-scroller
        position="bottom-right"
        :scroll-offset="150"
        :offset="[18, 18]"
      >
        <q-btn fab icon="keyboard_arrow_up" color="accent" />
      </q-page-scroller>
    </q-page-container>
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
      toggleMode: false,
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
      $q: useQuasar(),
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
