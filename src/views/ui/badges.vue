<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";

import "prismjs";
import "prismjs/themes/prism.css";

export default {
  data() {
    return {
      title: "Badges",
      items: [{
        text: "Base UI",
        href: "/",
      },
      {
        text: "Badges",
        active: true,
      },
      ],
    };
  },
  name: "Badges",
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
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Default Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="default" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="default" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>badge</code> selector to set a default badge.
            </p>
            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge variant="primary" class="bg-primary">Primary</b-badge>
                <b-badge class="bg-secondary">Secondary</b-badge>
                <b-badge class="bg-success">Success</b-badge>
                <b-badge class="bg-info">Info</b-badge>
                <b-badge class="bg-warning">Warning</b-badge>
                <b-badge class="bg-danger">Danger</b-badge>
                <b-badge class="bg-dark">Dark</b-badge>
                <b-badge class="bg-light text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;b-badge variant=&quot;primary&quot;&gt;Primary&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;secondary&quot;&gt;Secondary&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;success&quot;&gt;Success&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;info&quot;&gt;Info&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;warning&quot;&gt;Warning&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;danger&quot;&gt;Danger&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;dark&quot;&gt;Dark&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;light&quot;&gt;Light&lt;/b-badge&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Soft Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="soft-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="soft-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>badge-soft-</code> class with the below-mentioned variation
              to create a softer badge.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge variant="soft-primary" class="badge-soft-primary">Primary</b-badge>
                <b-badge variant="soft-secondary" class="badge-soft-secondary">Secondary</b-badge>
                <b-badge variant="soft-success" class="badge-soft-success">Success</b-badge>
                <b-badge variant="soft-info" class="badge-soft-info">Info</b-badge>
                <b-badge variant="soft-warning" class="badge-soft-warning">Warning</b-badge>
                <b-badge variant="soft-danger" class="badge-soft-danger">Danger</b-badge>
                <b-badge variant="soft-dark" class="badge-soft-dark">Dark</b-badge>
                <b-badge variant="soft-light" class="badge-soft-light text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;span class=&quot;badge badge-soft-primary&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-secondary&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-success&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-info&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-warning&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-danger&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-dark&quot;&gt;Dark&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-light&quot;&gt;Light&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Outline Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="outline-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="outline-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>badge-outline-</code> class with the below-mentioned
              variation to create a badge with the outline.
            </p>
            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-link href="#" class="badge badge-outline-primary">Primary</b-link>
                <b-badge variant="outline-secondary" class="badge-outline-secondary">Secondary</b-badge>
                <b-badge variant="outline-success" class="badge-outline-success">Success</b-badge>
                <b-badge variant="outline-info" class="badge-outline-info">Info</b-badge>
                <b-badge variant="outline-warning" class="badge-outline-warning">Warning</b-badge>
                <b-badge variant="outline-danger" class="badge-outline-danger">Danger</b-badge>
                <b-badge variant="outline-dark" class="badge-outline-dark">Dark</b-badge>
                <b-badge variant="outline-light" class="badge-outline-light text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;span class=&quot;badge badge-outline-primary&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-secondary&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-success&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-info&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-warning&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-danger&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-dark&quot;&gt;Dark&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-outline-light&quot;&gt;Light&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Rounded Pill Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="pill-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="pill-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>rounded-pill</code> class to make badges more rounded with a
              larger border-radius.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge pill variant="primary">Primary</b-badge>
                <b-badge pill variant="secondary">Secondary</b-badge>
                <b-badge pill variant="success">Success</b-badge>
                <b-badge pill class="bg-info">Info</b-badge>
                <b-badge pill class="bg-warning">Warning</b-badge>
                <b-badge pill variant="danger">Danger</b-badge>
                <b-badge pill variant="dark">Dark</b-badge>
                <b-badge pill variant="light" class="text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;b-badge variant=&quot;primary&quot; pill &gt;Primary&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;secondary&quot; pill &gt;Secondary&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;success&quot; pill &gt;Success&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;info&quot; pill &gt;Info&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;warning&quot; pill &gt;Warning&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;danger&quot; pill &gt;Danger&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;dark&quot; pill &gt;Dark&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;light&quot; pill &gt;Light&lt;/b-badge&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Rounded Pill Badges with soft effect</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="rounded-pill-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="rounded-pill-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>rounded-pill badge-soft-</code> class with the
              below-mentioned variation to create a badge more rounded with a
              soft background.
            </p>
            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge pill variant="soft-primary" class="badge-soft-primary">Primary</b-badge>
                <b-badge pill variant="soft-secondary" class="badge-soft-secondary">Secondary</b-badge>
                <b-badge pill variant="soft-success" class="badge-soft-success">Success</b-badge>
                <b-badge pill variant="soft-info" class="badge-soft-info">Info</b-badge>
                <b-badge pill variant="soft-warning" class="badge-soft-warning">Warning</b-badge>
                <b-badge pill variant="soft-danger" class="badge-soft-danger">Danger</b-badge>
                <b-badge pill variant="soft-dark" class="badge-soft-dark">Dark</b-badge>
                <b-badge pill variant="soft-light" class="badge-soft-light text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;span class=&quot;badge rounded-pill badge-soft-primary&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-secondary&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-success&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-info&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-warning&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-danger&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-dark&quot;&gt;Dark&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-soft-light&quot;&gt;Light&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Soft Border Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="badges-soft-border" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="badges-soft-border" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>badge-border</code> and <code>badge-soft-</code> with below
              mentioned modifier classes to make badges with border & soft
              backgorund.
            </p>
            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge variant="soft-primary" class="badge-soft-primary badge-border">Primary</b-badge>
                <b-badge variant="soft-secondary" class="badge-soft-secondary badge-border">Secondary</b-badge>
                <b-badge variant="soft-success" class="badge-soft-success badge-border">Success</b-badge>
                <b-badge variant="soft-danger" class="badge-soft-danger badge-border">Danger</b-badge>
                <b-badge variant="soft-warning" class="badge-soft-warning badge-border">Warning</b-badge>
                <b-badge variant="soft-info" class="badge-soft-info badge-border">Info</b-badge>
                <b-badge variant="soft-dark" class="badge-soft-dark badge-border">Dark</b-badge>
                <b-badge variant="soft-light" class="badge-soft-light badge-border text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;span class=&quot;badge badge-soft-primary badge-border&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-secondary badge-border&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-success badge-border&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-info badge-border&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-warning badge-border&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-danger badge-border&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-dark badge-border&quot;&gt;Dark&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-soft-light badge-border&quot;&gt;Light&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Outline Pill Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="outline-pill-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="outline-pill-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>rounded-pill badge-outline-</code> class with the
              below-mentioned variation to create a outline Pill badge.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge pill variant="outline-primary" class="badge-outline-primary">Primary</b-badge>
                <b-badge pill variant="outline-secondary" class="badge-outline-secondary">Secondary</b-badge>
                <b-badge pill variant="outline-success" class="badge-outline-success">Success</b-badge>
                <b-badge pill variant="outline-info" class="badge-outline-info">Info</b-badge>
                <b-badge pill variant="outline-warning" class="badge-outline-warning">Warning</b-badge>
                <b-badge pill variant="outline-danger" class="badge-outline-danger">Danger</b-badge>
                <b-badge pill variant="outline-dark" class="badge-outline-dark">Dark</b-badge>
                <b-badge pill variant="outline-light" class="badge-outline-light text-dark">Light</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;span class=&quot;badge rounded-pill badge-outline-primary&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-secondary&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-success&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-info&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-warning&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-danger&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-dark&quot;&gt;Dark&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge rounded-pill badge-outline-light&quot;&gt;Light&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Label Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="badges-label" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="badges-label" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the
              <code>badge-label</code> class to create a badge with the label.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge variant="primary" class="badge-label">
                  <i class="mdi mdi-circle-medium"></i>
                  Primary
                </b-badge>
                <b-badge variant="secondary" class="badge-label">
                  <i class="mdi mdi-circle-medium"></i>
                  Secondary
                </b-badge>
                <b-badge variant="success" class="badge-label">
                  <i class="mdi mdi-circle-medium"></i>
                  Success
                </b-badge>
                <b-badge variant="danger" class="badge-label">
                  <i class="mdi mdi-circle-medium"></i>
                  Danger
                </b-badge>
                <b-badge class="badge-label bg-warning">
                  <i class="mdi mdi-circle-medium"></i>
                  Warning
                </b-badge>
                <b-badge class="badge-label bg-info">
                  <i class="mdi mdi-circle-medium"></i> Info
                </b-badge>

                <b-badge variant="dark" class="badge-label">
                  <i class="mdi mdi-circle-medium"></i> Dark
                </b-badge>

                <b-badge variant="light" class="badge-label text-dark">
                  <i class="mdi mdi-circle-medium"></i> Light
                </b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;b-badge variant=&quot;primary&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Primary&lt;/b-badge&gt;</code>

<code>&lt;b-badge variant=&quot;secondary&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Secondary&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;success&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Success&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;danger&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Danger&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;warning&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Warning&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;info&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Info&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;dark&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Dark&lt;/b-badge&gt;</code>
 
<code>&lt;b-badge variant=&quot;light&quot; class=&quot;badge-label&quot; &gt;&lt;i class=&quot;mdi mdi-circle-medium&quot;&gt;&lt;/i&gt; Light&lt;/b-badge&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>
    </b-row>
    <b-row>
      <b-col xxl="12">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Gradient Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="badges-gradient" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="badges-gradient">
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the <code>badge-gradient-*</code> class to create a gradient styled badge.
            </p>
            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-badge class="badge-gradient-primary">Primary</b-badge>
                <b-badge class="badge-gradient-secondary">Secondary</b-badge>
                <b-badge class="badge-gradient-success">Success</b-badge>
                <b-badge class="badge-gradient-danger">Danger</b-badge>
                <b-badge class="badge-gradient-warning">Warning</b-badge>
                <b-badge class="badge-gradient-info">Info</b-badge>
                <b-badge class="badge-gradient-dark">Dark</b-badge>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px;">
<code>&lt;span class=&quot;badge badge-gradient-primary&quot;&gt;Primary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-secondary&quot;&gt;Secondary&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-success&quot;&gt;Success&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-danger&quot;&gt;Danger&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-warning&quot;&gt;Warning&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-info&quot;&gt;Info&lt;/span&gt;</code>

<code>&lt;span class=&quot;badge badge-gradient-dark&quot;&gt;Dark&lt;/span&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Button Position Badges</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="button-position-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="button-position-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use the below utilities to modify a badge and position it in the
              corner of a link or button.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-3">
                <b-button type="button" variant="primary" class="position-relative">
                  Mails
                  <span class="
                      position-absolute
                      top-0
                      start-100
                      translate-middle
                      badge
                      rounded-pill
                      bg-success
                    ">
                    +99
                    <span class="visually-hidden">unread messages</span>
                  </span>
                </b-button>

                <b-button type="button" variant="light" class="position-relative">
                  Alerts
                  <span class="
                      position-absolute
                      top-0
                      start-100
                      translate-middle
                      badge
                      border border-light
                      rounded-circle
                      bg-danger
                      p-1
                    ">
                    <span class="visually-hidden">unread messages</span>
                  </span>
                </b-button>

                <b-button type="button" variant="primary" class="
                    position-relative
                    p-0
                    avatar-xs
                    rounded
                  ">
                  <span class="avatar-title bg-transparent">
                    <i class="bx bxs-envelope"></i>
                  </span>
                  <span class="
                      position-absolute
                      top-0
                      start-100
                      translate-middle
                      badge
                      border border-light
                      rounded-circle
                      bg-danger
                      p-1
                    ">
                    <span class="visually-hidden">unread messages</span>
                  </span>
                </b-button>

                <b-button type="button" variant="light" class="
                    position-relative
                    p-0
                    avatar-xs
                    rounded-circle
                  ">
                  <span class="avatar-title bg-transparent text-reset">
                    <i class="bx bxs-bell"></i>
                  </span>
                </b-button>

                <b-button type="button" variant="light" class="
                    position-relative
                    p-0
                    avatar-xs
                    rounded-circle
                  ">
                  <span class="avatar-title bg-transparent text-reset">
                    <i class="bx bx-menu"></i>
                  </span>
                  <span class="
                      position-absolute
                      top-0
                      start-100
                      translate-middle
                      badge
                      border border-light
                      rounded-circle
                      bg-success
                      p-1
                    ">
                    <span class="visually-hidden">unread messages</span>
                  </span>
                </b-button>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="height: 200px">
<code>&lt;b-button variant=&quot;primary&quot; class=&quot;y position-relative&quot;&gt;
    Mails &lt;span class=&quot;position-absolute top-0 start-100 translate-middle badge rounded-pill bg-success&quot;&gt;+99 &lt;span class=&quot;visually-hidden&quot;&gt;unread messages&lt;/span&gt;&lt;/span&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;light&quot; class=&quot;position-relative&quot;&gt;
    Alerts &lt;span class=&quot;position-absolute top-0 start-100 translate-middle badge border border-light rounded-circle bg-danger p-1&quot;&gt;&lt;span class=&quot;visually-hidden&quot;&gt;unread messages&lt;/span&gt;&lt;/span&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;primary&quot; class=&quot;y position-relative p-0 avatar-xs rounded&quot;&gt;
    &lt;span class=&quot;avatar-title bg-transparent&quot;&gt;
        &lt;i class=&quot;bx bxs-envelope&quot;&gt;&lt;/i&gt;
    &lt;/span&gt;
    &lt;span class=&quot;position-absolute top-0 start-100 translate-middle badge border border-light rounded-circle bg-danger p-1&quot;&gt;&lt;span class=&quot;visually-hidden&quot;&gt;unread messages&lt;/span&gt;&lt;/span&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;light&quot; class=&quot;position-relative p-0 avatar-xs rounded-circle&quot;&gt;
    &lt;span class=&quot;avatar-title bg-transparent text-reset&quot;&gt;
        &lt;i class=&quot;bx bxs-bell&quot;&gt;&lt;/i&gt;
    &lt;/span&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;light&quot; class=&quot;position-relative p-0 avatar-xs rounded-circle&quot;&gt;
    &lt;span class=&quot;avatar-title bg-transparent text-reset&quot;&gt;
        &lt;i class=&quot;bx bx-menu&quot;&gt;&lt;/i&gt;
    &lt;/span&gt;
    &lt;span class=&quot;position-absolute top-0 start-100 translate-middle badge border border-light rounded-circle bg-success p-1&quot;&gt;&lt;span class=&quot;visually-hidden&quot;&gt;unread messages&lt;/span&gt;&lt;/span&gt;
&lt;/b-button&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>

        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Badges With Button</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="button-badge" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="button-badge" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Badges can be used as part of buttons to provide a counter.
            </p>

            <div class="live-preview">
              <div class="d-flex flex-wrap gap-2">
                <b-button variant="primary" type="button">
                  Notifications
                  <b-badge variant="success" class="ms-1">4</b-badge>
                </b-button>
                <b-button variant="success" type="button">
                  Messages
                  <b-badge variant="danger" class="ms-1">2</b-badge>
                </b-button>
                <b-button variant="outline-secondary" type="button">
                  Draft
                  <b-badge variant="success" class="ms-1">2</b-badge>
                </b-button>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;b-button variant=&quot;primary&quot; &gt;
    Notifications &lt;b-badge variant=&quot;success&quot; class=&quot;ms-1&quot;&gt;4&lt;/b-badge&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;success&quot; &gt;
    Messages &lt;b-badge variant=&quot;danger quot;;mclass=quot;;s-1&quot;&gt;2&lt;/b-badge&gt;
&lt;/b-button&gt;</code>

<code>&lt;b-button variant=&quot;outline-secondary&quot;&gt;
    Draft &lt;b-badge variant=&quot;success&quot; class=&quot;ms-1&quot;&gt;2&lt;/b-badge&gt;
&lt;/b-button&gt;
</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Badges with Heading</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="heading-badges" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="heading-badges" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Example of the badge used in the HTML Heading.
            </p>

            <div class="live-preview">
              <h1>
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h1>
              <h2>
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h2>
              <h3>
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h3>
              <h4>
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h4>
              <h5>
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h5>
              <h6 class="mb-0">
                Example heading
                <b-badge variant="secondary">New</b-badge>
              </h6>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;h1&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h1&gt;</code>

<code>&lt;h2&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h2&gt;</code>

<code>&lt;h3&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h3&gt;</code>

<code>&lt;h4&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h4&gt;</code>

<code>&lt;h5&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h5&gt;</code>

<code>&lt;h6&gt;Example heading &lt;b-badge variant=&quot;secondary&quot;&gt;New&lt;/b-badge&gt;&lt;/h6&gt;</code></pre>
            </div>
          </b-card-body>

        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>