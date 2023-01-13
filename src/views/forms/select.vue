<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
  page: {
    title: "Select",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Select",
      items: [
        {
          text: "Forms",
          href: "/",
        },
        {
          text: "Select",
          active: true,
        },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
  },
  mounted() {
    const checkbox = document.getElementsByClassName("code-switcher");
    Array.from(checkbox).forEach((check) => {
      check.addEventListener("change", () => {
        const card = check.closest(".card");
        const preview = card.querySelector(".live-preview");
        const code = card.querySelector(".code-view");
        if (check.checked) {
          // do this
          preview.classList.add("d-none");
          code.classList.remove("d-none");
        } else {
          // do that
          preview.classList.remove("d-none");
          code.classList.add("d-none");
        }
      });
    });
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
            <b-card-title class="mb-0 flex-grow-1">Default Select</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="FormSelectDefault" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="FormSelectDefault" />
              </div>
            </div>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use <code>&lt;select&gt;</code> attribute with numerous options to
              show value with choice's option.
            </p>
            <div class="live-preview">
              <b-row>
                <b-col lg="6">
                  <select class="form-select mb-3" aria-label="Default select example">
                    <option selected>Select your Status</option>
                    <option value="1">Declined Payment</option>
                    <option value="2">Delivery Error</option>
                    <option value="3">Wrong Amount</option>
                  </select>
                </b-col>
                <b-col lg="6">
                  <select class="form-select rounded-pill mb-3" aria-label="Default select example">
                    <option selected>Search for services</option>
                    <option value="1">Information Architecture</option>
                    <option value="2">UI/UX Design</option>
                    <option value="3">Back End Development</option>
                  </select>
                </b-col>
                <b-col lg="6">
                  <select class="form-select" aria-label="Disabled select example" disabled>
                    <option selected>Open this select menu (Disabled)</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                </b-col>
              </b-row>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code> &lt;select class=&quot;form-select mb-3&quot; aria-label=&quot;Default select example&quot;&gt;
    &lt;option selected&gt;Open this select menu&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code>

<code> &lt;select class=&quot;form-select rounded-pill mb-3&quot; aria-label=&quot;Default select example&quot;&gt;
    &lt;option selected&gt;Search for services&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;Information Architecture&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;UI/UX Design&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Back End Development&lt;/option&gt;
&lt;/select&gt;</code>

<code>&lt;select class=&quot;form-select&quot; aria-label=&quot;Disabled select example&quot; disabled&gt;
    &lt;option selected&gt;Open this select menu (Disabled)&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Menu Size</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="FormSelectMenuSizing" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="FormSelectMenuSizing" />
              </div>
            </div>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use <code>multiple</code> attribute to select multiple values and
              <code>size="your value"</code> attribute to show a number of
              choice option within a select area.
            </p>
            <div class="live-preview">
              <b-row class="gy-4">
                <b-col lg="6">
                  <select class="form-select" multiple aria-label="multiple select example">
                    <option selected>
                      Open this select menu (multiple select option)
                    </option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                </b-col>
                <b-col lg="6">
                  <select class="form-select" size="3" aria-label="size 3 select example">
                    <option selected>
                      Open this select menu (select menu size)
                    </option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                    <option value="4">Four</option>
                    <option value="5">Five</option>
                  </select>
                </b-col>
              </b-row>
            </div>
            <div class="d-none code-view">
              <pre class="language-markup" style="height: 275px">
<code>&lt;select class=&quot;form-select&quot; multiple aria-label=&quot;multiple select example&quot;&gt;
    &lt;option selected&gt;Open this select menu (multiple select option)&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code>

<code>&lt;select class=&quot;form-select&quot; size=&quot;3&quot; aria-label=&quot;size 3 select example&quot;&gt;
    &lt;option selected&gt;Open this select menu (select menu size)&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
    &lt;option value=&quot;4&quot;&gt;Four&lt;/option&gt;
    &lt;option value=&quot;5&quot;&gt;Five&lt;/option&gt;
&lt;/select&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Select Size</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="FormSelectSizing" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="FormSelectSizing" />
              </div>
            </div>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use <code>form-select-sm</code> class to set small select size and
              <code>form-select-lg</code> class to form-select class to set
              large select size. No such class is required for default select
              size.
            </p>
            <div class="live-preview">
              <b-row class="align-items-center g-3">
                <b-col lg="4">
                  <select class="form-select form-select-sm" aria-label=".form-select-sm example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                </b-col>
                <b-col lg="4">
                  <select class="form-select" aria-label=".form-select-sm example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                </b-col>
                <b-col lg="4">
                  <select class="form-select form-select-lg" aria-label=".form-select-lg example">
                    <option selected>Open this select menu</option>
                    <option value="1">One</option>
                    <option value="2">Two</option>
                    <option value="3">Three</option>
                  </select>
                </b-col>
              </b-row>
            </div>
            <div class="d-none code-view">
              <pre class="language-markup" style="height: 275px"><code>&lt;select class=&quot;form-select form-select-sm  mb-3&quot; aria-label=&quot;.form-select-sm example&quot;&gt;
    &lt;option selected&gt;Open this select menu&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code>

<code>&lt;select class=&quot;form-select mb-3&quot; aria-label=&quot;.form-select-lg example&quot;&gt;
    &lt;option selected&gt;Open this select menu&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code>

<code>&lt;select class=&quot;form-select form-select-lg&quot; aria-label=&quot;.form-select-lg example&quot;&gt;
    &lt;option selected&gt;Open this select menu&lt;/option&gt;
    &lt;option value=&quot;1&quot;&gt;One&lt;/option&gt;
    &lt;option value=&quot;2&quot;&gt;Two&lt;/option&gt;
    &lt;option value=&quot;3&quot;&gt;Three&lt;/option&gt;
&lt;/select&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
