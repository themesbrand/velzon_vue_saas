<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";

import 'prismjs';
import 'prismjs/themes/prism.css';

export default {
    data() {
        return {
            title: "Placeholders",
            items: [
                {
                    text: "Base UI",
                    href: "/",
                },
                {
                    text: "Placeholders",
                    active: true,
                },
            ],
        };
    },
    name: "Placeholders",
    components: {
        Layout,
        PageHeader,
    },
    mounted() {
        const checkbox = document.getElementsByClassName("code-switcher");
        Array.from(checkbox).forEach((check) => {
            check.addEventListener('change', () => {
                const card = check.closest('.card');
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
    }
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Default Placeholder</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="baseexample-showcode" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox"
                                    id="baseexample-showcode" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="text-muted">In the example below, we take a typical card component and recreate it
                            with placeholders applied to create a “loading card”.</p>

                        <div class="live-preview">
                            <b-row class="justify-content-center">
                                <b-col xl="7">
                                    <b-row class="justify-content-between">
                                        <b-col lg="5" sm="6">
                                            <b-card no-body>
                                                <img src="@/assets/images/small/img-1.jpg" class="card-img-top"
                                                    alt="card img" />

                                                <b-card-body>
                                                    <h5 class="card-title">Card title</h5>
                                                    <p class="card-text">Some quick example text to build on the card
                                                        title and make up the bulk of the card's content.</p>
                                                    <b-link href="#" class="btn btn-primary">Go somewhere</b-link>
                                                </b-card-body>
                                            </b-card>
                                        </b-col>
                                        <b-col lg="5" sm="6">
                                            <b-card no-body aria-hidden="true">
                                                <img src="@/assets/images/small/img-2.jpg" class="card-img-top"
                                                    alt="card dummy img" />
                                                <b-card-body>
                                                    <h5 class="card-title placeholder-glow">
                                                        <span class="placeholder col-6"></span>
                                                    </h5>
                                                    <p class="card-text placeholder-glow">
                                                        <span class="placeholder col-7"></span>
                                                        <span class="placeholder col-4"></span>
                                                        <span class="placeholder col-4"></span>
                                                        <span class="placeholder col-6"></span>
                                                    </p>
                                                    <b-link href="#" tabindex="-1"
                                                        class="btn btn-primary disabled placeholder col-6"></b-link>
                                                </b-card-body>
                                            </b-card>
                                        </b-col>
                                    </b-row>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup" style="height: 275px">
<code>&lt;!-- Base Examples --&gt;
&lt;b-card&gt;
    &lt;img src=&quot;...&quot; class=&quot;card-img-top&quot; alt=&quot;card img&quot;&gt;
    &lt;b-card no-body&gt;
        &lt;h5 class=&quot;card-title&quot;&gt;Card title&lt;/h5&gt;
        &lt;p class=&quot;card-text&quot;&gt;Some quick example text to build on the card title and make up the bulk of the card's content.&lt;/p&gt;
        &lt;a href=&quot;#&quot; class=&quot;btn btn-primary&quot;&gt;Go somewhere&lt;/a&gt;
    &lt;/b-card&gt;
&lt;/b-card&gt;</code>

<code>&lt;b-card aria-hidden=&quot;true&quot;&gt;
    &lt;img src=&quot;assets/images/small/img-2.jpg&quot; class=&quot;card-img-top&quot; alt=&quot;card dummy img&quot;&gt;
    &lt;b-card no-body&gt;
      &lt;b-card title=&quot; &quot; class=&quot;placeholder-glow&quot;&gt;
        &lt;span class=&quot;placeholder col-6&quot;&gt;&lt;/span&gt;
      &lt;/b-card&gt;
      &lt;b-card-text class=&quot;placeholder-glow&quot;&gt;
        &lt;span class=&quot;placeholder col-7&quot;&gt;&lt;/span&gt;
        &lt;span class=&quot;placeholder col-4&quot;&gt;&lt;/span&gt;
        &lt;span class=&quot;placeholder col-4&quot;&gt;&lt;/span&gt;
        &lt;span class=&quot;placeholder col-6&quot;&gt;&lt;/span&gt;
      &lt;/b-card-text&gt;
      &lt;b-link href=&quot;#&quot; tabindex=&quot;-1&quot; class=&quot;btn btn-primary disabled placeholder col-6&quot;&gt;&lt;/b-link&gt;
    &lt;/b-card&gt;
&lt;/b-card&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col xxl="6">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Width</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="width-showcode" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="width-showcode" />
                            </div>
                        </div>
                    </b-card-header>
                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>w-25,w-50,w-75</code> or
                            <code>w-100</code> class to placeholder class to set different widths to the placeholder.
                        </p>
                        <div class="live-preview">
                            <span class="placeholder w-50"></span>
                            <span class="placeholder w-75"></span>
                            <span class="placeholder w-25"></span>
                            <span class="placeholder w-100"></span>
                        </div>
                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- Width Sizing--&gt;
&lt;div class=&quot;live-preview&quot;&gt;
    &lt;span class=&quot;placeholder col-6&quot;&gt;&lt;/span&gt;
    &lt;span class=&quot;placeholder w-75&quot;&gt;&lt;/span&gt;
    &lt;span class=&quot;placeholder&quot; style=&quot;width: 25%;&quot;&gt;&lt;/span&gt;
&lt;/div&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xxl="6">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Sizing</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="sizing-showcode" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="sizing-showcode" />
                            </div>
                        </div>
                    </b-card-header>
                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>placeholder-lg</code>,
                            <code>placeholder-sm</code>, or
                            <code>placeholder-xs</code> class to placeholder class to set different size placeholder.
                        </p>
                        <div class="live-preview">
                            <b-row class="gap-0">
                                <b-col cols="12">
                                    <span class="placeholder placeholder-lg w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder placeholder-sm w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder placeholder-xs w-100"></span>
                                </b-col>
                            </b-row>
                        </div>
                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- Sizing --&gt;
&lt;span class=&quot;placeholder col-12 placeholder-lg&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 placeholder-sm&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 placeholder-xs&quot;&gt;&lt;/span&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Color</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="color-showcode" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="color-showcode" />
                            </div>
                        </div>
                    </b-card-header>
                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>bg-</code> class with the below-mentioned color variation to set a custom color.
                        </p>
                        <div class="live-preview">
                            <b-row class="g-2">
                                <b-col cols="12">
                                    <span class="placeholder w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-primary w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-secondary w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-success w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-danger w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-warning w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-info w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-light w-100"></span>
                                </b-col>
                                <b-col cols="12">
                                    <span class="placeholder bg-dark w-100"></span>
                                </b-col>
                            </b-row>
                        </div>
                        <div class="d-none code-view">
                            <pre class="language-markup" style="height: 275px">
<code>&lt;!-- Color --&gt;
&lt;span class=&quot;placeholder col-12 mb-3&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-primary&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-secondary&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-success&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-danger&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-warning&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-info&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-light&quot;&gt;&lt;/span&gt;</code>

<code>&lt;span class=&quot;placeholder col-12 mb-3 bg-dark&quot;&gt;&lt;/span&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>