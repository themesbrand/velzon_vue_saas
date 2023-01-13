<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

import { icons } from "./data-material";

export default {
  page: {
    title: "Material Design",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      icons: icons,
      title: "Material Design",
      items: [
        {
          text: "Icons",
          href: "/",
        },
        {
          text: "Material Design",
          active: true,
        },
      ],
      iconsCount: 0,
      newIconsCount: 0,
    };
  },
  components: {
    Layout,
    PageHeader,
  },
  mounted() {
    this.icons.push({ name: "blank", hex: "f68c" });

    this.icons.forEach((icon) => {
      var item = this.getIconItem(icon, this.isNew(icon));
      document.getElementById("icons").appendChild(item);
      if (this.isNew(icon)) {
        var newItem = this.getIconItem(icon, false);
        document.getElementById("newIcons").appendChild(newItem);
        this.newIconsCount++;
      }
      this.iconsCount++;
    });
  },
  methods: {
    isNew(icon) {
      return icon.version === "5.0.45";
    },

    getIconItem(icon) {
      var div = document.createElement("div"),
        i = document.createElement("i");
      div.className = "col-xl-3 col-lg-4 col-sm-6";
      i.className = "mdi mdi-" + icon.name;
      div.appendChild(i);
      var span = document.createElement("span");
      span.appendChild(document.createTextNode("mdi-" + icon.name));
      div.appendChild(span);
      return div;
    },

    isDeprecated(icon) {
      return typeof icon.deprecated == "undefined" ? false : icon.deprecated;
    },
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row class="icon-demo-content">
      <b-col cols="12">
        <b-card no-body>
          <b-card-body>
            <b-card-title>New Icons</b-card-title>
            <p class="card-title-desc mb-2">
              Use
              <code>&lt;i class="mdi mdi-*-*"&gt;&lt;/i&gt;</code> class.<b-badge variant="success">v 6.5.95</b-badge>.
            </p>

            <b-row class="icon-demo-content" id="newIcons"></b-row>
          </b-card-body>
        </b-card>

        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">All Icons</b-card-title>
            <b-row class="icon-demo-content" id="icons"></b-row>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col cols="12">
        <b-card no-body>
          <b-card-body>
            <b-card-title>Size</b-card-title>

            <b-row class="icon-demo-content">
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-18px mdi-account"></i> mdi-18px
              </b-col>

              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-24px mdi-account"></i> mdi-24px
              </b-col>

              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-36px mdi-account"></i> mdi-36px
              </b-col>

              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-48px mdi-account"></i> mdi-48px
              </b-col>
            </b-row>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col cols="12">
        <b-card no-body>
          <b-card-body>
            <b-card-title>Rotate</b-card-title>

            <b-row class="icon-demo-content">
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-45 mdi-account"></i> mdi-rotate-45
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-90 mdi-account"></i> mdi-rotate-90
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-135 mdi-account"></i> mdi-rotate-135
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-180 mdi-account"></i> mdi-rotate-180
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-225 mdi-account"></i> mdi-rotate-225
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-270 mdi-account"></i> mdi-rotate-270
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-rotate-315 mdi-account"></i> mdi-rotate-315
              </b-col>
            </b-row>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col cols="12">
        <b-card no-body>
          <b-card-body>
            <b-card-title>Spin</b-card-title>

            <b-row class="icon-demo-content">
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-spin mdi-loading"></i> mdi-spin
              </b-col>
              <b-col xl="3" lg="4" sm="6">
                <i class="mdi mdi-spin mdi-star"></i> mdi-spin
              </b-col>
            </b-row>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
