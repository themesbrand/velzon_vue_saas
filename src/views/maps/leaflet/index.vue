<script>
import Layout from "../../../layouts/main";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import Basic from "./basic";
import Boundary from "./boundary";
import Icons from "./icons";
import Geometry from "./geometry";
import Markers from "./markers";

/**
 * Leaflet-map component
 */
export default {
  page: {
    title: "Leaflet map",
    meta: [{ name: "description", content: appConfig.description }]
  },
  components: {
    Layout,
    PageHeader,
    Boundary,
    Icons,
    Basic,
    Geometry,
    Markers
  },
  data() {
    return {
      title: "Leaflet",
      items: [
        {
          text: "Maps",
          href: "/"
        },
        {
          text: "Leaflet",
          active: true
        }
      ]
    };
  }
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Example</b-card-title>
            <Basic class="leaflet-map" />
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Fixed Bounds</b-card-title>
            <Boundary class="leaflet-map" />
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Custom Icon Example</b-card-title>
            <Icons class="leaflet-map" />
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Geometry Example</b-card-title>
            <Geometry class="leaflet-map" />
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
    <b-row>
      <b-col lg="6">
        <b-card no-body>
          <b-card-body>
            <b-card-title class="mb-4">Draggable marker</b-card-title>
            <Markers class="leaflet-map" />
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>