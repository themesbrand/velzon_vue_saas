<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";

import "prismjs";
import "prismjs/themes/prism.css";

export default {
  data() {
    return {
      title: "Progress",
      items: [
        {
          text: "Base UI",
          href: "/",
        },
        {
          text: "Progress",
          active: true,
        },
      ],
    };
  },
  name: "Progress",
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
            <b-card-title class="mb-0 flex-grow-1">Default Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="default" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="default" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>b-progress</code> tag to show default progress.
            </p>

            <div class="live-preview">
              <b-progress variant="primary" class="mb-4" :value="0" />

              <b-progress variant="primary" class="mb-4" :value="25" />

              <b-progress variant="primary" class="mb-4" :value="50" />

              <b-progress variant="primary" class="mb-4" :value="75" />

              <b-progress variant="primary" :value="100" />
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="max-height:  275px">
<code>&lt;!-- Base Examples --&gt;
    &lt;b-progress :value=&quot;0&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;25&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;50&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;75&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;
    
    &lt;b-progress :value=&quot;100&quot;&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1"> Progress with background color </b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="background-show-code" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="background-show-code" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>variant=""</code> in progress bar class with the
              below-mentioned color variation to set the background color
              progress bar.
            </p>

            <div class="live-preview">
              <b-progress :value="15" variant="primary" class="mb-4"></b-progress>

              <b-progress :value="25" variant="success" class="mb-4"></b-progress>

              <b-progress :value="50" variant="info" class="mb-4"></b-progress>

              <b-progress :value="75" variant="warning" class="mb-4"></b-progress>

              <b-progress :value="100" variant="danger"></b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="max-height:  275px">
<code>&lt;!-- Backgrounds --&gt;
    &lt;b-progress :value=&quot;15&quot; variant=&quot;primary&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;25&quot; variant=&quot;success&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;50&quot; variant=&quot;info&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;75&quot; variant=&quot;warning&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;100&quot; variant=&quot;danger&quot; class=&quot;mb-4&quot;&gt;&lt;/b-progress&gt;

    </code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Progress with Label</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="labelprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="labelprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Add labels to your progress bars by placing text within the
              progress-bar.
            </p>

            <div class="live-preview">
              <b-progress :value="25" variant="primary" class="mb-4" show-value></b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;!-- Labels Example --&gt;
    &lt;b-progress :value=&quot;25&quot; variant=&quot;primary&quot; class=&quot;mb-4&quot; show-value &gt;&lt;/b-progress&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Multiple Bars</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="multibarprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="multibarprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>bg-</code> class to progress bar class with the
              below-mentioned color to change the appearance of individual
              progress bars.
            </p>

            <div class="live-preview">
              <b-progress>
                <b-progress-bar :value="15" variant="primary" />
                <b-progress-bar :value="30" variant="success" />
                <b-progress-bar :value="20" variant="info" />
              </b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;!-- Multiple Bars --&gt;
&lt;b-progress&gt;
    &lt;b-progress-bar :value=&quot;15&quot; variant=&quot;primary&quot; /&gt;
    &lt;b-progress-bar :value=&quot;30&quot; variant=&quot;success&quot; /&gt;
    &lt;b-progress-bar :value=&quot;20&quot; variant=&quot;info&quot; /&gt;
&lt;/b-progress&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Height</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="heightprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="heightprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>progress-sm</code>, <code>progress-lg</code>, or
              <code>progress-xl</code> class to set the different heights of
              progress.
            </p>
            <div class="live-preview">
              <div class="mb-4">
                <h5 class="fs-13">Small Progress</h5>
                <b-progress :value="25" class="progress-sm" variant="primary" />
              </div>
              <div class="mb-4">
                <h5 class="fs-13">Default Progress</h5>
                <b-progress :value="40" variant="success" />
              </div>
              <div class="mb-4">
                <h5 class="fs-13">Large Progress</h5>
                <b-progress :value="50" class="progress-lg" variant="warning" />
              </div>
              <div>
                <h5 class="fs-13">Extra Large Progress</h5>
                <b-progress :value="70" class="progress-xl" variant="danger" />
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="max-height:  275px">
<code>&lt;!-- Prgress sm --&gt;
    &lt;b-progress :value=&quot;25&quot; class=&quot;progress-sm&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;40&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;50&quot; class=&quot;progress-lg&quot; variant=&quot;warning&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress :value=&quot;70&quot; class=&quot;progress-xl&quot; variant=&quot;danger&quot;&gt;&lt;/b-progress&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Striped Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="stripesprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="stripesprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>progress-bar-striped</code> class to add strip to the
              progress.
            </p>
            <div class="live-preview">
              <b-progress striped :value="25" class="mb-4" variant="primary" />
              <b-progress striped :value="40" variant="success" />
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;!-- Striped Prgress --&gt;
    &lt;b-progress striped :value=&quot;25&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;

    &lt;b-progress striped :value=&quot;40&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>

        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1"> Animated Striped Progress </b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="animationstripesprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="animationstripesprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>progress-bar-striped progress-bar-animated</code> class to
              add strip with animation to the progress.
            </p>

            <div class="live-preview">
              <b-progress striped animated :value="75" variant="primary" />
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;b-progress striped animated :value=&quot;75&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Gradient Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="gradientprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="gradientprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>bg-gradient</code> class to show gradient progress bar.
            </p>

            <div class="live-preview">

              <b-progress class="mb-4">
                <b-progress-bar :value="15" variant="primary" class="bg-gradient" />
              </b-progress>

              <b-progress class="mb-4">
                <b-progress-bar :value="25" variant="success" class="bg-gradient" />
              </b-progress>

              <b-progress class="mb-4">
                <b-progress-bar :value="50" variant="info" class="bg-gradient" />
              </b-progress>

              <b-progress class="mb-4">
                <b-progress-bar :value="75" variant="warning" class="bg-gradient" />
              </b-progress>

              <b-progress>
                <b-progress-bar :value="100" variant="danger" class="bg-gradient" />
              </b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>
&lt;b-progress :value=&quot;15&quot;  class=&quot;bg-gradient&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress :value=&quot;25&quot;  class=&quot;bg-gradient&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress :value=&quot;50&quot;  class=&quot;bg-gradient&quot; variant=&quot;info&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress :value=&quot;75&quot;  class=&quot;bg-gradient&quot; variant=&quot;warning&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress :value=&quot;100&quot; class=&quot;bg-gradient&quot;  variant=&quot;danger&quot;&gt;&lt;/b-progress&gt;
    </code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Animated Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="animatedprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="animatedprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>animated-progess</code> class to show progress with
              animation.
            </p>
            <div class="live-preview">

              <b-progress class="animated-progress mb-4">
                <b-progress-bar :value="15" variant="primary" />
              </b-progress>

              <b-progress class="animated-progress mb-4">
                <b-progress-bar :value="25" variant="success" />
              </b-progress>

              <b-progress class="animated-progress mb-4">
                <b-progress-bar :value="50" variant="info" />
              </b-progress>

              <b-progress class="animated-progress mb-4">
                <b-progress-bar :value="75" variant="warning" />
              </b-progress>

              <b-progress class="animated-progress">
                <b-progress-bar :value="100" variant="danger" />
              </b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>
&lt;b-progress animated :value=&quot;15&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;25&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;50&quot; variant=&quot;info&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;75&quot; variant=&quot;warning&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;100&quot; variant=&quot;danger&quot;&gt;&lt;/b-progress&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Custom Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="customprogress-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="customprogress-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>animated-progess custom-progess</code> class to show custom
              progress with animation.
            </p>
            <div class="live-preview">

              <b-progress class="animated-progress custom-progress mb-4">
                <b-progress-bar :value="15" variant="primary" />
              </b-progress>

              <b-progress class="animated-progress custom-progress mb-4">
                <b-progress-bar :value="25" variant="success" />
              </b-progress>

              <b-progress class="animated-progress custom-progress mb-4">
                <b-progress-bar :value="50" variant="info" />
              </b-progress>

              <b-progress class="animated-progress custom-progress mb-4">
                <b-progress-bar :value="75" variant="warning" />
              </b-progress>

              <b-progress class="animated-progress custom-progress mb-4">
                <b-progress-bar :value="100" variant="danger" />
              </b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>
&lt;b-progress animated :value=&quot;15&quot; class=&quot;custom-progress mb-4&quot; variant=&quot;primary&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;25&quot; class=&quot;custom-progress mb-4&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;50&quot; class=&quot;custom-progress mb-4&quot; variant=&quot;info&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;75&quot; class=&quot;custom-progress mb-4&quot; variant=&quot;warning&quot;&gt;&lt;/b-progress&gt;

&lt;b-progress animated :value=&quot;100&quot; class=&quot;custom-progress&quot; variant=&quot;danger&quot;&gt;&lt;/b-progress&gt;
</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1"> Custom Progress with Label </b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="customprogresslabel-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="customprogresslabel-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>animated-progess custom-progess progress-label</code> class
              to show custom progress with animation and label.
            </p>
            <div class="live-preview">
              <div class="d-flex align-items-center pb-2 mt-4">
                <div class="flex-shrink-0 me-3">
                  <div class="avatar-xs">
                    <div class="
                        avatar-title
                        bg-light
                        rounded-circle
                        text-muted
                        fs-16
                      ">
                      <i class="mdi mdi-facebook"></i>
                    </div>
                  </div>
                </div>
                <div class="flex-grow-1">
                  <b-progress class="animated-progress custom-progress progress-label">
                    <b-progress-bar :value="15" variant="primary">
                    <div class="label">15%</div>
                    </b-progress-bar>
                  </b-progress>
                </div>
              </div>

              <div class="d-flex align-items-center py-2">
                <div class="flex-shrink-0 me-3">
                  <div class="avatar-xs">
                    <div class="
                        avatar-title
                        bg-light
                        rounded-circle
                        text-muted
                        fs-16
                      ">
                      <i class="mdi mdi-twitter"></i>
                    </div>
                  </div>
                </div>
                <div class="flex-grow-1">

                  <b-progress class="animated-progress custom-progress progress-label">
                    <b-progress-bar :value="25" variant="success">
                    <div class="label">25%</div>
                    </b-progress-bar>
                  </b-progress>
                </div>
              </div>

              <div class="d-flex align-items-center py-2">
                <div class="flex-shrink-0 me-3">
                  <div class="avatar-xs">
                    <div class="
                        avatar-title
                        bg-light
                        rounded-circle
                        text-muted
                        fs-16
                      ">
                      <i class="mdi mdi-github"></i>
                    </div>
                  </div>
                </div>
                <div class="flex-grow-1">
                  <b-progress class="animated-progress custom-progress progress-label">
                    <b-progress-bar :value="30" variant="info">
                    <div class="label">30%</div>
                    </b-progress-bar>
                  </b-progress>
                </div>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="max-height:  275px">
<code>&lt;div class=&quot;d-flex align-items-center pb-2&quot;&gt;
    &lt;div class=&quot;flex-shrink-0 me-3&quot;&gt;
        &lt;div class=&quot;avatar-xs&quot;&gt;
            &lt;div class=&quot;avatar-title bg-light rounded-circle text-muted fs-16&quot;&gt;
                &lt;i class=&quot;mdi mdi-facebook&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    &lt;div class=&quot;flex-grow-1&quot;&gt;
&lt;b-progress animated :value=&quot;15&quot; class=&quot;custom-progress progress-label&quot; variant=&quot;primary&quot;&gt;15%&lt;/b-progress&gt;
    &lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;d-flex align-items-center py-2&quot;&gt;
    &lt;div class=&quot;flex-shrink-0 me-3&quot;&gt;
        &lt;div class=&quot;avatar-xs&quot;&gt;
            &lt;div class=&quot;avatar-title bg-light rounded-circle text-muted fs-16&quot;&gt;
                &lt;i class=&quot;mdi mdi-twitter&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    &lt;div class=&quot;flex-grow-1&quot;&gt;
&lt;b-progress animated :value=&quot;25&quot; class=&quot;custom-progress progress-label&quot; variant=&quot;success&quot;&gt;25%&lt;/b-progress&gt;
    &lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;d-flex align-items-center py-2&quot;&gt;
    &lt;div class=&quot;flex-shrink-0 me-3&quot;&gt;
        &lt;div class=&quot;avatar-xs&quot;&gt;
            &lt;div class=&quot;avatar-title bg-light rounded-circle text-muted fs-16&quot;&gt;
                &lt;i class=&quot;mdi mdi-github&quot;&gt;&lt;/i&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/div&gt;
    &lt;div class=&quot;flex-grow-1&quot;&gt;
&lt;b-progress animated :value=&quot;50&quot; class=&quot;custom-progress progress-label&quot; variant=&quot;info&quot;&gt;50%&lt;/b-progress&gt;
    &lt;/div&gt;
&lt;/div&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Content Progress</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="bsprogrescontent-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="bsprogrescontent-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted pb-2">
              Example of progress with content wrapped in progress.
            </p>

            <div class="live-preview">
              <b-card no-body class="bg-light overflow-hidden shadow-none">
                <b-card-body>
                  <div class="d-flex">
                    <div class="flex-grow-1">
                      <h6 class="mb-0">
                        <b class="text-secondary">30%</b> Update in progress...
                      </h6>
                    </div>
                    <div class="flex-shrink-0">
                      <h6 class="mb-0">1 min left</h6>
                    </div>
                  </div>
                </b-card-body>

                <b-progress class="bg-soft-secondary rounded-0">
                  <b-progress-bar :value="30" variant="secondary" />
                </b-progress>
              </b-card>

              <b-card no-body class="bg-light overflow-hidden shadow-none">
                <b-card-body>
                  <div class="d-flex">
                    <div class="flex-grow-1">
                      <h6 class="mb-0">
                        <b class="text-success">60%</b> Update in progress...
                      </h6>
                    </div>
                    <div class="flex-shrink-0">
                      <h6 class="mb-0">45s left</h6>
                    </div>
                  </div>
                </b-card-body>

                <b-progress class="bg-soft-success rounded-0">
                  <b-progress-bar :value="60" variant="success" />
                </b-progress>
              </b-card>

              <b-card no-body class="bg-light overflow-hidden shadow-none">
                <b-card-body>
                  <div class="d-flex">
                    <div class="flex-grow-1">
                      <h6 class="mb-0">
                        <b class="text-danger">82%</b> Update in progress...
                      </h6>
                    </div>
                    <div class="flex-shrink-0">
                      <h6 class="mb-0">25s left</h6>
                    </div>
                  </div>
                </b-card-body>

                <b-progress class="bg-soft-danger rounded-0">
                  <b-progress-bar :value="82" variant="danger" />
                </b-progress>
              </b-card>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup" style="max-height:  275px">
<code>&lt;b-card class=&quot;bg-light overflow-hidden&quot;&gt;
    &lt;b-card no-body&gt;
        &lt;div class=&quot;d-flex&quot;&gt;
            &lt;div class=&quot;flex-grow-1&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;&lt;b class=&quot;text-secondary&quot;&gt;30%&lt;/b&gt; Update in progress...&lt;/h6&gt;
            &lt;/div&gt;
            &lt;div class=&quot;flex-shrink-0&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;1 min left&lt;/h6&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/b-card&gt;
&lt;b-progress :value=&quot;30&quot; class=&quot;custom-progress bg-soft-secondary rounded-0&quot; variant=&quot;secondary&quot;&gt;&lt;/b-progress&gt;
&lt;/b-card&gt;</code>

<code>&lt;b-card class=&quot;bg-light overflow-hidden&quot;&gt;
    &lt;b-card no-body&gt;
        &lt;div class=&quot;d-flex&quot;&gt;
            &lt;div class=&quot;flex-grow-1&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;&lt;b class=&quot;text-success&quot;&gt;60%&lt;/b&gt; Update in progress...&lt;/h6&gt;
            &lt;/div&gt;
            &lt;div class=&quot;flex-shrink-0&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;45s left&lt;/h6&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/b-card&gt;
&lt;b-progress :value=&quot;60&quot; class=&quot;custom-progress bg-soft-success rounded-0&quot; variant=&quot;success&quot;&gt;&lt;/b-progress&gt;
&lt;/b-card&gt;</code>

<code>&lt;b-card class=&quot;bg-light overflow-hidden&quot;&gt;
    &lt;b-card no-body&gt;
        &lt;div class=&quot;d-flex&quot;&gt;
            &lt;div class=&quot;flex-grow-1&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;&lt;b class=&quot;text-danger&quot;&gt;82%&lt;/b&gt; Update in progress...&lt;/h6&gt;
            &lt;/div&gt;
            &lt;div class=&quot;flex-shrink-0&quot;&gt;
                &lt;h6 class=&quot;mb-0&quot;&gt;25s left&lt;/h6&gt;
            &lt;/div&gt;
        &lt;/div&gt;
    &lt;/b-card&gt;
&lt;b-progress :value=&quot;82&quot; class=&quot;custom-progress bg-soft-danger rounded-0&quot; variant=&quot;danger&quot;&gt;&lt;/b-progress&gt;
&lt;/b-card&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xxl="6">
        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Progress with Steps</b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="bsprogressexample-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="bsprogressexample-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted pb-2">
              Here is the example of progress which is represented by steps
              completion.
            </p>

            <div class="live-preview">
              <div class="position-relative m-4">

                <b-progress style="max-height: 1px">
                  <b-progress-bar :value="50" variant="primary" />
                </b-progress>

                <b-button pill variant="primary" size="sm" type="button" class="
                    position-absolute
                    top-0
                    start-0
                    translate-middle
                    
                  " style="width: 2rem; height: 2rem">
                  1
                </b-button>
                <b-button pill variant="primary" size="sm" type="button" class="
                    position-absolute
                    top-0
                    start-50
                    translate-middle
                    
                  " style="width: 2rem; height: 2rem">
                  2
                </b-button>
                <b-button pill variant="light" size="sm" type="button" class="
                    position-absolute
                    top-0
                    start-100
                    translate-middle
                    
                  " style="width: 2rem; height: 2rem">
                  3
                </b-button>
              </div>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>&lt;div class=&quot;position-relative m-4&quot;&gt;
    &lt;div class=&quot;progress&quot; style=&quot;height: 1px;&quot;&gt;
        &lt;div class=&quot;progress-bar&quot; role=&quot;progressbar&quot; style=&quot;width: 50%;&quot; aria-valuenow=&quot;25&quot; aria-valuemin=&quot;0&quot; aria-valuemax=&quot;100&quot;&gt;&lt;/div&gt;
    &lt;/div&gt;
    &lt;b-button size=&quot;sm&quot; variant=&quot;primary&quot; class=&quot;position-absolute top-0 start-0 translate-middle rounded-pill&quot; style=&quot;width: 2rem; height:2rem;&quot;&gt;1&lt;/b-button&gt;
    &lt;b-button size=&quot;sm&quot; variant=&quot;primary&quot; class=&quot;position-absolute top-0 start-50 translate-middle rounded-pill&quot; style=&quot;width: 2rem; height:2rem;&quot;&gt;2&lt;/b-button&gt;
    &lt;b-button size=&quot;sm&quot; variant=&quot;light&quot; class=&quot;position-absolute top-0 start-100 translate-middlerounded-pill&quot; style=&quot;width: 2rem; height:2rem;&quot;&gt;3&lt;/b-button&gt;
&lt;/div&gt;</code></pre>
            </div>
          </b-card-body>
        </b-card>

        <b-card no-body>
          <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1"> Step Progress with Arrow </b-card-title>
            <div class="flex-shrink-0">
              <div class="form-check form-switch form-switch-right form-switch-md">
                <label for="stepprogressexample-showcode" class="form-label text-muted">Show Code</label>
                <input class="form-check-input code-switcher" type="checkbox" id="stepprogressexample-showcode" />
              </div>
            </div>
          </b-card-header>

          <b-card-body>
            <p class="text-muted pb-2">
              Use
              <code>progress-step-arrow</code> class to create step progress with
              an arrow.
            </p>

            <div class="live-preview">

              <b-progress class="progress-step-arrow progress-info">
                <b-progress-bar :value="100">
                  Step 1
                </b-progress-bar>

                <b-progress-bar :value="100">
                  Step 2
                </b-progress-bar>

                <b-progress-bar :value="100" variant="light" class="text-dark">
                  Step 3
                </b-progress-bar>
              </b-progress>
            </div>

            <div class="d-none code-view">
              <pre class="language-markup">
<code>
&lt;b-progress class=&quot;progress-step-arrow progress-info&quot;&gt;
    &lt;b-progress :value=&quot;33&quot; variant=&quot;primary&quot; &gt;Step 1 &lt;b-progress &gt;
    &lt;b-progress :value=&quot;33&quot; variant=&quot;primary&quot; &gt;Step 2 &lt;b-progress &gt;
    &lt;b-progress :value=&quot;33&quot; variant=&quot;light&quot; &gt;Step 3 &lt;b-progress &gt;
&lt;/b-progress&gt;
    </code></pre>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>