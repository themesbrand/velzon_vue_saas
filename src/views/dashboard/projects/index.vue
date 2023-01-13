<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import Widgets from "./widget.vue";
import Schedules from "./schedule.vue";
import Project from "./projects.vue";
import Task from "./tasks.vue";
import Member from "./members.vue";
import Chat from "./chat.vue";
import Status from "./status.vue";
import ActiveProjects from "./active-projects.vue";

export default {
  page: {
    title: "Projects",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Projects",
      items: [
        {
          text: "Dashboards",
          href: "/",
        },
        {
          text: "Projects",
          active: true,
        },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
    Widgets,
    Schedules,
    Project,
    Task,
    Member,
    Chat,
    ActiveProjects,
    Status
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />

    <b-row class="project-wrapper">
      <b-col xxl="8">
        <b-row>
          <Widgets />
          <b-col xl="4">
          </b-col>
          <b-col xl="4">
          </b-col>
        </b-row>
        <b-row>
          <b-col xl="12">
            <Project />
          </b-col>
        </b-row>
      </b-col>

      <b-col xxl="4">
        <Schedules />
      </b-col>
    </b-row>

    <b-row>
      <b-col xl="7">
        <ActiveProjects />
      </b-col>
      <b-col xl="5">
        <Task />
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="4">
        <Member />
      </b-col>
      <b-col xxl="4" lg="6">
        <Chat />
      </b-col>
      <b-col xxl="4" lg="6">
        <Status />
      </b-col>
    </b-row>

  </Layout>
</template>