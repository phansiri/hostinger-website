<template>
  <div class="q-pa-lg">
    <div class="full-width row wrap justify-center">
      <!-- <div class="col-12 col-md">
        <q-timeline layout="dense" side="right" color="secondary">
          <q-timeline-entry heading>Experience</q-timeline-entry>

          <q-timeline-entry
            title="31st Marine Expeditionary Unit"
            subtitle="May 2020 - Present"
          >
            <div>
              Billet: Cyberspace Warfare Officer<br />
              Description: Pushing the envelope
            </div>
          </q-timeline-entry>
          <q-timeline-entry
            title="Defensive Cyberspace Operations - Internal Defensive Measures Compay, III Marine Information Group, III Marine Expeditionary Force"
            subtitle="Dec 2018 - May 2020"
          >
            <div>
              Billet: Cyberspace Warfare Officer - Executive Officer, Operations
              Officer, and Platoon Commander<br />
              Description: Helped stood up DCO-IDM Company on Okinawa
            </div>
          </q-timeline-entry>
          <q-timeline-entry
            title="University of Washington"
            subtitle="Aug 2013 - Mar 2017"
          >
            <div>
              Billet: Marine Enlisted Commissioning Education Program
              Participant<br />
              Description: Bachelors of Science in Informatics
            </div>
          </q-timeline-entry>

          <q-timeline-entry
            title="Enlisted time throughout the Marine Corps"
            subtitle="2003-2013"
          >
            <div>
              Billet: Aviation Maintenance Data Marine<br />
              Description:
            </div>
          </q-timeline-entry>

          <q-timeline-entry
            title="USMC"
            subtitle="14 July 2003"
            color="blue"
            icon="star"
          >
            <div>
              Enlisted and jumped into the unknown in hopes of pursuing a better
              life.
            </div>
          </q-timeline-entry>
        </q-timeline>
      </div>
      <div class="col-12 col-md">
        <q-timeline layout="dense" side="right" color="secondary">
          <q-timeline-entry heading>Education</q-timeline-entry>
          <q-timeline-entry
            title="31st Marine Expeditionary Unit"
            subtitle="May 2020 - Present"
          >
            <div>
              Billet: Cyberspace Warfare Officer<br />
              Description: Pushing the envelope
            </div>
          </q-timeline-entry>
          <q-timeline-entry
            title="Defensive Cyberspace Operations - Internal Defensive Measures Compay, III Marine Information Group, III Marine Expeditionary Force"
            subtitle="Dec 2018 - May 2020"
          >
            <div>
              Billet: Cyberspace Warfare Officer - Executive Officer, Operations
              Officer, and Platoon Commander<br />
              Description: Helped stood up DCO-IDM Company on Okinawa
            </div>
          </q-timeline-entry>
          <q-timeline-entry
            title="University of Washington"
            subtitle="Aug 2013 - Mar 2017"
          >
            <div>
              Billet: Marine Enlisted Commissioning Education Program
              Participant<br />
              Description: Bachelors of Science in Informatics
            </div>
          </q-timeline-entry>

          <q-timeline-entry
            title="Enlisted time throughout the Marine Corps"
            subtitle="2003-2013"
          >
            <div>
              Billet: Aviation Maintenance Data Marine<br />
              Description:
            </div>
          </q-timeline-entry>

          <q-timeline-entry
            title="USMC"
            subtitle="14 July 2003"
            color="blue"
            icon="star"
          >
            <div>
              Enlisted and jumped into the unknown in hopes of pursuing a better
              life.
            </div>
          </q-timeline-entry>
        </q-timeline>
      </div> -->

      <div class="col-12 col-md">
        <q-timeline color="primary">
          <q-timeline-entry heading>Experience</q-timeline-entry>
          <q-timeline-entry
            v-for="(item, index) in expList"
            :key="index"
            :title="item.title"
            :subtitle="item.subtitle"
            :icon="item.icon"
          >
            Position: {{ item.billet }}
            <br />
            Description: {{ item.desc }}
          </q-timeline-entry>
        </q-timeline>
      </div>

      <div class="col-12 col-md">
        <q-timeline color="primary">
          <q-timeline-entry heading>Education</q-timeline-entry>

          <q-timeline-entry
            v-for="(item, index) in eduList"
            :key="index"
            :title="item.title"
            :subtitle="item.subtitle"
            :icon="item.icon"
          >
            {{ item.billet }}
            <br />
            -{{ item.desc }}
            <br />
            Learn More at: <a href="{{item.url}}">{{ item.urlTitle }}</a>
          </q-timeline-entry>
        </q-timeline>
      </div>
    </div>
  </div>
</template>

<script>
// import { ref } from "vue";
import timeline_exp from "@/components/timeline_exp.json";
import timeline_edu from "@/components/timeline_edu.json";

export default {
  setup() {
    const expList = timeline_exp;
    const eduList = timeline_edu;
    return {
      expList,
      eduList,
    };
  },
};
</script>
