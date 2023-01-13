<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";
import JobWidgets from "./job-widgets.vue";
import FeaturedCompanies from "./featured-companies.vue";
import ApplicationsStatistic from "./applications-statistic.vue";
import RecomendedJobs from "./recomended-jobs.vue";
import RecentApplicants from "./recent-applicants.vue";

export default {
  page: {
    title: "Job Dashboard",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Job Dashboard",
      items: [
        {
          text: "Dashboards",
          href: "/",
        },
        {
          text: "Job Dashboard",
          active: true,
        },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
    JobWidgets,
    FeaturedCompanies,
    ApplicationsStatistic,
    RecomendedJobs,
    RecentApplicants
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />

    <b-row>
      <JobWidgets />
      <FeaturedCompanies />
    </b-row>

    <ApplicationsStatistic />

    <RecomendedJobs />

    <RecentApplicants />
  </Layout>
</template>