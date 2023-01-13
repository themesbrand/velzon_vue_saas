<script>
import { AlertTriangleIcon } from '@zhuowenli/vue-feather-icons';

import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import Widget from "./widget.vue";
import AudiencesMetrics from "./audiences-metrics.vue";
import AudiencesSessions from "./audiences-sessions.vue";
import Country from "./country.vue";
import Referrals from "./referrals.vue";
import SessionsCounties from "./sessions-countries.vue";
import TopPages from "./top-pages.vue";
import Users from "./users.vue";

export default {
  page: {
    title: "Analytics",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Analytics",
      items: [
        {
          text: "Dashboards",
          href: "/",
        },
        {
          text: "Analytics",
          active: true,
        },
      ],
    };
  },
  components: {
    AlertTriangleIcon,
    Layout,
    PageHeader,
    Widget,
    AudiencesSessions,
    AudiencesMetrics,
    Country,
    Referrals,
    SessionsCounties,
    TopPages,
    Users,
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col xxl="5">
        <b-row>
          <b-col cols="12">
            <b-card no-body>
              <b-card-body class="p-0">
                <b-alert variant="warning" class="border-0 rounded-0 m-0 d-flex align-items-center" show>
                  <alert-triangle-icon class="text-warning me-2 icon-sm"></alert-triangle-icon>
                  <div class="flex-grow-1 text-truncate">
                    Your free trial expired in <b>17</b> days.
                  </div>
                  <div class="flex-shrink-0">
                    <router-link to="/pages/pricing" class="text-reset text-decoration-underline"><b>Upgrade</b>
                    </router-link>
                  </div>
                </b-alert>

                <b-row class="align-items-end">
                  <b-col sm="8">
                    <div class="p-3">
                      <p class="fs-16 lh-base">Upgrade your plan from a <span class="fw-semibold">Free
                          trial</span>, to ‘Premium Plan’ <i class="mdi mdi-arrow-right"></i></p>
                      <div class="mt-3">
                        <router-link to="/pages/pricing" class="btn btn-success">Upgrade Account!</router-link>
                      </div>
                    </div>
                  </b-col>
                  <b-col sm="4">
                    <div class="px-3">
                      <img src="@/assets/images/user-illustarator-2.png" class="img-fluid" alt="">
                    </div>
                  </b-col>
                </b-row>
              </b-card-body>
            </b-card>
          </b-col>
        </b-row>
        <Widget />
      </b-col>
      <b-col xxl="7">
        <b-row class="h-100">
          <b-col xl="6">
            <Country />
          </b-col>
          <b-col xl="6">
            <SessionsCounties />
          </b-col>
        </b-row>
      </b-col>
    </b-row>

    <b-row class="h-100">
      <b-col xl="6">
        <AudiencesMetrics />
      </b-col>
      <b-col xl="6">
        <AudiencesSessions />
      </b-col>
    </b-row>

    <b-row>
      <b-col xl="4">
        <Users />
      </b-col>
      <b-col xl="4" md="6">
        <Referrals />
      </b-col>
      <b-col xl="4" md="6">
        <TopPages />
      </b-col>
    </b-row>
  </Layout>
</template>
