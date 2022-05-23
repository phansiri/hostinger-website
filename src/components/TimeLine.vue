<template>
  <div class="q-pa-lg">
    <q-timeline layout="dense" side="right" color="secondary">
      <q-timeline-entry heading>Timeline</q-timeline-entry>

      <q-timeline-entry
        title="31st Marine Expeditionary Unit"
        subtitle="20 May 2020 - Present"
      >
        <div>
          Billet: Cyberspace Warfare Officer<br />
          Description: Something cool
        </div>
      </q-timeline-entry>

      <q-timeline-entry title="USMC" subtitle="14 July 2003" icon="delete">
        <div>
          Enlisted and jumped into the unknown in hopes of pursuing a better
          life.
        </div>
      </q-timeline-entry>

      <!-- <q-timeline-entry heading>November, 2017</q-timeline-entry>

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        side="left"
        avatar="https://cdn.quasar.dev/img/avatar3.jpg"
      >
        <div>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        side="right"
      >
        <div>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        side="left"
        color="orange"
        icon="done_all"
      >
        <div>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        side="right"
      >
        <div>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </q-timeline-entry>

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        side="left"
      >
        <div>
          Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in
          reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla
          pariatur. Excepteur sint occaecat cupidatat non proident, sunt in
          culpa qui officia deserunt mollit anim id est laborum.
        </div>
      </q-timeline-entry> -->
    </q-timeline>
  </div>
</template>

<script>
// import { ref } from "vue";

export default {
  setup() {
    const timelineItems = [
      {
        title: "testing 1",
        subtitle: "date 1 - present",
        icon: "",
        desc: "something cool",
      },
      {
        title: "testing 2",
        subtitle: "date 2 - date 1",
        desc: "something cool",
      },
      {
        title: "testing 3",
        subtitle: "date 3 - date 2",
        desc: "something cool",
      },
      {
        title: "testing 4",
        subtitle: "date 4 - date 3",
        desc: "something cool",
      },
    ];

    return {
      timelineItems,
    };
  },
};
</script>
