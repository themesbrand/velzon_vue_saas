<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import Widget from "./widget.vue";
import SalesForecast from "./forecast.vue";
import DealType from "./deal-type.vue";
import BalanceOverview from "./balance-overview.vue";
import DealStatus from "./deals-status.vue";
import Tasks from "./tasks.vue";
import UpcomingActivity from "./activities.vue";
import ClosingDeals from "./closing-deals.vue";

export default {
  page: {
    title: "CRM",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "CRM",
      items: [
        {
          text: "Dashboards",
          href: "/",
        },
        {
          text: "CRM",
          active: true,
        },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
    Widget,
    SalesForecast,
    DealType,
    BalanceOverview,
    DealStatus,
    Tasks,
    UpcomingActivity,
    ClosingDeals
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    
    <b-row>
      <b-col xl="12">
        <Widget />
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="3" md="6">
        <SalesForecast />
      </b-col>

      <b-col xxl="3" md="6">
        <DealType />
      </b-col>
      <b-col xxl="6">
        <BalanceOverview />
      </b-col>
    </b-row>
    <b-row>
      <b-col xl="7">
          <DealStatus />
      </b-col>
      <b-col xl="5">
          <Tasks />
      </b-col>
    </b-row>
    <b-row>
      <b-col xxl="5">
          <UpcomingActivity />
      </b-col>
      <b-col xxl="7">
          <ClosingDeals />
      </b-col>
    </b-row>
  </Layout>
</template>
