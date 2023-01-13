<script>
import Layout from "../../layouts/main.vue";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Widgets",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Widgets",

        };
    },
    name: "Widgets",
    components: {
        Layout
    },
};
</script>

<template>
    <Layout>
        <b-row>
            <b-col lg="12">
                <b-card no-body class="rounded-0 bg-soft-success mx-n4 mt-n4 border-top">
                    <div class="px-4">
                        <b-row>
                            <b-col xxl="5" class="align-self-center">
                                <div class="py-4">
                                    <h4 class="display-6 coming-soon-text">Frequently asked questions</h4>
                                    <p class="text-success fs-15 mt-3">If you can not find answer to your question in
                                        our FAQ, you can always contact us or email us. We will answer you shortly!</p>
                                    <div class="hstack flex-wrap gap-2">
                                        <b-button pill variant="primary" type="button" class="btn-label"><i
                                                class="ri-mail-line label-icon align-middle rounded-pill fs-16 me-2"></i>
                                            Email Us</b-button>
                                        <b-button pill variant="info" type="button" class="btn-label"><i
                                                class="ri-twitter-line label-icon align-middle rounded-pill fs-16 me-2"></i>
                                            Send Us Tweet</b-button>
                                    </div>
                                </div>
                            </b-col>
                            <b-col xxl="3" class="ms-auto">
                                <div class="mb-n5 pb-1 faq-img d-none d-xxl-block">
                                    <img src="@/assets/images/faq-img.png" alt="" class="img-fluid">
                                </div>
                            </b-col>
                        </b-row>
                    </div>
                </b-card>

                <b-row class="justify-content-evenly">
                    <b-col lg="4">
                        <div class="mt-3">
                            <div class="d-flex align-items-center mb-2">
                                <div class="flex-shrink-0 me-1">
                                    <i class="ri-question-line fs-24 align-middle text-success me-1"></i>
                                </div>
                                <div class="flex-grow-1">
                                    <h5 class="fs-14 mb-0">General Questions</h5>
                                </div>
                            </div>

                            <b-accordion class="accordion-border-box" id="genques-accordion">
                                <b-accordion-item title="What is Lorem Ipsum ?" visible>
                                    If several languages coalesce, the grammar of the resulting language is more
                                    simple and regular than that of the individual languages. The new common
                                    language will be more simple and regular than the existing European
                                    languages. It will be as simple their most common words.
                                </b-accordion-item>
                                <b-accordion-item title="Why do we use it ?">
                                    The new common language will be more simple and regular than the existing
                                    European languages. It will be as simple as Occidental; in fact, it will be
                                    Occidental. To an English person, it will seem like simplified English, as a
                                    skeptical Cambridge friend of mine told me what Occidental is.
                                </b-accordion-item>
                                <b-accordion-item title="Where does it come from ?">

                                    he wise man therefore always holds in these matters to this principle of
                                    selection: he rejects pleasures to secure other greater pleasures, or else
                                    he endures pains to avoid worse pains.But I must explain to you how all this
                                    mistaken idea of denouncing pleasure and praising pain was born and I will
                                    give you a complete.
                                </b-accordion-item>
                                <b-accordion-item title="Where can I get some ?">

                                    Cras ultricies mi eu turpis hendrerit fringilla. Vestibulum ante ipsum
                                    primis in faucibus orci luctus et ultrices posuere cubilia Curae; In ac dui
                                    quis mi consectetuer lacinia. Nam pretium turpis et arcu arcu tortor,
                                    suscipit eget, imperdiet nec, imperdiet iaculis aliquam ultrices mauris.

                                </b-accordion-item>
                            </b-accordion>
                        </div>
                    </b-col>

                    <b-col lg="4">
                        <div class="mt-3">
                            <div class="d-flex align-items-center mb-2">
                                <div class="flex-shrink-0 me-1">
                                    <i class="ri-user-settings-line fs-24 align-middle text-success me-1"></i>
                                </div>
                                <div class="flex-grow-1">
                                    <h5 class="fs-14 mb-0">Manage Account</h5>
                                </div>
                            </div>

                            <b-accordion class="accordion-border-box" id="manageaccount-accordion">
                                <b-accordion-item title="Where can I get some ?">
                                    If several languages coalesce, the grammar of the resulting language is more
                                    simple and regular than that of the individual languages. The new common
                                    language will be more simple and regular than the existing European
                                    languages. It will be as simple their most common words.
                                </b-accordion-item>
                                <b-accordion-item title="Where does it come from ?" visible>
                                    The new common language will be more simple and regular than the existing
                                    European languages. It will be as simple as Occidental; in fact, it will be
                                    Occidental. To an English person, it will seem like simplified English, as a
                                    skeptical Cambridge friend of mine told me what Occidental is.

                                </b-accordion-item>
                                <b-accordion-item title="Why do we use it ?">
                                    he wise man therefore always holds in these matters to this principle of
                                    selection: he rejects pleasures to secure other greater pleasures, or else
                                    he endures pains to avoid worse pains.But I must explain to you how all this
                                    mistaken idea of denouncing pleasure and praising pain was born and I will
                                    give you a complete.
                                </b-accordion-item>
                                <b-accordion-item title=" What is Lorem Ipsum ?">
                                    Cras ultricies mi eu turpis hendrerit fringilla. Vestibulum ante ipsum
                                    primis in faucibus orci luctus et ultrices posuere cubilia Curae; In ac dui
                                    quis mi consectetuer lacinia. Nam pretium turpis et arcu arcu tortor,
                                    suscipit eget, imperdiet nec, imperdiet iaculis aliquam ultrices mauris.
                                </b-accordion-item>
                            </b-accordion>
                        </div>
                    </b-col>

                    <b-col lg="4">
                        <div class="mt-3">
                            <div class="d-flex align-items-center mb-2">
                                <div class="flex-shrink-0 me-1">
                                    <i class="ri-shield-keyhole-line fs-24 align-middle text-success me-1"></i>
                                </div>
                                <div class="flex-grow-1">
                                    <h5 class="fs-14 mb-0">Privacy &amp; Security</h5>
                                </div>
                            </div>

                            <b-accordion class="accordion-border-box" id="privacy-accordion">
                                <b-accordion-item title="Why do we use it ?" visible>
                                    If several languages coalesce, the grammar of the resulting language is more
                                    simple and regular than that of the individual languages. The new common
                                    language will be more simple and regular than the existing European
                                    languages. It will be as simple their most common words.
                                </b-accordion-item>
                                <b-accordion-item title="Where can I get some ?">
                                    The new common language will be more simple and regular than the existing
                                    European languages. It will be as simple as Occidental; in fact, it will be
                                    Occidental. To an English person, it will seem like simplified English, as a
                                    skeptical Cambridge friend of mine told me what Occidental is.
                                </b-accordion-item>
                                <b-accordion-item title="What is Lorem Ipsum ?">
                                    he wise man therefore always holds in these matters to this principle of
                                    selection: he rejects pleasures to secure other greater pleasures, or else
                                    he endures pains to avoid worse pains.But I must explain to you how all this
                                    mistaken idea of denouncing pleasure and praising pain was born and I will
                                    give you a complete.
                                </b-accordion-item>
                                <b-accordion-item title="Where does it come from ?">
                                    Cras ultricies mi eu turpis hendrerit fringilla. Vestibulum ante ipsum
                                    primis in faucibus orci luctus et ultrices posuere cubilia Curae; In ac dui
                                    quis mi consectetuer lacinia. Nam pretium turpis et arcu arcu tortor,
                                    suscipit eget, imperdiet nec, imperdiet iaculis aliquam ultrices mauris.
                                </b-accordion-item>
                            </b-accordion>
                        </div>
                    </b-col>
                </b-row>
            </b-col>
        </b-row>
    </Layout>
</template>
