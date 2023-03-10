<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";

import 'prismjs';
import 'prismjs/themes/prism.css';

export default {
    data() {
        return {
            title: "Images",
            items: [
                {
                    text: "Base UI",
                    href: "/",
                },
                {
                    text: "Images",
                    active: true,
                },
            ],
        };
    },
    name: "Images",
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
            <b-col xxl="6">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Image Rounded & Circle</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="rounded-circle-image" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox"
                                    id="rounded-circle-image" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>b-avatar rounded="sm"</code> to show an image with a round border and rounded shape
                            respectively.
                        </p>

                        <div class="live-preview">
                            <b-row class="align-items-center">
                                <b-col cols="6">
                                    <img class="rounded" alt="200x200" width="200" src="@/assets/images/small/img-4.jpg"
                                        data-holder-rendered="true" />
                                </b-col>
                                <b-col cols="6">
                                    <div class="mt-4 mt-md-0">
                                        <img class="rounded-circle avatar-xl" alt="200x200"
                                            src="@/assets/images/users/avatar-4.jpg" data-holder-rendered="true" />
                                    </div>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- Rounded Image --&gt;
&lt;b-img class=&quot;rounded&quot; alt=&quot;200x200&quot; width=&quot;200&quot; src=&quot;...&quot; data-holder-rendered=&quot;true&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;!-- Rounded-circle Image --&gt;
&lt;b-img class=&quot;rounded-circle avatar-xl&quot; alt=&quot;200x200&quot; src=&quot;...&quot; data-holder-rendered=&quot;true&quot;&gt;&lt;/b-img&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>

            <b-col xxl="6">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Image Thumbnails</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="thumbnails-image" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="thumbnails-image" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>img-thumbnail</code> class to give an image
                            rounded 1px border appearance.
                        </p>

                        <div class="live-preview">
                            <b-row>
                                <b-col cols="6">
                                    <img class="img-thumbnail" alt="200x200" width="200"
                                        src="@/assets/images/small/img-3.jpg" data-holder-rendered="true" />
                                </b-col>
                                <b-col cols="6">
                                    <div class="mt-4 mt-md-0">
                                        <img class="img-thumbnail rounded-circle avatar-xl" alt="200x200"
                                            src="@/assets/images/users/avatar-3.jpg" data-holder-rendered="true" />
                                    </div>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- Thumbnails Images --&gt;
&lt;b-img class=&quot;img-thumbnail&quot; alt=&quot;200x200&quot; width=&quot;200&quot; src=&quot;...&quot; data-holder-rendered=&quot;true&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img class=&quot;img-thumbnail rounded-circle avatar-xl&quot; alt=&quot;200x200&quot; src=&quot;...&quot; data-holder-rendered=&quot;true&quot;&gt;&lt;/b-img&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Image Sizes</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="image-size" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="image-size" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="text-muted mb-4">
                            Use
                            <code>avatar-xxs</code>,
                            <code>avatar-xs</code>,
                            <code>avatar-sm</code>,
                            <code>avatar-md</code>,
                            <code>avatar-lg</code>,
                            <code>avatar-xl</code> class for different image sizes.
                        </p>

                        <div class="live-preview">
                            <b-row>
                                <b-col md="12">
                                    <b-row class="g-3">
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-2.jpg" alt
                                                    class="rounded avatar-xxs" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xxs</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-10.jpg" alt
                                                    class="rounded avatar-xs" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xs</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-3.jpg" alt
                                                    class="rounded avatar-sm" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-sm</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-4.jpg" alt
                                                    class="rounded avatar-md" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-md</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-5.jpg" alt
                                                    class="rounded avatar-lg" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-lg</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-8.jpg" alt
                                                    class="rounded avatar-xl" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xl</code>
                                                </p>
                                            </div>
                                        </b-col>
                                    </b-row>
                                </b-col>

                                <b-col md="12">
                                    <b-row class="g-3 mt-5">
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-2.jpg" alt
                                                    class="rounded-circle avatar-xxs" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xxs</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-10.jpg" alt
                                                    class="rounded-circle avatar-xs" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xs</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-3.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-sm</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-4.jpg" alt
                                                    class="rounded-circle avatar-md" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-md</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-5.jpg" alt
                                                    class="rounded-circle avatar-lg" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-lg</code>
                                                </p>
                                            </div>
                                        </b-col>
                                        <b-col xxl="2" md="4" cols="6">
                                            <div>
                                                <img src="@/assets/images/users/avatar-8.jpg" alt
                                                    class="rounded-circle avatar-xl" />
                                                <p class="mt-2 mb-lg-0">
                                                    <code>avatar-xl</code>
                                                </p>
                                            </div>
                                        </b-col>
                                    </b-row>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup"
                                style="height: 275px;"><code>&lt;!-- Image Sizes --&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-xxs&quot;/&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-xs&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-sm&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-md&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-lg&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded avatar-xl&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-xxs&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-xs&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-md&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-lg&quot;&gt;&lt;/b-img&gt;</code>

<code>&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-xl&quot;&gt;&lt;/b-img&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Avatar With Content</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="avatar-content" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="avatar-content" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="text-muted">
                            Use
                            <code>avatar-xxs, avatar-xs,avatar-sm,avatar-md,avatar-lg,avatar-xl</code> class to set
                            different avatar content.
                        </p>

                        <div class="live-preview">
                            <b-row class="g-3">
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-xxs mt-3">
                                        <div class="avatar-title rounded bg-soft-primary text-primary fs-10">XXS</div>
                                    </div>
                                </b-col>
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-xs mt-3">
                                        <div class="avatar-title rounded bg-soft-secondary text-secondary">XS</div>
                                    </div>
                                </b-col>
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-sm mt-3">
                                        <div class="avatar-title rounded bg-soft-success text-success fs-14">SM</div>
                                    </div>
                                </b-col>
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-md mt-3">
                                        <div class="avatar-title rounded bg-soft-info text-info fs-16">MD</div>
                                    </div>
                                </b-col>
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-lg mt-3">
                                        <div class="avatar-title rounded bg-soft-warning text-warning fs-20">LG</div>
                                    </div>
                                </b-col>
                                <b-col xxl="2" md="4" cols="6">
                                    <div class="avatar-xl mt-3">
                                        <div class="avatar-title rounded bg-soft-danger text-danger fs-22">XL</div>
                                    </div>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup" style="height: 200px;">
<code>&lt;!-- Avatar With Content --&gt;
&lt;div class=&quot;avatar-xxs&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-primary text-primary&quot;&gt;
XXS
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;avatar-xs&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-secondary text-secondary&quot;&gt;
XS
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;avatar-sm&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-success text-success&quot;&gt;
Sm
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;avatar-md&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-info text-info&quot;&gt;
Md
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;avatar-lg&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-warning text-warning&quot;&gt;
Lg
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;div class=&quot;avatar-xl&quot;&gt;
&lt;div class=&quot;avatar-title rounded bg-soft-danger text-danger&quot;&gt;
Xl
&lt;/div&gt;
&lt;/div&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Avatar Group</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="avatar-group" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="avatar-group" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <div class="live-preview">
                            <b-row>
                                <b-col lg="6">
                                    <div class="mt-lg-0 mt-3">
                                        <p class="text-muted">
                                            Use
                                            <code>avatar-group</code> class to show avatar images with the group.
                                        </p>
                                        <div class="avatar-group">
                                            <div class="avatar-group-item">
                                                <img src="@/assets/images/users/avatar-4.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                            </div>
                                            <div class="avatar-group-item">
                                                <img src="@/assets/images/users/avatar-5.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                            </div>
                                            <div class="avatar-group-item">
                                                <div class="avatar-sm">
                                                    <div class="avatar-title rounded-circle bg-light text-primary">A
                                                    </div>
                                                </div>
                                            </div>
                                            <div class="avatar-group-item">
                                                <img src="@/assets/images/users/avatar-2.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                            </div>
                                        </div>
                                    </div>
                                </b-col>

                                <b-col lg="6">
                                    <div class="mt-lg-0 mt-3">
                                        <p class="text-muted">
                                            Use
                                            <code>avatar-group</code> class with
                                            <code>data-bs-toggle="tooltip"</code> to show avatar group images with
                                            tooltip.
                                        </p>
                                        <div class="avatar-group">
                                            <b-link href="javascript: void(0);" class="avatar-group-item"
                                                data-bs-toggle="tooltip" data-bs-placement="top" title="Christi">
                                                <img src="@/assets/images/users/avatar-4.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                            </b-link>
                                            <b-link href="javascript: void(0);" class="avatar-group-item"
                                                data-bs-toggle="tooltip" data-bs-placement="top" title="Frank Hook">
                                                <img src="@/assets/images/users/avatar-3.jpg" alt
                                                    class="rounded-circle avatar-sm" />
                                            </b-link>
                                            <b-link href="javascript: void(0);" class="avatar-group-item"
                                                data-bs-toggle="tooltip" data-bs-placement="top" title="Christi">
                                                <div class="avatar-sm">
                                                    <div class="avatar-title rounded-circle bg-light text-primary">C
                                                    </div>
                                                </div>
                                            </b-link>
                                            <b-link href="javascript: void(0);" class="avatar-group-item"
                                                data-bs-toggle="tooltip" data-bs-placement="top" title="mORE">
                                                <div class="avatar-sm">
                                                    <div class="avatar-title rounded-circle">2+</div>
                                                </div>
                                            </b-link>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup" style="height: 275px;">
<code>&lt;!-- Simple Group --&gt;
&lt;div class=&quot;avatar-group&quot;&gt;
&lt;div class=&quot;avatar-group-item&quot;&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;
&lt;/div&gt;
&lt;div class=&quot;avatar-group-item&quot;&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;
&lt;/div&gt;
&lt;div class=&quot;avatar-group-item&quot;&gt;
&lt;div class=&quot;avatar-sm&quot;&gt;
&lt;div class=&quot;avatar-title rounded-circle bg-light text-primary&quot;&gt;
A
&lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;div class=&quot;avatar-group-item&quot;&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;
&lt;/div&gt;
&lt;/div&gt;</code>

<code>&lt;!-- Avatar Group with Tooltip --&gt;
&lt;div class=&quot;avatar-group&quot;&gt;
&lt;a href=&quot;javascript: void(0);&quot; class=&quot;avatar-group-item&quot; data-bs-toggle=&quot;tooltip&quot; data-bs-placement=&quot;top&quot; title=&quot;Christi&quot;&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;
&lt;/a&gt;
&lt;a href=&quot;javascript: void(0);&quot; class=&quot;avatar-group-item&quot; data-bs-toggle=&quot;tooltip&quot; data-bs-placement=&quot;top&quot; title=&quot;Frank Hook&quot;&gt;
&lt;b-img src=&quot;...&quot; alt=&quot;&quot; class=&quot;rounded-circle avatar-sm&quot;&gt;&lt;/b-img&gt;
&lt;/a&gt;
&lt;a href=&quot;javascript: void(0);&quot; class=&quot;avatar-group-item&quot; data-bs-toggle=&quot;tooltip&quot; data-bs-placement=&quot;top&quot; title=&quot;Christi&quot;&gt;
&lt;div class=&quot;avatar-sm&quot;&gt;
&lt;div class=&quot;avatar-title rounded-circle bg-light text-primary&quot;&gt;
C
&lt;/div&gt;
&lt;/div&gt;
&lt;/a&gt;
&lt;a href=&quot;javascript: void(0);&quot; class=&quot;avatar-group-item&quot; data-bs-toggle=&quot;tooltip&quot; data-bs-placement=&quot;top&quot; title=&quot;more&quot;&gt;
&lt;div class=&quot;avatar-sm&quot;&gt;
&lt;div class=&quot;avatar-title rounded-circle&quot;&gt;
2+
&lt;/div&gt;
&lt;/div&gt;
&lt;/a&gt;
&lt;/div&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col xl="8">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Figures</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="Figures-image" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="Figures-image" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="card-title-desc text-muted">
                            Use the included
                            <code>figure</code>,
                            <code>figure-img</code> and
                            <code>figure-caption</code> classes to provide some baseline styles for the HTML5
                            <code>&lt;figure&gt;</code> and
                            <code>&lt;figcaption&gt;</code> elements.
                        </p>

                        <div class="live-preview">
                            <b-row class="g-3">
                                <b-col sm="6">
                                    <figure class="figure mb-0">
                                        <img src="@/assets/images/small/img-4.jpg" class="figure-img img-fluid rounded"
                                            alt="..." />
                                        <figcaption class="figure-caption">A caption for the above image.</figcaption>
                                    </figure>
                                </b-col>
                                <b-col sm="6">
                                    <figure class="figure mb-0">
                                        <img src="@/assets/images/small/img-5.jpg" class="figure-img img-fluid rounded"
                                            alt="..." />
                                        <figcaption class="figure-caption text-end">A caption for the above image.
                                        </figcaption>
                                    </figure>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- figures Images --&gt;
&lt;figure class=&quot;figure&quot;&gt;
&lt;b-img src=&quot;...&quot; class=&quot;figure-img img-fluid rounded&quot; alt=&quot;...&quot;&gt;&lt;/b-img&gt;
&lt;figcaption class=&quot;figure-caption&quot;&gt;A caption for the above image.&lt;/figcaption&gt;
&lt;/figure&gt;</code>

<code>&lt;figure class=&quot;figure mb-0&quot;&gt;
&lt;b-img src=&quot;...&quot; class=&quot;figure-img img-fluid rounded&quot; alt=&quot;...&quot;&gt;&lt;/b-img&gt;
&lt;figcaption class=&quot;figure-caption text-end&quot;&gt;A caption for the above image.&lt;/figcaption&gt;
&lt;/figure&gt;</code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>

            <b-col xl="4">
                <b-card no-body>
                    <b-card-header class="align-items-center d-flex">
                        <b-card-title class="mb-0 flex-grow-1">Responsive Images</b-card-title>
                        <div class="flex-shrink-0">
                            <div class="form-check form-switch form-switch-right form-switch-md">
                                <label for="responsive-image" class="form-label text-muted">Show Code</label>
                                <input class="form-check-input code-switcher" type="checkbox" id="responsive-image" />
                            </div>
                        </div>
                    </b-card-header>

                    <b-card-body>
                        <p class="card-title-desc text-muted">
                            Responsive Images with
                            <code>img-fluid,max-width: 100%; and height: auto;</code> to the image so that it scales
                            with the parent width.
                        </p>

                        <div class="live-preview">
                            <div>
                                <img src="@/assets/images/small/img-2.jpg" class="img-fluid" alt="Responsive image" />
                            </div>
                        </div>

                        <div class="d-none code-view">
                            <pre class="language-markup">
<code>&lt;!-- Responsive Images --&gt;
&lt;b-img src=&quot;...&quot; class=&quot;img-fluid&quot; alt=&quot;Responsive image&quot;&gt; &lt;/b-img&gt; </code></pre>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>