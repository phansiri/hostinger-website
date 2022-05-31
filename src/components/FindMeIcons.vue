<template>
  <div>
    <div class="row justify-center q-pa-md q-gutter-sm">
      <q-btn
        rounded
        v-for="(link, index) in socialLinks"
        :key="index"
        :color="link.color"
        :target="link.target"
        :href="link.href"
        ><q-icon :name="link.icon" />
        <q-tooltip>{{ link.tooltip }}</q-tooltip>
      </q-btn>
    </div>
  </div>

  <div class="row justify-center q-pa-lg q-gutter-sm">
    <q-btn rounded v-for="(skill, index) in skills" :key="index"
      ><q-icon :name="skill.icon" />
      <q-tooltip>{{ skill.tooltip }}</q-tooltip>
    </q-btn>
  </div>
</template>

<script>
import {
  fabGithub,
  fabLinkedinIn,
  fasPersonMilitaryRifle,
} from "@quasar/extras/fontawesome-v6";

import {
  fabJava,
  fabPython,
  fabJs,
  fabHtml5,
  fabCss3,
  fasDatabase,
  fasCloud,
} from "@quasar/extras/fontawesome-v6";

export default {
  setup() {
    const socialLinks = [
      {
        icon: fabGithub,
        tooltip: "Github",
        color: "black",
        target: "_blank",
        href: "https://github.com/phansiri",
      },
      {
        icon: fasPersonMilitaryRifle,
        tooltip: "United States Marine Corps",
        color: "green",
        target: "_blank",
        href: "https://www.marines.mil/",
      },
      {
        icon: fabLinkedinIn,
        tooltip: "LinkedIn",
        color: "blue",
        target: "_blank",
        href: "https://www.linkedin.com/in/litthideth-phansiri-6b79b098/",
      },
    ];
    const skills = [
      {
        icon: fabJava,
        tooltip: "Java",
      },
      {
        icon: fabPython,
        tooltip: "Python",
      },
      {
        icon: fabJs,
        tooltip: "JavaScript",
      },
      {
        icon: fabHtml5,
        tooltip: "Html5",
      },
      {
        icon: fabCss3,
        tooltip: "Css3",
      },
      {
        icon: fasDatabase,
        tooltip: "SQL Database",
      },
      {
        icon: fasCloud,
        tooltip: "AWS, GCP, and Azure",
      },
    ];

    return {
      socialLinks,
      skills,
    };
  },
  // created() {
  //   this.fabGithub = fabGithub;
  //   this.fabLinkedinIn = fabLinkedinIn;
  //   this.fasPersonMilitaryRifle = fasPersonMilitaryRifle;
  //   this.fabJava = fabJava;
  //   this.fabPython = fabPython;
  //   this.fabJs = fabJs;
  //   this.fabHtml5 = fabHtml5;
  //   this.fabCss3 = fabCss3;
  //   this.fasDatabase = fasDatabase;
  //   this.fasCloud = fasCloud;
  // },
};
</script>
