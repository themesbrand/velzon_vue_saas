<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

import "prismjs";
import "prismjs/themes/prism.css";

export default {
  page: {
    title: "Highlight",
    meta: [{
      name: "description",
      content: appConfig.description
    }],
  },
  data() {
    return {
      title: "Highlight",
      items: [{
        text: "Advance UI",
        href: "/",
      },
      {
        text: "Highlight",
        active: true,
      },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <div class="flex-grow-1">
              <b-card-title class="mb-0">HTML Highlight</b-card-title>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              HTML highlight is used to mark or highlight text that is of
              property, relevance, or special interest to an HTML document. here
              is the example shown below.
            </p>

            <div>
              <pre class="live-preview">
<code class="language-markup">&lt;!DOCTYPE html&gt;
&lt;html&gt;
    &lt;head&gt;
        &lt;title&gt;Velzon - Responsive Admin Dashboard Template&lt;/title&gt;
    &lt;/head&gt;
    &lt;body&gt;
        &lt;div&gt;
            &lt;h1&gt;This is a Heading 1&lt;/h1&gt;
            &lt;h2&gt;This is a Heading 2&lt;/h2&gt;
            &lt;h3&gt;This is a Heading 3&lt;/h3&gt;
            &lt;h4&gt;This is a Heading 4&lt;/h4&gt;
        &lt;/div&gt;
        &lt;!-- end div content --&gt;
    &lt;/body&gt;
&lt;/html&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <div class="flex-grow-1">
              <b-card-title class="mb-0">CSS Highlight</b-card-title>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              CSS highlight is used to mark or highlight text that is of
              property, relevance, or special interest to a CSS document. Here
              is the example shown below.
            </p>
            <div>
              <pre class="live-preview">
<code class="language-css">body {
    color: #212529; 
    background-color: #f3f3f9;
    font-family: "Poppins",sans-serif;
}

.example {
    margin: 0;
    color: #74788d; 
}</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <div class="flex-grow-1">
              <b-card-title class="mb-0">Javascript Highlight</b-card-title>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Javascript highlight is used to mark or highlight text that is of
              property, relevance, or special interest to a Javascript document.
              Here is the example shown below.
            </p>
            <div>
              <pre class="live-preview">
<code class="language-js">function myFunction() {
    var divElement = document.getElementById("myDIV");
    if (divElement.style.display === "none") {
      divElement.style.display = "block";
    } else {
      divElement.style.display = "none";
    }
}</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>