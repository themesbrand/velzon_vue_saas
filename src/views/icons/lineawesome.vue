<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Line Awesome",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Line Awesome",
            items: [
                {
                    text: "Icons",
                    href: "/",
                },
                {
                    text: "Line Awesome",
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
        <b-row class="icon-demo-content">
            <b-col cols="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title>Examples</b-card-title>
                        <p class="text-muted mb-0">Use <code>&lt;i class="lab la-*-*">&lt;/i></code> class.</p>
                    </b-card-header>
                    <b-card-body>
                        <h6 class="text-uppercase text-muted fw-semibold">Accessibility</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-accessible-icon"></i> lab la-accessible-icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-american-sign-language-interpreting"></i> las
                                la-amean-sign-language-interpreting
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-assistive-listening-systems"></i> las la-assistive-listening-systems
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-audio-description"></i> las la-audio-description
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blind"></i> las la-blind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-braille"></i> las la-braille
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-closed-captioning"></i> las la-closed-captioning
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-deaf"></i> las la-deaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-low-vision"></i> las la-low-vision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-volume"></i> las la-phone-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question-circle"></i> las la-question-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-language"></i> las la-sign-language
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tty"></i> las la-tty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-universal-access"></i> las la-universal-acces
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Alert</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation"></i> las la-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-circle"></i> las la-exclamation-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-triangle"></i> las la-exclamation-triangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation"></i> las la-radiation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation-alt"></i> las la-radiation-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Animals</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cat"></i> las la-cat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crow"></i> las la-crow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dog"></i> las la-dog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dove"></i> las la-dove
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dragon"></i> las la-dragon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-feather"></i> las la-feather
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-feather-alt"></i> las la-feather-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fish"></i> las la-fish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frog"></i> las la-frog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hippo"></i> las la-hippo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-horse"></i> las la-horse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-horse-head"></i> las la-horse-head
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kiwi-bird"></i> las la-kiwi-bird
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-otter"></i> las la-otter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paw"></i> las la-paw
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spider"></i> las la-spider
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Arrows</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-double-down"></i>las la-angle-double-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-double-left"></i>las la-angle-double-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-double-right"></i>las la-angle-double-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-double-up"></i>las la-angle-double-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-down"></i>las la-angle-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-left"></i>las la-angle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-right"></i>las la-angle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angle-up"></i>las la-angle-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-alt-circle-down"></i>las la-arrow-alt-circle-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-alt-circle-left"></i>las la-arrow-alt-circle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-alt-circle-right"></i>las la-arrow-alt-circle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-alt-circle-up"></i>las la-arrow-alt-circle-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-circle-down"></i> las la-arrow-circle-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-circle-left"></i> las la-arrow-circle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-circle-right"></i> las la-arrow-circle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-circle-up"></i> las la-arrow-circle-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-down"></i> las la-arrow-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-left"></i> las la-arrow-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-right"></i> las la-arrow-righ
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrow-up"></i> las la-arrow-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrows-alt"></i> las la-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrows-alt-h"></i> las la-arrows-alt-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-arrows-alt-v"></i> las la-arrows-alt-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-down"></i> las la-caret-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-left"></i> las la-caret-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-right"></i> las la-caret-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-square-down"></i> las la-caret-square-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-square-left"></i> las la-caret-square-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-square-right"></i> las la-caret-square-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-square-up"></i> las la-caret-square-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-caret-up"></i> las la-caret-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cart-arrow-down"></i> las la-cart-arrow-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-line"></i> las la-chart-line
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-circle-down"></i> las la-chevron-circle-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-circle-left"></i> las la-chevron-circle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-circle-right"></i> las la-chevron-circle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-circle-up"></i> las la-chevron-circle-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-down"></i> las la-chevron-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-left"></i> las la-chevron-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-right"></i> las la-chevron-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chevron-up"></i> las la-chevron-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-download-alt"></i> las la-cloud-download-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-upload-alt"></i> las la-cloud-upload-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compress-arrows-alt"></i> las la-compress-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-download"></i> las la-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exchange-alt"></i> las la-exchange-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-expand-arrows-alt"></i> las la-expand-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-external-link-alt"></i> las la-external-link-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-external-link-square-alt"></i> las la-external-link-square-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-down"></i> las la-hand-point-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-left"></i> las la-hand-point-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-right"></i> las la-hand-point-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-up"></i> las la-hand-point-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-pointer"></i> las la-hand-pointer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-history"></i> las la-history
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-level-down-alt"></i> las la-level-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-level-up-alt"></i> las la-level-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-location-arrow"></i> las la-location-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-long-arrow-alt-down"></i> las la-long-arrow-alt-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-long-arrow-alt-left"></i> las la-long-arrow-alt-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-long-arrow-alt-right"></i> las la-long-arrow-alt-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-long-arrow-alt-up"></i> las la-long-arrow-alt-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mouse-pointer"></i> las la-mouse-pointer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-play"></i> las la-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-random"></i> las la-random
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-recycle"></i> las la-recycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo"></i> las la-redo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo-alt"></i> las la-redo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-reply"></i> las la-reply
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-reply-all"></i> las la-reply-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-retweet"></i> las la-retweet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share"></i> las la-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-square"></i> las la-share-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-in-alt"></i> las la-sign-in-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-out-alt"></i> las la-sign-out-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort"></i> las la-sort
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-down"></i> las la-sort-alpha-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-down-alt"></i> las la-sort-alpha-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-up"></i> las la-sort-alpha-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-up-alt"></i> las la-sort-alpha-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-down"></i> las la-sort-amount-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-down-alt"></i> las la-sort-amount-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-up"></i> las la-sort-amount-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-up-alt"></i> las la-sort-amount-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-down"></i> las la-sort-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-down"></i> las la-sort-numeric-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-down-alt"></i> las la-sort-numeric-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-up"></i> las la-sort-numeric-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-up-alt"></i> las la-sort-numeric-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-up"></i> las la-sort-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync"></i> las la-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync-alt"></i> las la-sync-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-text-height"></i> las la-text-height
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-text-width"></i> las la-text-width
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo"></i> las la-undo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo-alt"></i> las la-undo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-upload"></i> las la-upload
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Audio & Video</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-audio-description"></i> las la-audio-description
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-backward"></i> las la-backward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broadcast-tower"></i> las la-broadcast-tower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-circle"></i> las la-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-closed-captioning"></i> las la-closed-captioning
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compress"></i> las la-compress
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compress-arrows-alt"></i> las la-compress-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eject"></i> las la-eject
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-expand"></i> las la-expand
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-expand-arrows-alt"></i> las la-expand-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fast-backward"></i> las la-fast-backward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fast-forward"></i> las la-fast-forward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-audio"></i> las la-file-audio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-video"></i> las la-file-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-film"></i> las la-film
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-forward"></i> las la-forward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones"></i> las la-headphones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt-slash"></i> las la-microphone-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-slash"></i> las la-microphone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-music"></i> las la-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pause"></i> las la-pause
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pause-circle"></i> las la-pause-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-volume"></i> las la-phone-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-photo-video"></i> las la-photo-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-play"></i> las la-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-play-circle"></i> las la-play-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-podcast"></i> las la-podcast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-random"></i> las la-random
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo"></i> las la-redo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo-alt"></i> las la-redo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss"></i> las la-rss
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss-square"></i> las la-rss-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-step-backward"></i> las la-step-backward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-step-forward"></i> las la-step-forward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stop"></i> las la-stop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stop-circle"></i> las la-stop-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync"></i> las la-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync-alt"></i> las la-sync-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo"></i> las la-undo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo-alt"></i> las la-undo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video"></i> las la-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-down"></i> las la-volume-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-mute"></i> las la-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-off"></i> las la-volume-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-up"></i> las la-volume-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-youtube"></i> lab la-youtube
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Automotive</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-air-freshener"></i> las la-air-freshener
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ambulance"></i> las la-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bus"></i> las la-bus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bus-alt"></i> las la-bus-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car"></i> las la-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car-alt"></i> las la-car-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car-battery"></i> las la-car-battery
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car-crash"></i> las la-car-crash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car-side"></i> las la-car-side
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-charging-station"></i> las la-charging-station
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gas-pump"></i> las la-gas-pump
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-motorcycle"></i> las la-motorcycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-oil-can"></i> las la-oil-can
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shuttle-van"></i> las la-shuttle-van
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tachometer-alt"></i> las la-tachometer-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-taxi"></i> las la-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck"></i> las la-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck-monster"></i> las la-truck-monster
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck-pickup"></i> las la-truck-pickup
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Autumn</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-apple-alt"></i> las la-apple-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-campground"></i> las la-campground
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-sun"></i> las la-cloud-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drumstick-bite"></i> las la-drumstick-bite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-football-ball"></i> las la-football-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hiking"></i> las la-hiking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mountain"></i> las la-mountain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tractor"></i> las la-tractor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tree"></i> las la-tree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wind"></i> las la-wind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-bottle"></i> las la-wine-bottle
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Beverage</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-beer"></i> las la-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blender"></i> las la-blender
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cocktail"></i> las la-cocktail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flask"></i> las la-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-cheers"></i> las la-glass-cheers
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini"></i> las la-glass-martini
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini-alt"></i> las la-glass-martini-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-whiskey"></i> las la-glass-whiskey
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mug-hot"></i> las la-mug-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-bottle"></i> las la-wine-bottle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass"></i> las la-wine-glas
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass-alt"></i>las la-wine-glass-alt
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Brand Icons</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-500px"></i> lab la-500px
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-accusoft"></i> lab la-accusoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adn"></i> lab la-adn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adobe"></i> lab la-adobe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adversal"></i> lab la-adversa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-affiliatetheme"></i> lab la-affiliatetheme
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-airbnb"></i> lab la-airbnb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-algolia"></i> lab la-algolia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-amazon"></i> lab la-amazon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-amilia"></i> lab la-amilia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-android"></i> lab la-android
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angellist"></i> lab la-angellist
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angrycreative"></i> lab la-angrycreative
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angular"></i> lab la-angular
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-app-store"></i> lab la-app-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-app-store-ios"></i> lab la-app-store-ios
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-apper"></i> lab la-apper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-apple"></i> lab la-apple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-artstation"></i> lab la-artstation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-asymmetrik"></i> lab la-asymmetrik
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-atlassian"></i> lab la-atlassian
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-audible"></i> lab la-audible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-autoprefixer"></i> lab la-autoprefixer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-avianex"></i> lab la-avianex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-aviato"></i> lab la-aviato
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-aws"></i> lab la-aws
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bandcamp"></i> lab la-bandcamp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-battle-net"></i> lab la-battle-net
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-behance"></i> lab la-behance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-behance-square"></i> lab la-behance-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bimobject"></i> lab la-bimobject
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bitbucket"></i> lab la-bitbucket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bity"></i> lab la-bity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-black-tie"></i> lab la-black-tie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blackberry"></i> lab la-blackberry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blogger"></i> lab la-blogger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blogger-b"></i> lab la-blogger-b
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bootstrap"></i> lab la-bootstrap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buffer"></i> lab la-buffer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buromobelexperte"></i> lab la-buromobelexperte
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buy-n-large"></i> lab la-buy-n-large
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buysellads"></i> lab la-buysellads
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-canadian-maple-leaf"></i> lab la-canadian-maple-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-centercode"></i> lab la-centercode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-centos"></i> lab la-centos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-chrome"></i> lab la-chrome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-chromecast"></i> lab la-chromecast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudscale"></i> lab la-cloudscale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudsmith"></i> lab la-cloudsmith
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudversify"></i> lab la-cloudversify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-codepen"></i> lab la-codepen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-codiepie"></i> lab la-codiepie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-confluence"></i> lab la-confluence
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-connectdevelop"></i> lab la-connectdevelop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-contao"></i> lab la-contao
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cotton-bureau"></i> lab la-cotton-bureau
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cpanel"></i> lab la-cpanel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons"></i>lab la-creative-commons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-by"></i>lab la-creative-commons-by
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc"></i>lab la-creative-commons-nc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc-eu"></i>lab la-creative-commons-nc-eu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc-jp"></i>lab la-creative-commons-nc-jp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nd"></i>lab la-creative-commons-nd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-pd"></i>lab la-creative-commons-pd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-pd-alt"></i>lab la-creative-commons-pd-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-remix"></i>lab la-creative-commons-remix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sa"></i>lab la-creative-commons-sa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sampling"></i>lab la-creative-commons-sampling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sampling-plus"></i>lab
                                la-creative-commons-sampling-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-share"></i>lab la-creative-commons-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-zero"></i>lab la-creative-commons-zero
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-css3"></i> lab la-css3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-css3-alt"></i> lab la-css3-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cuttlefish"></i> lab la-cuttlefish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dashcube"></i> lab la-dashcube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-delicious"></i> lab la-delicious
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deploydog"></i> lab la-deploydog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deskpro"></i> lab la-deskpro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dev"></i> lab la-dev
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deviantart"></i> lab la-deviantart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dhl"></i> lab la-dhl
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-diaspora"></i> lab la-diaspora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-digg"></i> lab la-digg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-digital-ocean"></i> lab la-digital-ocean
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-discord"></i> lab la-discord
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-discourse"></i> lab la-discourse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dochub"></i> lab la-dochub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-docker"></i> lab la-docker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-draft2digital"></i> lab la-draft2digital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dribbble"></i> lab la-dribbble
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dribbble-square"></i> lab la-dribbble-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dropbox"></i> lab la-dropbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-drupal"></i> lab la-drupal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dyalog"></i> lab la-dyalog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-earlybirds"></i> lab la-earlybirds
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ebay"></i> lab la-ebay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-edge"></i> lab la-edge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-elementor"></i> lab la-elementor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ello"></i> lab la-ello
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ember"></i> lab la-ember
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-empire"></i> lab la-empire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-envira"></i> lab la-envira
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-erlang"></i> lab la-erlang
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-etsy"></i> lab la-etsy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-evernote"></i> lab la-evernote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-expeditedssl"></i> lab la-expeditedssl
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook"></i> lab la-facebook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-f"></i> lab la-facebook-k
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-messenger"></i> lab la-facebook-messenger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-square"></i> lab la-facebook-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fedex"></i> lab la-fedex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fedora"></i> lab la-fedora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-figma"></i> lab la-figma
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-firefox"></i> lab la-firefox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-first-order"></i> lab la-first-order
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-first-order-alt"></i> lab la-first-order-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-firstdraft"></i> lab la-firstdraft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-flickr"></i> lab la-flickr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-flipboard"></i> lab la-flipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fly"></i> lab la-fly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome"></i> lab la-font-awesome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome-alt"></i> lab la-font-awesome-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome-flag"></i> lab la-font-awesome-flog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fonticons"></i> lab la-fonticons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fonticons-fi"></i> lab la-fonticons-fi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fort-awesome"></i> lab la-fort-awesome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fort-awesome-alt"></i> lab la-fort-awesome-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-forumbee"></i> lab la-forumbee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-foursquare"></i> lab la-foursquare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-free-code-camp"></i> lab la-free-code-camp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-freebsd"></i> lab la-freebsd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fulcrum"></i> lab la-fulcrum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-get-pocket"></i> lab la-get-pocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git"></i> lab la-git
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git-alt"></i>lab la-git-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git-square"></i> lab la-git-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-github"></i>lab la-github
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-github-alt"></i>lab la-github-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-github-square"></i>lab la-github-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gitkraken"></i>lab la-gitkraken
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gitlab"></i> lab la-gitlab
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gitter"></i> lab la-gitter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-glide"></i> lab la-glide
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-glide-g"></i> lab la-glide-g
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gofore"></i> lab la-gofore
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-goodreads"></i> lab la-goodreads
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-goodreads-g"></i> lab la-goodreads-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google"></i> lab la-google
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-drive"></i>lab la-google-drive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-play"></i>lab la-google-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus"></i>lab la-google-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus-g"></i>lab la-google-plus-g
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus-square"></i>lab la-google-plus-squar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gratipay"></i> lab la-gratipay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-grav"></i> lab la-grav
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gripfire"></i> lab la-gripfire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-grunt"></i> lab la-grunt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gulp"></i> lab la-gulp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hacker-news"></i> lab la-hacker-news
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hacker-news-square"></i> lab la-hacker-news-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hackerrank"></i> lab la-hackerrank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hips"></i> lab la-hips
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hire-a-helper"></i> lab la-hire-a-helper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hooli"></i> lab la-hooli
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hornbill"></i> lab la-hornbill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hotjar"></i> lab la-hotjar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-houzz"></i> lab la-houzz
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-html5"></i> lab la-html5
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hubspot"></i> lab la-hubspot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-imdb"></i> lab la-imdb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-instagram"></i> lab la-instagram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-intercom"></i> lab la-intercom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-internet-explorer"></i> lab la-internet-explorer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-invision"></i> lab la-invisio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ioxhost"></i> lab la-ioxhost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itch-io"></i> lab la-itch-io
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itunes"></i> lab la-itunes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itunes-note"></i> lab la-itunes-note
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-java"></i> lab la-java
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jenkins"></i> lab la-jenkins
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jira"></i> lab la-jira
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-joget"></i> lab la-joget
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-joomla"></i> lab la-joomla
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-js"></i> lab la-js
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-js-square"></i> lab la-js-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jsfiddle"></i> lab la-jsfiddle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kaggle"></i> lab la-kaggle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-keybase"></i> lab la-keybase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-keycdn"></i> lab la-keycdn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kickstarter"></i> lab la-kickstarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kickstarter-k"></i> lab la-kickstarter-
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-korvue"></i> lab la-korvue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-laravel"></i> lab la-laravel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lastfm"></i> lab la-lastfm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lastfm-square"></i> lab la-lastfm-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-leanpub"></i> lab la-leanpub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-less"></i> lab la-less
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-line"></i> lab la-line
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linkedin"></i> lab la-linkedin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linkedin-in"></i> lab la-linkedin-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linode"></i> lab la-linode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linux"></i> lab la-linux
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lyft"></i> lab la-lyft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-magento"></i> lab la-magento
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mailchimp"></i> lab la-mailchimp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mandalorian"></i> lab la-mandalorian
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-markdown"></i> lab la-markdown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mastodon"></i> lab la-mastodon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-maxcdn"></i> lab la-maxcdn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mdb"></i> lab la-mdb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medapps"></i> lab la-medapps
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medium"></i> lab la-medium
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medium-m"></i> lab la-medium-m
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medrt"></i> lab la-medrt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-meetup"></i> lab la-meetup
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-megaport"></i> lab la-megaport
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mendeley"></i> lab la-mendeley
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-microsoft"></i> lab la-microsoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mix"></i> lab la-mix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mixcloud"></i> lab la-mixclou
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mizuni"></i> lab la-mizuni
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-modx"></i> lab la-modx
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-monero"></i> lab la-monero
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-neos"></i> lab la-neos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-nimblr"></i> lab la-nimblr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-node"></i> lab la-node
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-node-js"></i> lab la-node-js
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-npm"></i> lab la-npm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ns8"></i> lab la-ns8
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-nutritionix"></i> lab la-nutritionix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-odnoklassniki"></i> lab la-odnoklassniki
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-odnoklassniki-square"></i> lab la-odnoklassniki-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-opencart"></i> lab la-opencart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-openid"></i> lab la-openid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-opera"></i> lab la-opera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-optin-monster"></i> lab la-optin-monster
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-orcid"></i> lab la-orcid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-osi"></i> lab la-osi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-page4"></i> lab la-page4
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pagelines"></i> lab la-pagelines
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-palfed"></i> lab la-palfed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-patreon"></i> lab la-patreon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-periscope"></i> lab la-periscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phabricator"></i> lab la-phabricator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phoenix-framework"></i> lab la-phoenix-framework
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phoenix-squadron"></i> lab la-phoenix-squadron
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-php"></i> lab la-php
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper"></i> lab la-pied-piper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-alt"></i> lab la-pied-piper-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-hat"></i> lab la-pied-piper-hat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-pp"></i> lab la-pied-piper-pp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest"></i> lab la-pinterest
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest-p"></i> lab la-pinterest-p
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest-square"></i> lab la-pinterest-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-product-hunt"></i> lab la-product-hunt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pushed"></i> lab la-pushed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-python"></i> lab la-python
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-qq"></i> lab la-qq
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-quinscape"></i> lab la-quinscape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-quora"></i> lab la-quora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-r-project"></i> lab la-r-project
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-raspberry-pi"></i> lab la-raspberry-p
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ravelry"></i> lab la-ravelry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-react"></i> lab la-react
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reacteurope"></i> lab la-reacteurope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-readme"></i> lab la-readme
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rebel"></i> lab la-rebel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-red-river"></i> lab la-red-river
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit"></i> lab la-reddit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit-alien"></i>lab la-reddit-alien
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit-square"></i>lab la-reddit-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-redhat"></i>lab la-redhat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-renren"></i>lab la-renren
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-researchgate"></i> lab la-researchgate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-resolving"></i> lab la-resolving
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rev"></i> lab la-rev
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rocketchat"></i> lab la-rocketchat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rockrms"></i> lab la-rockrms
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-safari"></i> lab la-safari
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-salesforce"></i> lab la-salesforce
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sass"></i> lab la-sass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-schlix"></i> lab la-schlix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-scribd"></i> lab la-scribd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-searchengin"></i> lab la-searchengin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sellcast"></i> lab la-sellcast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sellsy"></i> lab la-sells
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-servicestack"></i> lab la-servicestack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-shirtsinbulk"></i> lab la-shirtsinbulk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-shopware"></i> lab la-shopware
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-simplybuilt"></i> lab la-simplybuilt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sith"></i> lab la-sith
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sketch"></i> lab la-sketch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-skyatlas"></i> lab la-skyatlas
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-skype"></i> lab la-skype
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slack"></i> lab la-slack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slack-hash"></i> lab la-slack-has
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slideshare"></i> lab la-slideshare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat"></i> lab la-snapchat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat-ghost"></i> lab la-snapchat-ghos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat-square"></i> lab la-snapchat-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sourcetree"></i> lab la-sourcetree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-speakap"></i> lab la-speakap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-speaker-deck"></i> lab la-speaker-deck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-squarespace"></i> lab la-squarespace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stack-exchange"></i> lab la-stack-exchange
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stack-overflow"></i> lab la-stack-overflow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stackpath"></i> lab la-stackpath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-staylinked"></i> lab la-staylinked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sticker-mule"></i> lab la-sticker-mule
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-strava"></i> lab la-strava
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-studiovinari"></i> lab la-studiovinari
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stumbleupon"></i> lab la-stumbleupon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stumbleupon-circle"></i> lab la-stumbleupon-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-superpowers"></i> lab la-superpowers
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-supple"></i> lab la-supple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-suse"></i> lab la-suse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-swift"></i> lab la-swift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-symfony"></i> lab la-symfony
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-teamspeak"></i> lab la-teamspeak
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-telegram"></i> lab la-telegram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-telegram-plane"></i> lab la-telegram-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tencent-weibo"></i> lab la-tencent-weibo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-the-red-yeti"></i> lab la-the-red-yeti
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-themeco"></i> lab la-themeco
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-themeisle"></i> lab la-themeisle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-think-peaks"></i> lab la-think-peaks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-trade-federation"></i> lab la-trade-federation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-trello"></i> lab la-trello
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tripadvisor"></i> lab la-tripadvisor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tumblr"></i> lab la-tumblr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tumblr-square"></i> lab la-tumblr-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-twitter"></i>lab la-twitter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-twitter-square"></i>lab la-twitter-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-typo3"></i> lab la-typo3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uber"></i> lab la-uber
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ubuntu"></i> lab la-ubuntu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uikit"></i> lab la-uikit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-umbraco"></i> lab la-umbraco
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uniregistry"></i> lab la-uniregistry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-untappd"></i> lab la-untappd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ups"></i> lab la-ups
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-usb"></i> lab la-usb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-usps"></i> lab la-usps
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ussunnah"></i> lab la-ussunnah
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vaadin"></i> lab la-vaadin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viacoin"></i> lab la-viacoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viadeo"></i> lab la-viadeo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viadeo-square"></i> lab la-viadeo-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viber"></i> lab la-viber
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo"></i> lab la-vimeo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo-square"></i> lab la-vimeo-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo-v"></i> lab la-vimeo-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vine"></i> lab la-vine
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vk"></i> lab la-vk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vnv"></i> lab la-vnv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vuejs"></i> lab la-vuejs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-waze"></i> lab la-waze
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weebly"></i> lab la-weebly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weibo"></i> lab la-weibo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weixin"></i> lab la-weixin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whatsapp"></i> lab la-whatsapp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whatsapp-square"></i> lab la-whatsapp-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whmcs"></i> lab la-whmcs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wikipedia-w"></i> lab la-wikipedia-w
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-windows"></i> lab la-windows
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wix"></i> lab la-wix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wolf-pack-battalion"></i> lab la-wolf-pack-battalion
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wordpress"></i> lab la-wordpress
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wordpress-simple"></i> lab la-wordpress-simple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpbeginner"></i> lab la-wpbeginner
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpexplorer"></i> lab la-wpexplorer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpforms"></i> lab la-wpforms
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpressr"></i> lab la-wpressr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-xing"></i> lab la-xing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-xing-square"></i> lab la-xing-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-y-combinator"></i> lab la-y-combinator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yahoo"></i> lab la-yahoo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yammer"></i> lab la-yammer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yandex"></i> lab la-yandex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yandex-international"></i> lab la-yandex-international
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yarn"></i> lab la-yarn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yelp"></i> lab la-yelp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yoast"></i> lab la-yoast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-youtube-square"></i> lab la-youtube-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-zhihu"></i> lab la-zhihu
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Buildings</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archway"></i> las la-archway
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-building"></i> las la-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-campground"></i> las la-campgroun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-church"></i> las la-church
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-city"></i> las la-city
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clinic-medical"></i> las la-clinic-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dungeon"></i> las la-dungeon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gopuram"></i> las la-gopuram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-home"></i> las la-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital"></i> las la-hospital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital-alt"></i> las la-hospital-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hotel"></i> las la-hotel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-house-damage"></i> las la-house-damage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-igloo"></i> las la-igloo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-industry"></i> las la-industry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kaaba"></i> las la-kaaba
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-landmark"></i> las la-landmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-monument"></i> las la-monument
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mosque"></i> las la-mosque
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-place-of-worship"></i> las la-place-of-worship
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-school"></i> las la-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-store"></i> las la-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-store-alt"></i> las la-store-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-synagogue"></i> las la-synagogue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-torii-gate"></i> las la-torii-gate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-university"></i> las la-university
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vihara"></i> las la-vihara
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-warehouse"></i> las la-warehouse
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Business</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-book"></i> las la-address-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-card"></i> las la-address-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archive"></i> las la-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale"></i> las la-balance-scale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-left"></i> las la-balance-scale-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-right"></i> las la-balance-scale-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-birthday-cake"></i> las la-birthday-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book"></i> las la-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-briefcase"></i> las la-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-building"></i> las la-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullseye"></i> las la-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-business-time"></i> las la-business-tim
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calculator"></i> las la-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-alt"></i> las la-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-certificate"></i> las la-certificate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-area"></i> las la-chart-area
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-bar"></i> las la-chart-ba
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-line"></i> las la-chart-line
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-pie"></i> las la-chart-pie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-city"></i> las la-city
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard"></i> las la-clipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-columns"></i> las la-columns
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copyright"></i> las la-copyright
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-edit"></i> las la-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope"></i> las la-envelop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-open"></i> las la-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-square"></i> las la-envelope-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eraser"></i> las la-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fax"></i> las la-fax
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-minus"></i> las la-folder-minus"
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-open"></i> las la-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-plus"></i> las la-folder-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glasses"></i> las la-glasses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe"></i> las la-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-highlighter"></i> las la-highlighter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-industry"></i> las la-industry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-landmark"></i> las la-landmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-marker"></i> las la-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paperclip"></i> las la-paperclip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-alt"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-fancy"></i> las la-pen-fancy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-nib"></i> las la-pen-nib
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-square"></i> las la-pen-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-alt"></i> las la-pencil-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-percent"></i> las la-percent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-slash"></i> las la-phone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square"></i> las la-phone-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square-alt"></i> las la-phone-square-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-volume"></i> las la-phone-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-project-diagram"></i> las la-project-diagram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-registered"></i> las la-registered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sitemap"></i> las la-sitemap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-socks"></i> las la-socks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sticky-note"></i> las la-sticky-not
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stream"></i> las la-stream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-table"></i> las la-table
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tag"></i> las la-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tags"></i> las la-tags
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tasks"></i> las la-tasks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbtack"></i> las la-thumbtack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trademark"></i> las la-trademark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wallet"></i> las la-wallet
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Camping</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-binoculars"></i> las la-binoculars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-campground"></i> las la-campground
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire"></i> las la-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6"> las la-fire-alt
                                <i class="las la-fire-alt"></i>
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-first-aid"></i> las la-first-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frog"></i> las la-frog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hiking"></i> las la-hiking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map"></i> las la-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marked"></i> las la-map-marked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-signs"></i> las la-map-signs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mountain"></i> las la-mountain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-route"></i> las la-route
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toilet-paper"></i> las la-toilet-paper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tree"></i> las la-tree
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Charity</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dollar-sign"></i> las la-dollar-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-donate"></i> las la-donate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dove"></i> las la-dove
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gift"></i> las la-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe"></i> las la-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding-heart"></i> las la-hand-holding-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding-usd"></i> las la-hand-holding-usd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hands-helping"></i> las la-hands-helping
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-handshake"></i> las la-handshake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-leaf"></i> las la-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-parachute-box"></i> las la-parachute-box
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-piggy-bank"></i> las la-piggy-bank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ribbon"></i> las la-ribbon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-seedling"></i> las la-seedling
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Chat</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment"></i> las la-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-alt"></i> las la-comment-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-dots"></i> las la-comment-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-medical"></i> las la-comment-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-slash"></i> las la-comment-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comments"></i> las la-comments
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frown"></i> las la-frown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-icons"></i> las la-icons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meh"></i> las la-meh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-slash"></i> las la-phone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poo"></i> las la-poo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-left"></i> las la-quote-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-right"></i> las la-quote-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile"></i> las la-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sms"></i> las la-sms
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video"></i> las la-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video-slash"></i> las la-video-slash
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Chess</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess"></i> las la-chess
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-bishop"></i> las la-chess-bishop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-board"></i> las la-chess-board
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-king"></i> las la-chess-king
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-knight"></i> las la-chess-knight
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-pawn"></i> las la-chess-pawn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-queen"></i> las la-chess-queen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-rook"></i> las la-chess-rook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-square-full"></i> las la-square-full
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Childhood</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-apple-alt"></i> las la-apple-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baby"></i> las la-baby
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baby-carriage"></i> las la-baby-carriage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-biking"></i> las la-biking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-birthday-cake"></i> las la-birthday-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie"></i> las la-cookie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie-bite"></i> las la-cookie-bite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gamepad"></i> las la-gamepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ice-cream"></i> las la-ice-cream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mitten"></i> las la-mitten
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-robot"></i> las la-robot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-school"></i> las la-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shapes"></i> las la-shapes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowman"></i> las la-snowman
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Clothing</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-graduation-cap"></i> las la-graduation-cap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-cowboy"></i> las la-hat-cowboy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-cowboy-side"></i> las la-hat-cowboy-side
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-wizard"></i> las la-hat-wizard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mitten"></i> las la-mitten
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shoe-prints"></i> las la-shoe-prints
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-socks"></i> las la-socks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tshirt"></i> las la-tshirt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-tie"></i> las la-user-tie
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Code</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archive"></i> las la-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-barcode"></i> las la-barcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bug"></i> las la-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-code"></i> las la-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-code-branch"></i> las la-code-branch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-code"></i> las la-file-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-filter"></i> las la-filter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-extinguisher"></i> las la-fire-extinguisher
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-open"></i> las la-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-keyboard"></i> las la-keyboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laptop-code"></i> las la-laptop-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microchip"></i> las la-microchip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-project-diagram"></i> las la-project-diagram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-qrcode"></i> las la-qrcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shield-alt"></i> las la-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sitemap"></i> las la-sitemap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stream"></i> las la-stream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-terminal"></i> las la-terminal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-secret"></i> las la-user-secret
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-window-close"></i> las la-window-close
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-window-maximize"></i> las la-window-maximize
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-window-minimize"></i> las la-window-minimize
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-window-restore"></i> las la-window-restore
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Communication</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-book"></i> las la-address-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-card"></i> las la-address-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-american-sign-language-interpreting"></i> las
                                la-american-sign-language-interpreting
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-assistive-listening-systems"></i> las la-assistive-listening-systems
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-at"></i> las la-at
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bluetooth"></i> lab la-bluetooth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bluetooth-b"></i> lab la-bluetooth-b
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broadcast-tower"></i> las la-broadcast-tower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chalkboard"></i> las la-chalkboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment"></i> las la-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-alt"></i> las la-comment-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comments"></i> las la-comments
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope"></i> las la-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-open"></i> las la-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-square"></i> las la-envelope-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fax"></i> las la-fax
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-inbox"></i> las la-inbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-language"></i> las la-language
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt-slash"></i> las la-microphone-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-slash"></i> las la-microphone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile"></i> las la-mobile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile-alt"></i> las la-mobile-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paper-plane"></i> las la-paper-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-slash"></i> las la-phone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square"></i> las la-phone-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square-alt"></i> las la-phone-square-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-volume"></i> las la-phone-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss"></i> las la-rss
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss-square"></i> las la-rss-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tty"></i> las la-tty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-voicemail"></i> las la-voicemail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wifi"></i> las la-wifi
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Computers</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-database"></i> las la-database
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-desktop"></i> las la-desktop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-download"></i> las la-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ethernet"></i> las la-ethernet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hdd"></i> las la-hdd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones"></i> las la-headphones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-keyboard"></i> las la-keyboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laptop"></i> las la-laptop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-memory"></i> las la-memory
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microchip"></i> las la-microchip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile"></i> las la-mobile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile-alt"></i> las la-mobile-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mouse"></i> las la-mouse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plug"></i> las la-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-power-off"></i> las la-power-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite"></i> las la-satellite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite-dish"></i> las la-satellite-dish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sd-card"></i> las la-sd-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-server"></i> las la-server
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sim-card"></i> las la-sim-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stream"></i> las la-stream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablet"></i> las la-tablet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablet-alt"></i> las la-tablet-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-upload"></i> las la-upload
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Construction</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-brush"></i> las la-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drafting-compass"></i> las la-drafting-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dumpster"></i> las la-dumpster
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hammer"></i> las la-hammer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hard-hat"></i> las la-hard-hat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paint-roller"></i> las la-paint-roller
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-alt"></i> las la-pencil-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-ruler"></i> las la-pencil-ruler
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler"></i> las la-ruler
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-combined"></i> las la-ruler-combined
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-horizontal"></i> las la-ruler-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-vertical"></i> las la-ruler-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-screwdriver"></i> las la-screwdriver
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toolbox"></i> las la-toolbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tools"></i> las la-tools
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck-pickup"></i> las la-truck-pickup
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wrench"></i> las la-wrench
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Currency</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bitcoin"></i> lab la-bitcoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-btc"></i> lab la-btc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dollar-sign"></i> las la-dollar-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ethereum"></i> lab la-ethereum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-euro-sign"></i> las la-euro-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gg"></i> lab la-gg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gg-circle"></i> lab la-gg-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hryvnia"></i> las la-hryvnia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lira-sign"></i> las la-lira-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill"></i> las la-money-bill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-alt"></i> las la-money-bill-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-wave"></i> las la-money-bill-wave
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-wave-alt"></i> las la-money-bill-wave-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check"></i> las la-money-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check-alt"></i> las la-money-check-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pound-sign"></i> las la-pound-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruble-sign"></i> las la-ruble-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rupee-sign"></i> las la-rupee-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shekel-sign"></i> las la-shekel-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tenge"></i> las la-tenge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-won-sign"></i> las la-won-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-yen-sign"></i> las la-yen-sign
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Date & Time</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-alt"></i> las la-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-check"></i> las la-calendar-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-minus"></i> las la-calendar-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-plus"></i> las la-calendar-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-times"></i> las la-calendar-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clock"></i> las la-clock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hourglass"></i> las la-hourglass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hourglass-end"></i> las la-hourglass-end
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hourglass-half"></i> las la-hourglass-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hourglass-start"></i> las la-hourglass-start
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stopwatch"></i> las la-stopwatch
                            </b-col>
                        </b-row>
                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Design</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-adjust"></i> las la-adjust
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bezier-curve"></i> las la-bezier-curve
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-brush"></i> las la-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clone"></i> las la-clone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crop"></i> las la-crop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crop-alt"></i> las la-crop-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crosshairs"></i> las la-crosshairs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drafting-compass"></i> las la-drafting-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-draw-polygon"></i> las la-draw-polygon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-edit"></i> las la-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eraser"></i> las la-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-dropper"></i> las la-eye-dropper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fill"></i> las la-fill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fill-drip"></i> las la-fill-drip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-highlighter"></i> las la-highlighter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-icons"></i> las la-icons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-layer-group"></i> las la-layer-group
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magic"></i> las la-magic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-marker"></i> las la-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-object-group"></i> las la-object-group
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-object-ungroup"></i> las la-object-ungroup
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paint-brush"></i> las la-paint-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paint-roller"></i> las la-paint-roller
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-palette"></i> las la-palette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-alt"></i> las la-pen-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-fancy"></i> las la-pen-fancy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-nib"></i> las la-pen-nib
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-alt"></i> las la-pencil-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-ruler"></i> las la-pencil-ruler
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-combined"></i> las la-ruler-combined
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-horizontal"></i> las la-ruler-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-vertical"></i> las la-ruler-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-splotch"></i> las la-splotch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spray-can"></i> las la-spray-can
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stamp"></i> las la-stamp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swatchbook"></i> las la-swatchbook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint"></i> las la-tint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint-slash"></i> las la-tint-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vector-square"></i> las la-vector-square
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Editors</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-align-center"></i> las la-align-center
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-align-justify"></i> las la-align-justify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-align-left"></i> las la-align-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-align-right"></i> las la-align-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bold"></i> las la-bold
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-border-all"></i> las la-border-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-border-none"></i> las la-border-none
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-border-style"></i> las la-border-style
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard"></i> las la-clipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clone"></i> las la-clone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-columns"></i> las la-columns
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-edit"></i> las la-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eraser"></i> las la-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-font"></i> las la-font
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glasses"></i> las la-glasses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heading"></i> las la-heading
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-highlighter"></i> las la-highlighter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-i-cursor"></i> las la-i-cursor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-icons"></i> las la-icons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-indent"></i> las la-indent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-italic"></i> las la-italic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-link"></i> las la-link
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-list"></i> las la-list
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-list-alt"></i> las la-list-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-list-ol"></i> las la-list-ol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-list-ul"></i> las la-list-ul
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-marker"></i> las la-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-outdent"></i> las la-outdent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paper-plane"></i> las la-paper-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paperclip"></i> las la-paperclip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paragraph"></i> las la-paragraph
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-alt"></i> las la-pen-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-fancy"></i> las la-pen-fancy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-nib"></i> las la-pen-nib
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-alt"></i> las la-pencil-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-left"></i> las la-quote-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-right"></i> las la-quote-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-reply-all"></i> las la-reply-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-screwdriver"></i> las la-screwdriver
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share"></i> las la-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spell-check"></i> las la-spell-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-strikethrough"></i> las la-strikethrough
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-subscript"></i> las la-subscript
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync"></i> las la-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-text-width"></i> las la-text-width
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-th"></i> las la-th
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-th-large"></i> las la-th-large
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-th-list"></i> las la-th-list
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tools"></i> las la-tools
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash"></i> las la-trash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-alt"></i> las la-trash-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-restore"></i> las la-trash-restore
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-restore-alt"></i> las la-trash-restore-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-underline"></i> las la-underline
                            </b-col>
                            <b-col xl="3" lg="4" sm="6"><i class="las la-undo"></i>
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo-alt"></i> las la-undo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlink"></i> las la-unlink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wrench"></i> las la-wrench
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Education</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-apple-alt"></i> las la-apple-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atom"></i> las la-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-award"></i> las la-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-open"></i> las la-book-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-reader"></i> las la-book-reader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chalkboard"></i> las la-chalkboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chalkboard-teacher"></i> las la-chalkboard-teacher
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-graduation-cap"></i> las la-graduation-cap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laptop-code"></i> las la-laptop-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microscope"></i> las la-microscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-music"></i> las la-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-school"></i> las la-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shapes"></i> las la-shapes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-theater-masks"></i> las la-theater-masks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-graduate"></i> las la-user-graduate
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Emoji</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-angry"></i> las la-angry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dizzy"></i> las la-dizzy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flushed"></i> las la-flushed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frown"></i> las la-frown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frown-open"></i> las la-frown-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grimace"></i> las la-grimace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin"></i> las la-grin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-alt"></i> las la-grin-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-beam"></i> las la-grin-beam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-beam-sweat"></i> las la-grin-beam-sweat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-hearts"></i> las la-grin-hearts
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-squint"></i> las la-grin-squint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-squint-tears"></i> las la-grin-squint-tears
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-stars"></i> las la-grin-stars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-tears"></i> las la-grin-tears
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-tongue"></i> las la-grin-tongue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-tongue-squint"></i> las la-grin-tongue-squint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-tongue-wink"></i> las la-grin-tongue-wink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grin-wink"></i> las la-grin-wink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kiss"></i> las la-kiss
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kiss-beam"></i> las la-kiss-beam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kiss-wink-heart"></i> las la-kiss-wink-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laugh"></i> las la-laugh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laugh-beam"></i> las la-laugh-beam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meh-rolling-eyes"></i> las la-meh-rolling-eyes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sad-cry"></i> las la-sad-cry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sad-tear"></i> las la-sad-tear
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile"></i> las la-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile-beam"></i> las la-smile-beam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile-wink"></i> las la-smile-wink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-surprise"></i> las la-surprise
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tired"></i> las la-tired
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Energy</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atom"></i> las la-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-empty"></i> las la-battery-empty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-full"></i> las la-battery-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-half"></i> las la-battery-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-quarter"></i> las la-battery-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-three-quarters"></i> las la-battery-three-quarters
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broadcast-tower"></i> las la-broadcast-tower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-burn"></i> las la-burn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-charging-station"></i> las la-charging-station
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire"></i> las la-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-alt"></i> las la-fire-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gas-pump"></i> las la-gas-pump
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-industry"></i> las la-industry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-leaf"></i> las la-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lightbulb"></i> las la-lightbulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plug"></i> las la-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poop"></i> las la-poop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-power-off"></i> las la-power-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation"></i> las la-radiation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation-alt"></i> las la-radiation-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-seedling"></i> las la-seedling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-solar-panel"></i> las la-solar-panel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sun"></i> las la-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-water"></i> las la-water
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wind"></i> las la-wind
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Files</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archive"></i> las la-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clone"></i> las la-clone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-archive"></i> las la-file-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-audio"></i> las la-file-audio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-code"></i> las la-file-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-excel"></i> las la-file-excel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-image"></i> las la-file-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-pdf"></i> las la-file-pdf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-powerpoint"></i> las la-file-powerpoint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-video"></i> las la-file-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-word"></i> las la-file-word
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-open"></i> las la-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-photo-video"></i> las la-photo-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sticky-note"></i> las la-sticky-note
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Finance</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale"></i> las la-balance-scale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-left"></i> las la-balance-scale-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-right"></i> las la-balance-scale-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book"></i> las la-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cash-register"></i> las la-cash-register
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-line"></i> las la-chart-line
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chart-pie"></i> las la-chart-pie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coins"></i> las la-coins
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-dollar"></i> las la-comment-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comments-dollar"></i> las la-comments-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-credit-card"></i> las la-credit-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-donate"></i> las la-donate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-invoice"></i> las la-file-invoice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-invoice-dollar"></i> las la-file-invoice-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding-usd"></i> las la-hand-holding-usd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-landmark"></i> las la-landmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill"></i> las la-money-bill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-alt"></i> las la-money-bill-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-wave"></i> las la-money-bill-wave
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-wave-alt"></i> las la-money-bill-wave-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check"></i> las la-money-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check-alt"></i> las la-money-check-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-percentage"></i> las la-percentage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-piggy-bank"></i> las la-piggy-bank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-receipt"></i> las la-receipt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stamp"></i> las la-stamp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wallet"></i> las la-wallet
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Fitness</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bicycle"></i> las la-bicycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bacon"></i> las la-bacon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bone"></i> las la-bone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bread-slice"></i> las la-bread-slice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-candy-cane"></i> las la-candy-cane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-carrot"></i> las la-carrot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cheese"></i> las la-cheese
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-meatball"></i> las la-cloud-meatball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie"></i> las la-cookie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drumstick-bite"></i> las la-drumstick-bite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-egg"></i> las la-egg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fish"></i> las la-fish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hamburger"></i> las la-hamburger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hotdog"></i> las la-hotdog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ice-cream"></i> las la-ice-cream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lemon"></i> las la-lemon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pepper-hot"></i> las la-pepper-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pizza-slice"></i> las la-pizza-slice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-seedling"></i> las la-seedling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stroopwafel"></i> las la-stroopwafel
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Games</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess"></i> las la-chess
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-bishop"></i> las la-chess-bishop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-board"></i> las la-chess-board
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-king"></i> las la-chess-king
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-knight"></i> las la-chess-knight
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-pawn"></i> las la-chess-pawn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-queen"></i> las la-chess-queen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chess-rook"></i> las la-chess-rook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice"></i> las la-dice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d20"></i> las la-dice-d20
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d6"></i> las la-dice-d6
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-five"></i> las la-dice-five
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-four"></i> las la-dice-four
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-one"></i> las la-dice-one
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-six"></i> las la-dice-six
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-three"></i> las la-dice-three
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-two"></i> las la-dice-two
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gamepad"></i> las la-gamepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ghost"></i> las la-ghost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headset"></i> las la-headset
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-playstation"></i> lab la-playstation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-puzzle-piece"></i> las la-puzzle-piece
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-steam"></i> lab la-steam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-steam-square"></i> lab la-steam-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-steam-symbol"></i> lab la-steam-symbol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-twitch"></i> lab la-twitch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-xbox"></i> lab la-xbox
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Genders</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-genderless"></i> las la-genderless
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mars"></i> las la-mars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mars-double"></i> las la-mars-double
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mars-stroke"></i> las la-mars-stroke
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mars-stroke-h"></i> las la-mars-stroke-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mars-stroke-v"></i> las la-mars-stroke-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mercury"></i> las la-mercury
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-neuter"></i> las la-neuter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-transgender"></i> las la-transgender
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-transgender-alt"></i> las la-transgender-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-venus"></i> las la-venus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-venus-double"></i> las la-venus-double
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-venus-mars"></i> las la-venus-mars
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Halloween</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-dead"></i> las la-book-dead
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broom"></i> las la-broom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cat"></i> las la-cat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-moon"></i> las la-cloud-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crow"></i> las la-crow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ghost"></i> las la-ghost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-wizard"></i> las la-hat-wizard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mask"></i> las la-mask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spider"></i> las la-spider
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toilet-paper"></i> las la-toilet-paper
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Hands</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-allergies"></i> las la-allergies
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fist-raised"></i> las la-fist-raised
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding"></i> las la-hand-holding
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding-heart"></i> las la-hand-holding-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-holding-usd"></i> las la-hand-holding-usd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-lizard"></i> las la-hand-lizard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-middle-finger"></i> las la-hand-middle-finger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-paper"></i> las la-hand-paper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-peace"></i> las la-hand-peace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-down"></i> las la-hand-point-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-left"></i> las la-hand-point-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-right"></i> las la-hand-point-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-point-up"></i> las la-hand-point-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-pointer"></i> las la-hand-pointer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-rock"></i> las la-hand-rock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-scissors"></i> las la-hand-scissors
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hand-spock"></i> las la-hand-spock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hands"></i> las la-hands
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hands-helping"></i> las la-hands-helping
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-handshake"></i> las la-handshake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-praying-hands"></i> las la-praying-hands
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-down"></i> las la-thumbs-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-up"></i> las la-thumbs-up
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Health</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-accessible-icon"></i> lab la-accessible-icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ambulance"></i> las la-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-h-square"></i> las la-h-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heartbeat"></i> las la-heartbeat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital"></i> las la-hospital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-medkit"></i> las la-medkit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-square"></i> las la-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-prescription"></i> las la-prescription
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stethoscope"></i> las la-stethoscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-md"></i> las la-user-md
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Holiday</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-candy-cane"></i> las la-candy-cane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-carrot"></i> las la-carrot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie-bite"></i> las la-cookie-bite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gift"></i> las la-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gifts"></i> las la-gifts
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-cheers"></i> las la-glass-cheers
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-holly-berry"></i> las la-holly-berry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mug-hot"></i> las la-mug-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sleigh"></i> las la-sleigh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowman"></i> las la-snowman
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Hotel</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baby-carriage"></i> las la-baby-carriage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-briefcase"></i> las la-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car"></i> las la-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cocktail"></i> las la-cocktail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-concierge-bell"></i> las la-concierge-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice"></i> las la-dice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-five"></i> las la-dice-five
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-closed"></i> las la-door-closed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-open"></i> las la-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dumbbell"></i> las la-dumbbell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini"></i> las la-glass-martini
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini-alt"></i> las la-glass-martini-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hot-tub"></i> las la-hot-tub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hotel"></i> las la-hotel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-infinity"></i> las la-infinity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-key"></i> las la-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-luggage-cart"></i> las la-luggage-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shower"></i> las la-shower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shuttle-van"></i> las la-shuttle-van
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smoking"></i> las la-smoking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smoking-ban"></i> las la-smoking-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowflake"></i> las la-snowflake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spa"></i> las la-spa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase"></i> las la-suitcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase-rolling"></i> las la-suitcase-rolling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimmer"></i> las la-swimmer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimming-pool"></i> las la-swimming-pool
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella-beach"></i> las la-umbrella-beach
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-utensils"></i> las la-utensils
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wifi"></i> las la-wifi
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Household</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">

                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blender"></i> las la-blender
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chair"></i> las la-chair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-couch"></i> las la-couch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-closed"></i> las la-door-closed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-open"></i> las la-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dungeon"></i> las la-dungeon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fan"></i> las la-fan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shower"></i> las la-shower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toilet-paper"></i> las la-toilet-paper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Images</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-adjust"></i> las la-adjust
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bolt"></i> las la-bolt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera"></i> las la-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera-retro"></i> las la-camera-retro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chalkboard"></i> las la-chalkboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clone"></i> las la-clone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compress"></i> las la-compress
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compress-arrows-alt"></i> las la-compress-arrows-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-expand"></i> las la-expand
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-dropper"></i> las la-eye-dropper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-image"></i> las la-file-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-film"></i> las la-film
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-badge"></i> las la-id-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card"></i> las la-id-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-image"></i> las la-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-images"></i> las la-images
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-photo-video"></i> las la-photo-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-portrait"></i> las la-portrait
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sliders-h"></i> las la-sliders-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint"></i> las la-tint
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Interfaces</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-award"></i> las la-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ban"></i> las la-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-barcode"></i> las la-barcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bars"></i> las la-bars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-beer"></i> las la-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blog"></i> las la-blog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bug"></i> las la-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullseye"></i> las la-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calculator"></i> las la-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-alt"></i> las la-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-check"></i> las la-calendar-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-minus"></i> las la-calendar-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-plus"></i> las la-calendar-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-times"></i> las la-calendar-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-certificate"></i> las la-certificate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-check"></i> las la-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-check-circle"></i> las la-check-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-check-double"></i> las la-check-double
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-check-square"></i> las la-check-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-circle"></i> las la-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard"></i> las la-clipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clone"></i> las la-clone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-download-alt"></i> las la-cloud-download-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-upload-alt"></i> las la-cloud-upload-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cog"></i> las la-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cogs"></i> las la-cogs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-database"></i> las la-database
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dot-circle"></i> las la-dot-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-download"></i> las la-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-edit"></i> las la-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ellipsis-h"></i> las la-ellipsis-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ellipsis-v"></i> las la-ellipsis-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope"></i> las la-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-open"></i> las la-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eraser"></i> las la-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation"></i> las la-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-circle"></i> las la-exclamation-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-triangle"></i> las la-exclamation-triangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-external-link-alt"></i> las la-external-link-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-external-link-square-alt"></i> las la-external-link-square-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-download"></i> las la-file-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-export"></i> las la-file-export
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-import"></i> las la-file-import
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-upload"></i> las la-file-upload
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-filter"></i> las la-filter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fingerprint"></i> las la-fingerprint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag"></i> las la-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag-checkered"></i> las la-flag-checkered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-open"></i> las la-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frown"></i> las la-frown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glasses"></i> las la-glasses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grip-horizontal"></i> las la-grip-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grip-lines"></i> las la-grip-lines
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grip-lines-vertical"></i> las la-grip-lines-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-grip-vertical"></i> las la-grip-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hashtag"></i> las la-hashtag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-history"></i> las la-history
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-home"></i> las la-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-i-cursor"></i> las la-i-cursor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info"></i> las la-info
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info-circle"></i> las la-info-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-language"></i> las la-language
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magic"></i> las la-magic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-marker"></i> las la-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-medal"></i> las la-medal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meh"></i> las la-meh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-slash"></i> las la-microphone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus"></i> las la-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus-circle"></i> las la-minus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus-square"></i> las la-minus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-alt"></i> las la-pen-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen-fancy"></i> las la-pen-fancy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pencil-alt"></i> las la-pencil-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus"></i> las la-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-circle"></i> las la-plus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-square"></i> las la-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poo"></i> las la-poo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-qrcode"></i> las la-qrcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question"></i> las la-question
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question"></i> las la-question
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question-circle"></i> las la-question-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-left"></i> las la-quote-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quote-right"></i> las la-quote-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo"></i> las la-redo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-redo-alt"></i> las la-redo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-reply"></i> las la-reply
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-reply-all"></i> las la-reply-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss"></i> las la-rss
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rss-square"></i> las la-rss-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-screwdriver"></i> las la-screwdriver
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search"></i> las la-search
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-minus"></i> las la-search-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-plus"></i> las la-search-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share"></i> las la-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-alt"></i> las la-share-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-alt-square"></i> las la-share-alt-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-square"></i> las la-share-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shield-alt"></i> las la-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-in-alt"></i> las la-sign-in-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-out-alt"></i> las la-sign-out-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-signal"></i> las la-signal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sitemap"></i> las la-sitemap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sliders-h"></i> las la-sliders-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile"></i> las la-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort"></i> las la-sort
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-down"></i> las la-sort-alpha-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-down-alt"></i> las la-sort-alpha-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-up"></i> las la-sort-alpha-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-alpha-up-alt"></i> las la-sort-alpha-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-down"></i> las la-sort-amount-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-amount-down-alt"></i> las la-sort-amount-down-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-up"></i> las la-sort-numeric-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-numeric-up-alt"></i> las la-sort-numeric-up-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sort-up"></i> las la-sort-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-half"></i> las la-star-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync"></i> las la-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync-alt"></i> las la-sync-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-down"></i> las la-thumbs-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-up"></i> las la-thumbs-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-times"></i> las la-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-times-circle"></i> las la-times-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toggle-off"></i> las la-toggle-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toggle-on"></i> las la-toggle-on
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tools"></i> las la-tools
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash"></i> las la-trash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-alt"></i> las la-trash-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-restore"></i> las la-trash-restore
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-restore-alt"></i> las la-trash-restore-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trophy"></i> las la-trophy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo"></i> las la-undo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-undo-alt"></i> las la-undo-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-upload"></i> las la-upload
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user"></i> las la-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-alt"></i> las la-user-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-circle"></i> las la-user-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-down"></i> las la-volume-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-mute"></i> las la-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-off"></i> las la-volume-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-up"></i> las la-volume-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wifi"></i> las la-wifi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wrench"></i> las la-wrench
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Logistics</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-box"></i> las la-box
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-boxes"></i> las la-boxes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard-check"></i> las la-clipboard-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard-list"></i> las la-clipboard-list
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dolly"></i> las la-dolly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dolly-flatbed"></i> las la-dolly-flatbed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hard-hat"></i> las la-hard-hat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pallet"></i> las la-pallet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shipping-fast"></i> las la-shipping-fast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck"></i> las la-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-warehouse"></i> las la-warehouse
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Maps</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ambulance"></i> las la-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-anchor"></i> las la-anchor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale"></i> las la-balance-scale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-left"></i> las la-balance-scale-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-right"></i> las la-balance-scale-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-beer"></i> las la-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bicycle"></i> las la-bicycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-binoculars"></i> las la-binoculars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-birthday-cake"></i> las la-birthday-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blind"></i> las la-blind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bomb"></i> las la-bomb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book"></i> las la-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bookmark"></i> las la-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-briefcase"></i> las la-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-building"></i> las la-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car"></i> las la-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crosshairs"></i> las la-crosshairs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-directions"></i> las la-directions
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dollar-sign"></i> las la-dollar-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-draw-polygon"></i> las la-draw-polygon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fighter-jet"></i> las la-fighter-jet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire"></i> las la-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-alt"></i> las la-fire-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-extinguisher"></i> las la-fire-extinguisher
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag"></i> las la-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag-checkered"></i> las la-flag-checkered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flask"></i> las la-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gamepad"></i> las la-gamepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gavel"></i> las la-gavel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gift"></i> las la-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini"></i> las la-glass-martini
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe"></i> las la-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-graduation-cap"></i> las la-graduation-cap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-h-square"></i> las la-h-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heartbeat"></i> las la-heartbeat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-helicopter"></i> las la-helicopter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-home"></i> las la-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital"></i> las la-hospital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-image"></i> las la-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-images"></i> las la-images
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-industry"></i> las la-industry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info"></i> las la-info
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info-circle"></i> las la-info-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-key"></i> las la-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-landmark"></i> las la-landmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-layer-group"></i> las la-layer-group
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-leaf"></i> las la-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lemon"></i> las la-lemon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-life-ring"></i> las la-life-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lightbulb"></i> las la-lightbulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-location-arrow"></i> las la-location-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-low-vision"></i> las la-low-vision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magnet"></i> las la-magnet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-male"></i> las la-male
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map"></i> las la-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker"></i> las la-map-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker-alt"></i> las la-map-marker-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-pin"></i> las la-map-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-signs"></i> las la-map-signs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-medkit"></i> las la-medkit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill"></i> las la-money-bill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-alt"></i> las la-money-bill-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-motorcycle"></i> las la-motorcycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-music"></i> las la-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-newspaper"></i> las la-newspaper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-parking"></i> las la-parking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paw"></i> las la-paw
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square"></i> las la-phone-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-square-alt"></i> las la-phone-square-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-volume"></i> las la-phone-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plane"></i> las la-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plug"></i> las la-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus"></i> las la-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-square"></i> las la-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-recycle"></i> las la-recycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-restroom"></i> las la-restroom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-road"></i> las la-road
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rocket"></i> las la-rocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-route"></i> las la-route
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search"></i> las la-search
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-minus"></i> las la-search-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-plus"></i> las la-search-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ship"></i> las la-ship
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shoe-prints"></i> las la-shoe-prints
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-bag"></i> las la-shopping-bag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-basket"></i> las la-shopping-basket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-cart"></i> las la-shopping-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shower"></i> las la-shower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowplow"></i> las la-snowplow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-street-view"></i> las la-street-view
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-subway"></i> las la-subway
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase"></i> las la-suitcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tag"></i> las la-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tags"></i> las la-tags
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-taxi"></i> las la-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbtack"></i> las la-thumbtack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ticket-alt"></i> las la-ticket-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint"></i> las la-tint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-traffic-light"></i> las la-traffic-light
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-train"></i> las la-train
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tram"></i> las la-tram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tree"></i> las la-tree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trophy"></i> las la-trophy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck"></i> las la-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck"></i> las la-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tty"></i> las la-tty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella"></i> las la-umbrella
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-university"></i> las la-university
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-utensil-spoon"></i> las la-utensil-spoon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-utensils"></i> las la-utensils
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wifi"></i> las la-wifi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass"></i> las la-wine-glass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wrench"></i> las la-wrench
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Maritime</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-anchor"></i> las la-anchor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-binoculars"></i> las la-binoculars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dharmachakra"></i> las la-dharmachakra
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frog"></i> las la-frog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ship"></i> las la-ship
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimmer"></i> las la-swimmer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-water"></i> las la-water
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wind"></i> las la-wind
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Marketing</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ad"></i> las la-ad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullseye"></i> las la-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-dollar"></i> las la-comment-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">3
                                <i class="las la-comments-dollar"></i> las la-comments-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-open-text"></i> las la-envelope-open-text
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-funnel-dollar"></i> las la-funnel-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lightbulb"></i> las la-lightbulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mail-bulk"></i> las la-mail-bulk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poll"></i> las la-poll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poll-h"></i> las la-poll-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-dollar"></i> las la-search-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search-location"></i> las la-search-location
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Mathematics</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calculator"></i> las la-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-divide"></i> las la-divide
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-equals"></i> las la-equals
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-greater-than"></i> las la-greater-than
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-greater-than-equal"></i> las la-greater-than-equal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-infinity"></i> las la-infinity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-less-than"></i> las la-less-than
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-less-than-equal"></i> las la-less-than-equal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus"></i> las la-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-not-equal"></i> las la-not-equal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-percentage"></i> las la-percentage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus"></i> las la-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-square-root-alt"></i> las la-square-root-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-subscript"></i> las la-subscript
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-superscript"></i> las la-superscript
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-times"></i> las la-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wave-square"></i> las la-wave-square
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Medical</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-allergies"></i> las la-allergies
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ambulance"></i> las la-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-band-aid"></i> las la-band-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-biohazard"></i> las la-biohazard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bone"></i> las la-bone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bong"></i> las la-bong
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-medical"></i> las la-book-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-brain"></i> las la-brain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-briefcase-medical"></i> las la-briefcase-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-burn"></i> las la-burn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cannabis"></i> las la-cannabis
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-capsules"></i> las la-capsules
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clinic-medical"></i> las la-clinic-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-medical"></i> las la-comment-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crutch"></i> las la-crutch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-diagnoses"></i> las la-diagnoses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dna"></i> las la-dna
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-medical"></i> las la-file-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-medical-alt"></i> las la-file-medical-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-prescription"></i> las la-file-prescription
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-first-aid"></i> las la-first-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heartbeat"></i> las la-heartbeat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital"></i> las la-hospital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital-alt"></i> las la-hospital-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital-symbol"></i> las la-hospital-symbol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card-alt"></i> las la-id-card-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-joint"></i> las la-joint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laptop-medical"></i> las la-laptop-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microscope"></i> las la-microscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mortar-pestle"></i> las la-mortar-pestle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-notes-medical"></i> las la-notes-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pager"></i> las la-pager
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pills"></i> las la-pills
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus"></i> las la-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poop"></i> las la-poop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-prescription"></i> las la-prescription
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-prescription-bottle"></i> las la-prescription-bottle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-prescription-bottle-alt"></i> las la-prescription-bottle-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-procedures"></i> las la-procedures
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation"></i> las la-radiation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation-alt"></i> las la-radiation-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smoking"></i> las la-smoking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smoking-ban"></i> las la-smoking-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-of-life"></i> las la-star-of-life
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stethoscope"></i> las la-stethoscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-syringe"></i> las la-syringe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablets"></i> las la-tablets
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-teeth"></i> las la-teeth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-teeth-open"></i> las la-teeth-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer"></i> las la-thermometer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tooth"></i> las la-tooth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-md"></i> las la-user-md
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-nurse"></i> las la-user-nurse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vial"></i> las la-vial
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vials"></i> las la-vials
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-weight"></i> las la-weight
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-x-ray"></i> las la-x-ray
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Moving</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archive"></i> las la-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-box-open"></i> las la-box-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-couch"></i> las la-couch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dolly"></i> las la-dolly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-people-carry"></i> las la-people-carry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-route"></i> las la-route
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign"></i> las la-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase"></i> las la-suitcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tape"></i> las la-tape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck-loading"></i> las la-truck-loading
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck-moving"></i> las la-truck-moving
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass"></i> las la-wine-glass
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Music</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drum"></i> las la-drum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drum-steelpan"></i> las la-drum-steelpan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-audio"></i> las la-file-audio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-guitar"></i> las la-guitar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones"></i> las la-headphones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones-alt"></i> las la-headphones-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt-slash"></i> las la-microphone-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-slash"></i> las la-microphone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-music"></i> las la-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-napster"></i> lab la-napster
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-play"></i> las la-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-record-vinyl"></i> las la-record-vinyl
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sliders-h"></i> las la-sliders-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-soundcloud"></i> lab la-soundcloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-spotify"></i> lab la-spotify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-down"></i> las la-volume-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-mute"></i> las la-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-off"></i> las la-volume-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-up"></i> las la-volume-up
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Objects</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ambulance"></i> las la-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-anchor"></i> las la-anchor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archive"></i> las la-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-award"></i> las la-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baby-carriage"></i> las la-baby-carriage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale"></i> las la-balance-scale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-left"></i> las la-balance-scale-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-right"></i> las la-balance-scale-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bath"></i> las la-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-beer"></i> las la-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bicycle"></i> las la-bicycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-binoculars"></i> las la-binoculars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-birthday-cake"></i> las la-birthday-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blender"></i> las la-blender
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bomb"></i> las la-bomb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book"></i> las la-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-dead"></i> las la-book-dead
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bookmark"></i> las la-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-briefcase"></i> las la-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broadcast-tower"></i> las la-broadcast-tower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bug"></i> las la-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-building"></i> las la-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullseye"></i> las la-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bus"></i> las la-bus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calculator"></i> las la-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-alt"></i> las la-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera"></i> las la-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera-retro"></i> las la-camera-retro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-candy-cane"></i> las la-candy-cane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-car"></i> las la-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-carrot"></i> las la-carrot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-church"></i> las la-church
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard"></i> las la-clipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud"></i> las la-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-coffee"></i> las la-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cog"></i> las la-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cogs"></i> las la-cogs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie"></i> las la-cookie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cookie-bite"></i> las la-cookie-bite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-copy"></i> las la-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cube"></i> las la-cube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cubes"></i> las la-cubes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cut"></i> las la-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice"></i> las la-dice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d20"></i> las la-dice-d20
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d6"></i> las la-dice-d6
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-five"></i> las la-dice-five
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-four"></i> las la-dice-four
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-one"></i> las la-dice-one
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-six"></i> las la-dice-six
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-three"></i> las la-dice-three
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-two"></i> las la-dice-two
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-digital-tachograph"></i> las la-digital-tachograph
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-closed"></i> las la-door-closed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-open"></i> las la-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drum"></i> las la-drum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-drum-steelpan"></i> las la-drum-steelpan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope"></i> las la-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope-open"></i> las la-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eraser"></i> las la-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-dropper"></i> las la-eye-dropper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fax"></i> las la-fax
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-feather"></i> las la-feather
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-feather-alt"></i> las la-feather-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fighter-jet"></i> las la-fighter-jet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-prescription"></i> las la-file-prescription
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-film"></i> las la-film
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire"></i> las la-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-alt"></i> las la-fire-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-extinguisher"></i> las la-fire-extinguisher
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag"></i> las la-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag-checkered"></i> las la-flag-checkered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flask"></i> las la-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-futbol"></i> las la-futbol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gamepad"></i> las la-gamepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gavel"></i> las la-gavel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gem"></i> las la-gem
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gift"></i> las la-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gifts"></i> las la-gifts
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-cheers"></i> las la-glass-cheers
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini"></i> las la-glass-martini
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-whiskey"></i> las la-glass-whiskey
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glasses"></i> las la-glasses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe"></i> las la-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-graduation-cap"></i> las la-graduation-cap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-guitar"></i> las la-guitar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-wizard"></i> las la-hat-wizard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hdd"></i> las la-hdd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones"></i> las la-headphones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headphones-alt"></i> las la-headphones-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-headset"></i> las la-headset
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart-broken"></i> las la-heart-broken
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-helicopter"></i> las la-helicopter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-highlighter"></i> las la-highlighter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-holly-berry"></i> las la-holly-berry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-home"></i> las la-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hospital"></i> las la-hospital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hourglass"></i> las la-hourglass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-igloo"></i> las la-igloo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-image"></i> las la-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-images"></i> las la-images
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-industry"></i> las la-industry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-key"></i> las la-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-keyboard"></i> las la-keyboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-laptop"></i> las la-laptop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-leaf"></i> las la-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lemon"></i> las la-lemon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-life-ring"></i> las la-life-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lightbulb"></i> las la-lightbulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock"></i> las la-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock-open"></i> las la-lock-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magic"></i> las la-magic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magnet"></i> las la-magnet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map"></i> las la-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker"></i> las la-map-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker-alt"></i> las la-map-marker-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-pin"></i> las la-map-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-signs"></i> las la-map-signs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-marker"></i> las la-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-medal"></i> las la-medal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-medkit"></i> las la-medkit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-memory"></i> las la-memory
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microchip"></i> las la-microchip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mitten"></i> las la-mitten
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile"></i> las la-mobile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mobile-alt"></i> las la-mobile-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill"></i> las la-money-bill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-bill-alt"></i> las la-money-bill-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check"></i> las la-money-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check-alt"></i> las la-money-check-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-moon"></i> las la-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-motorcycle"></i> las la-motorcycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mug-hot"></i> las la-mug-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-newspaper"></i> las la-newspaper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paint-brush"></i> las la-paint-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paper-plane"></i> las la-paper-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paperclip"></i> las la-paperclip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paste"></i> las la-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-paw"></i> las la-paw
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pen"></i> las la-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plane"></i> las la-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plug"></i> las la-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-puzzle-piece"></i> las la-puzzle-piece
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ring"></i> las la-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-road"></i> las la-road
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rocket"></i> las la-rocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-combined"></i> las la-ruler-combined
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-horizontal"></i> las la-ruler-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ruler-vertical"></i> las la-ruler-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite"></i> las la-satellite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite-dish"></i> las la-satellite-dish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-save"></i> las la-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-school"></i> las la-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-screwdriver"></i> las la-screwdriver
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-scroll"></i> las la-scroll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sd-card"></i> las la-sd-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-search"></i> las la-search
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shield-alt"></i> las la-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-bag"></i> las la-shopping-bag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-basket"></i> las la-shopping-basket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-cart"></i> las la-shopping-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shower"></i> las la-shower
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sim-card"></i> las la-sim-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sleigh"></i> las la-sleigh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowflake"></i> las la-snowflake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowplow"></i> las la-snowplow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-space-shuttle"></i> las la-space-shuttle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sticky-note"></i> las la-sticky-note
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stopwatch"></i> las la-stopwatch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stroopwafel"></i> las la-stroopwafel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-subway"></i> las la-subway
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase"></i> las la-suitcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sun"></i> las la-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablet"></i> las la-tablet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablet-alt"></i> las la-tablet-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tachometer-alt"></i> las la-tachometer-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tag"></i> las la-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tags"></i> las la-tags
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-taxi"></i> las la-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbtack"></i> las la-thumbtack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ticket-alt"></i> las la-ticket-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toilet"></i> las la-toilet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toolbox"></i> las la-toolbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tools"></i> las la-tools
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-train"></i> las la-train
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tram"></i> las la-tram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash"></i> las la-trash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trash-alt"></i> las la-trash-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tree"></i> las la-tree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trophy"></i> las la-trophy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-truck"></i> las la-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella"></i> las la-umbrella
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-university"></i> las la-university
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock"></i> las la-unlock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock-alt"></i> las la-unlock-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-utensil-spoon"></i> las la-utensil-spoon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-utensils"></i> las la-utensils
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wallet"></i> las la-wallet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-weight"></i> las la-weight
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass"></i> las la-wine-glass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wrench"></i> las la-wrench
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Other</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-500px"></i> lab la-500px
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-accusoft"></i> lab la-accusoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adn"></i> lab la-adn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adobe"></i> lab la-adobe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-adversal"></i> lab la-adversal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-affiliatetheme"></i> lab la-affiliatetheme
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-airbnb"></i> lab la-airbnb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-algolia"></i> lab la-algolia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-amazon"></i> lab la-amazon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-amilia"></i> lab la-amilia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-android"></i> lab la-android
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angellist"></i> lab la-angellist
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angrycreative"></i> lab la-angrycreative
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-angular"></i> lab la-angular
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-app-store"></i> lab la-app-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-app-store-ios"></i> lab la-app-store-ios
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-apper"></i> lab la-apper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-apple"></i> lab la-apple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-artstation"></i> lab la-artstation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-asymmetrik"></i> lab la-asymmetrik
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-atlassian"></i> lab la-atlassian
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-audible"></i> lab la-audible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-autoprefixer"></i> lab la-autoprefixer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-avianex"></i> lab la-avianex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-aviato"></i> lab la-aviato
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-aws"></i> lab la-aws
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-backspace"></i> las la-backspace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bandcamp"></i> lab la-bandcamp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-battle-net"></i> lab la-battle-net
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-behance"></i> lab la-behance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-behance-square"></i> lab la-behance-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-behance-square"></i> lab la-behance-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bimobject"></i> lab la-bimobject
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bitbucket"></i> lab la-bitbucket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bity"></i> lab la-bity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-black-tie"></i> lab la-black-tie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blackberry"></i> lab la-blackberry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blender-phone"></i> las la-blender-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blogger"></i> lab la-blogger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-blogger-b"></i> lab la-blogger-b
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bootstrap"></i> lab la-bootstrap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buffer"></i> lab la-buffer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buromobelexperte"></i> lab la-buromobelexperte
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buy-n-large"></i> lab la-buy-n-large
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-buysellads"></i> lab la-buysellads
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-canadian-maple-leaf"></i> lab la-canadian-maple-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-centercode"></i> lab la-centercode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-centos"></i> lab la-centos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-chrome"></i> lab la-chrome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-chromecast"></i> lab la-chromecast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudscale"></i> lab la-cloudscale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudsmith"></i> lab la-cloudsmith
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cloudversify"></i> lab la-cloudversify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-codepen"></i> lab la-codepen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-codiepie"></i> lab la-codiepie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-confluence"></i> lab la-confluence
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-connectdevelop"></i> lab la-connectdevelop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-contao"></i> lab la-contao
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cotton-bureau"></i> lab la-cotton-bureau
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cpanel"></i> lab la-cpanel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons"></i> lab la-creative-commons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-by"></i> lab la-creative-commons-by
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc"></i> lab la-creative-commons-nc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc-eu"></i> lab la-creative-commons-nc-eu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nc-jp"></i> lab la-creative-commons-nc-jp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-nd"></i> lab la-creative-commons-nd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-pd"></i> lab la-creative-commons-pd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-pd-alt"></i> lab la-creative-commons-pd-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-remix"></i> lab la-creative-commons-remix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sa"></i> lab la-creative-commons-sa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sampling"></i> lab la-creative-commons-sampling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-sampling-plus"></i> lab
                                la-creative-commons-sampling-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-share"></i> lab la-creative-commons-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-creative-commons-zero"></i> lab la-creative-commons-zero
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crown"></i> las la-crown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-css3"></i> lab la-css3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-css3-alt"></i> lab la-css3-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cuttlefish"></i> lab la-cuttlefish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dashcube"></i> lab la-dashcube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-delicious"></i> lab la-delicious
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deploydog"></i> lab la-deploydog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deskpro"></i> lab la-deskpro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dev"></i> lab la-dev
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-deviantart"></i> lab la-deviantart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dhl"></i> lab la-dhl
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-diaspora"></i> lab la-diaspora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-digg"></i> lab la-digg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-digital-ocean"></i> lab la-digital-ocean
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-discord"></i> lab la-discord
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-discourse"></i> lab la-discourse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dochub"></i> lab la-dochub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-docker"></i> lab la-docker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-draft2digital"></i> lab la-draft2digital
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dribbble"></i> lab la-dribbble
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dribbble-square"></i> lab la-dribbble-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dropbox"></i> lab la-dropbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-drupal"></i> lab la-drupal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dumpster-fire"></i> las la-dumpster-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-dyalog"></i> lab la-dyalog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-earlybirds"></i> lab la-earlybirds
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ebay"></i> lab la-ebay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-edge"></i> lab la-edge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-elementor"></i> lab la-elementor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ello"></i> lab la-ello
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ember"></i> lab la-ember
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-empire"></i> lab la-empire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-envira"></i> lab la-envira
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-erlang"></i> lab la-erlang
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-etsy"></i> lab la-etsy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-evernote"></i> lab la-evernote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-expeditedssl"></i> lab la-expeditedssl
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook"></i> lab la-facebook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-f"></i> lab la-facebook-f
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-messenger"></i> lab la-facebook-messenger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-facebook-square"></i> lab la-facebook-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fedex"></i> lab la-fedex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fedora"></i> lab la-fedora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-figma"></i> lab la-figma
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-csv"></i> las la-file-csv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-firefox"></i> lab la-firefox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-first-order"></i> lab la-first-order
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-first-order-alt"></i> lab la-first-order-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-firstdraft"></i> lab la-firstdraft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-flickr"></i> lab la-flickr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-flipboard"></i> lab la-flipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fly"></i> lab la-fly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome"></i> lab la-font-awesome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome-alt"></i> lab la-font-awesome-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-font-awesome-flag"></i> lab la-font-awesome-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fonticons"></i> lab la-fonticons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fonticons-fi"></i> lab la-fonticons-fi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fort-awesome"></i> lab la-fort-awesome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fort-awesome-alt"></i> lab la-fort-awesome-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-forumbee"></i> lab la-forumbee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-foursquare"></i> lab la-foursquare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-free-code-camp"></i> lab la-free-code-camp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-freebsd"></i> lab la-freebsd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fulcrum"></i> lab la-fulcrum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-get-pocket"></i> lab la-get-pocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git"></i> lab la-git
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git-alt"></i> lab la-git-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-git-square"></i> lab la-git-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gitlab"></i> lab la-gitlab
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gitter"></i> lab la-gitter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-glide"></i> lab la-glide
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-glide-g"></i> lab la-glide-g
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gofore"></i> lab la-gofore
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-goodreads"></i> lab la-goodreads
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-goodreads-g"></i> lab la-goodreads-g
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google"></i> lab la-google
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-drive"></i> lab la-google-drive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-play"></i> lab la-google-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus"></i> lab la-google-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus-g"></i> lab la-google-plus-g
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-plus-square"></i> lab la-google-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gratipay"></i> lab la-gratipay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-grav"></i> lab la-grav
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gripfire"></i> lab la-gripfire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-grunt"></i> lab la-grunt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-gulp"></i> lab la-gulp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hacker-news"></i> lab la-hacker-news
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hacker-news-square"></i> lab la-hacker-news-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hackerrank"></i> lab la-hackerrank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hips"></i> lab la-hips
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hire-a-helper"></i> lab la-hire-a-helper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hooli"></i> lab la-hooli
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hornbill"></i> lab la-hornbill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hotjar"></i> lab la-hotjar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-houzz"></i> lab la-houzz
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-html5"></i> lab la-html5
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-hubspot"></i> lab la-hubspot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-imdb"></i> lab la-imdb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-instagram"></i> lab la-instagram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-intercom"></i> lab la-intercom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-internet-explorer"></i> lab la-internet-explorer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-invision"></i> lab la-invision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ioxhost"></i> lab la-ioxhost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itch-io"></i> lab la-itch-io
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itunes"></i> lab la-itunes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-itunes-note"></i> lab la-itunes-note
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-java"></i> lab la-java
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jenkins"></i> lab la-jenkins
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jira"></i> lab la-jira
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-joget"></i> lab la-joget
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-joomla"></i> lab la-joomla
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-js"></i> lab la-js
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-js-square"></i> lab la-js-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jsfiddle"></i> lab la-jsfiddle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kaggle"></i> lab la-kaggle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-keybase"></i> lab la-keybase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-keycdn"></i> lab la-keycdn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kickstarter"></i> lab la-kickstarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-kickstarter-k"></i> lab la-kickstarter-k
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-korvue"></i> lab la-korvue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-laravel"></i> lab la-laravel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lastfm"></i> lab la-lastfm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lastfm-square"></i> lab la-lastfm-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-leanpub"></i> lab la-leanpub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-less"></i> lab la-less
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-line"></i> lab la-line
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linkedin"></i> lab la-linkedin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linkedin-in"></i> lab la-linkedin-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linode"></i> lab la-linode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-linux"></i> lab la-linux
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-lyft"></i> lab la-lyft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-magento"></i> lab la-magento
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mailchimp"></i> lab la-mailchimp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mandalorian"></i> lab la-mandalorian
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-markdown"></i> lab la-markdown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mastodon"></i> lab la-mastodon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-maxcdn"></i> lab la-maxcdn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mdb"></i> lab la-mdb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medapps"></i> lab la-medapps
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medium"></i> lab la-medium
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medium-m"></i> lab la-medium-m
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-medrt"></i> lab la-medrt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-meetup"></i> lab la-meetup
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-megaport"></i> lab la-megaport
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mendeley"></i> lab la-mendeley
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-microsoft"></i> lab la-microsoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-microsoft"></i> lab la-microsoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mix"></i> lab la-mix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mixcloud"></i> lab la-mixcloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-mizuni"></i> lab la-mizuni
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-modx"></i> lab la-modx
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-monero"></i> lab la-monero
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-neos"></i> lab la-neos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-network-wired"></i> las la-network-wired
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-nimblr"></i> lab la-nimblr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-node"></i> lab la-node
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-node-js"></i> lab la-node-js
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-npm"></i> lab la-npm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ns8"></i> lab la-ns8
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-nutritionix"></i> lab la-nutritionix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-odnoklassniki"></i> lab la-odnoklassniki
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-odnoklassniki-square"></i> lab la-odnoklassniki-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-opencart"></i> lab la-opencart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-openid"></i> lab la-openid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-opera"></i> lab la-opera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-optin-monster"></i> lab la-optin-monster
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-orcid"></i> lab la-orcid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-osi"></i> lab la-osi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-page4"></i> lab la-page4
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pagelines"></i> lab la-pagelines
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-palfed"></i> lab la-palfed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-patreon"></i> lab la-patreon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-periscope"></i> lab la-periscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phabricator"></i> lab la-phabricator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phoenix-framework"></i> lab la-phoenix-framework
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-phoenix-squadron"></i> lab la-phoenix-squadron
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-php"></i> lab la-php
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper"></i> lab la-pied-piper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-alt"></i> lab la-pied-piper-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-hat"></i> lab la-pied-piper-hat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pied-piper-pp"></i> lab la-pied-piper-pp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest"></i> lab la-pinterest
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest-p"></i> lab la-pinterest-p
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pinterest-square"></i> lab la-pinterest-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-product-hunt"></i> lab la-product-hunt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-pushed"></i> lab la-pushed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-python"></i> lab la-python
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-qq"></i> lab la-qq
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-quinscape"></i> lab la-quinscape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-quora"></i> lab la-quora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-r-project"></i> lab la-r-project
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-raspberry-pi"></i> lab la-raspberry-pi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ravelry"></i> lab la-ravelry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-react"></i> lab la-react
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reacteurope"></i> lab la-reacteurope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-readme"></i> lab la-readme
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rebel"></i> lab la-rebel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-red-river"></i> lab la-red-river
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit"></i> lab la-reddit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit-alien"></i> lab la-reddit-alien
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-reddit-square"></i> lab la-reddit-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-redhat"></i> lab la-redhat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-renren"></i> lab la-renren
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-replyd"></i> lab la-replyd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-researchgate"></i> lab la-researchgate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-resolving"></i> lab la-resolving
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rev"></i> lab la-rev
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rocketchat"></i> lab la-rocketchat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-rockrms"></i> lab la-rockrms
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-safari"></i> lab la-safari
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-salesforce"></i> lab la-salesforce
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sass"></i> lab la-sass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-schlix"></i> lab la-schlix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-scribd"></i> lab la-scribd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-searchengin"></i> lab la-searchengin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sellcast"></i> lab la-sellcast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sellsy"></i> lab la-sellsy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-servicestack"></i> lab la-servicestack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-shirtsinbulk"></i> lab la-shirtsinbulk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-shopware"></i> lab la-shopware
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-signature"></i> las la-signature
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-simplybuilt"></i> lab la-simplybuilt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sistrix"></i> lab la-sistrix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sith"></i> lab la-sith
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sketch"></i> lab la-sketch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull"></i> las la-skull
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-skyatlas"></i> lab la-skyatlas
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-skype"></i> lab la-skype
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slack"></i> lab la-slack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slack-hash"></i> lab la-slack-hash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-slideshare"></i> lab la-slideshare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat"></i> lab la-snapchat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat-ghost"></i> lab la-snapchat-ghost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-snapchat-square"></i> lab la-snapchat-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sourcetree"></i> lab la-sourcetree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-speakap"></i> lab la-speakap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-speaker-deck"></i> lab la-speaker-deck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-squarespace"></i> lab la-squarespace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stack-exchange"></i> lab la-stack-exchange
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stack-overflow"></i> lab la-stack-overflow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stackpath"></i> lab la-stackpath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-staylinked"></i> lab la-staylinked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-sticker-mule"></i> lab la-sticker-mule
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-strava"></i> lab la-strava
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-studiovinari"></i> lab la-studiovinari
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stumbleupon"></i> lab la-stumbleupon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stumbleupon-circle"></i> lab la-stumbleupon-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-superpowers"></i> lab la-superpowers
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-supple"></i> lab la-supple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-suse"></i> lab la-suse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-swift"></i> lab la-swift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-symfony"></i> lab la-symfony
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-teamspeak"></i> lab la-teamspeak
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-telegram"></i> lab la-telegram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-telegram-plane"></i> lab la-telegram-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tencent-weibo"></i> lab la-tencent-weibo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-the-red-yeti"></i> lab la-the-red-yeti
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-themeco"></i> lab la-themeco
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-themeisle"></i> lab la-themeisle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-think-peaks"></i> lab la-think-peaks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-trade-federation"></i> lab la-trade-federation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-trello"></i> lab la-trello
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tripadvisor"></i> lab la-tripadvisor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tumblr"></i> lab la-tumblr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-tumblr-square"></i> lab la-tumblr-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-twitter"></i> lab la-twitter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-twitter-square"></i> lab la-twitter-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-typo3"></i> lab la-typo3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uber"></i> lab la-uber
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ubuntu"></i> lab la-ubuntu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uikit"></i> lab la-uikit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-umbraco"></i> lab la-umbraco
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-uniregistry"></i> lab la-uniregistry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-untappd"></i> lab la-untappd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ups"></i> lab la-ups
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-usb"></i> lab la-usb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-usps"></i> lab la-usps
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ussunnah"></i> lab la-ussunnah
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vaadin"></i> lab la-vaadin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viacoin"></i> lab la-viacoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viadeo"></i> lab la-viadeo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viadeo-square"></i> lab la-viadeo-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-viber"></i> lab la-viber
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo"></i> lab la-vimeo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo-square"></i> lab la-vimeo-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vimeo-v"></i> lab la-vimeo-v
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vine"></i> lab la-vine
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vk"></i> lab la-vk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vnv"></i> lab la-vnv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vr-cardboard"></i> las la-vr-cardboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-vuejs"></i> lab la-vuejs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-waze"></i> lab la-waze
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weebly"></i> lab la-weebly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weibo"></i> lab la-weibo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-weight-hanging"></i> las la-weight-hanging
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-weixin"></i> lab la-weixin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whatsapp"></i> lab la-whatsapp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whatsapp-square"></i> lab la-whatsapp-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-whmcs"></i> lab la-whmcs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wikipedia-w"></i> lab la-wikipedia-w
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-windows"></i> lab la-windows
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wix"></i> lab la-wix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wolf-pack-battalion"></i> lab la-wolf-pack-battalion
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wordpress"></i> lab la-wordpress
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wordpress-simple"></i> lab la-wordpress-simple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpbeginner"></i> lab la-wpbeginner
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpexplorer"></i> lab la-wpexplorer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpforms"></i> lab la-wpforms
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wpressr"></i> lab la-wpressr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-xing"></i> lab la-xing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-xing-square"></i> lab la-xing-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-y-combinator"></i> lab la-y-combinator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yahoo"></i> lab la-yahoo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yammer"></i> lab la-yammer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yandex"></i> lab la-yandex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yandex-international"></i> lab la-yandex-international
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yarn"></i> lab la-yarn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yelp"></i> lab la-yelp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-yoast"></i> lab la-yoast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-youtube-square"></i> lab la-youtube-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-zhihu"></i> lab la-zhihu
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Payments & Shopping</h6>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-alipay"></i> lab la-alipay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-amazon-pay"></i> lab la-amazon-pay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-apple-pay"></i> lab la-apple-pay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-bitcoin"></i> lab la-bitcoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bookmark"></i> las la-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-btc"></i> lab la-btc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera"></i> las la-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera-retro"></i> las la-camera-retro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cart-arrow-down"></i> las la-cart-arrow-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cart-plus"></i> las la-cart-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-amazon-pay"></i> lab la-cc-amazon-pay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-amex"></i> lab la-cc-amex
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-apple-pay"></i> lab la-cc-apple-pay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-diners-club"></i> lab la-cc-diners-club
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-discover"></i> lab la-cc-discover
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-jcb"></i> lab la-cc-jcb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-mastercard"></i> lab la-cc-mastercard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-paypal"></i> lab la-cc-paypal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-stripe"></i> lab la-cc-stripe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-cc-visa"></i> lab la-cc-visa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-certificate"></i> las la-certificate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-credit-card"></i> las la-credit-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-ethereum"></i> lab la-ethereum
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gem"></i> las la-gem
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gift"></i> las la-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-google-wallet"></i> lab la-google-wallet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-handshake"></i> las la-handshake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-key"></i> las la-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check"></i> las la-money-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-money-check-alt"></i> las la-money-check-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-paypal"></i> lab la-paypal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-receipt"></i> las la-receipt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-bag"></i> las la-shopping-bag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-basket"></i> las la-shopping-basket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-cart"></i> las la-shopping-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stripe"></i> lab la-stripe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-stripe-s"></i> lab la-stripe-s
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tag"></i> las la-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tags"></i> las la-tags
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-down"></i> las la-thumbs-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-up"></i> las la-thumbs-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-trophy"></i> las la-trophy
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Political</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-award"></i> las la-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale"></i> las la-balance-scale
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-left"></i> las la-balance-scale-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-balance-scale-right"></i> las la-balance-scale-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bullhorn"></i> las la-bullhorn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-check-double"></i> las la-check-double
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-democrat"></i> las la-democrat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-donate"></i> las la-donate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dove"></i> las la-dove
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fist-raised"></i> las la-fist-raised
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flag-usa"></i> las la-flag-usa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-handshake"></i> las la-handshake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-person-booth"></i> las la-person-booth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-piggy-bank"></i> las la-piggy-bank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-republican"></i> las la-republican
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vote-yea"></i> las la-vote-yea
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ankh"></i> las la-ankh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atom"></i> las la-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bible"></i> las la-bible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-church"></i> las la-church
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cross"></i> las la-cross
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dharmachakra"></i> las la-dharmachakra
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dove"></i> las la-dove
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gopuram"></i> las la-gopuram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hamsa"></i> las la-hamsa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hanukiah"></i> las la-hanukiah
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-haykal"></i> las la-haykal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-jedi"></i> las la-jedi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-journal-whills"></i> las la-journal-whills
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-kaaba"></i> las la-kaaba
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-khanda"></i> las la-khanda
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-menorah"></i> las la-menorah
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mosque"></i> las la-mosque
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-om"></i> las la-om
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pastafarianism"></i> las la-pastafarianism
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-peace"></i> las la-peace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-place-of-worship"></i> las la-place-of-worship
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pray"></i> las la-pray
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-praying-hands"></i> las la-praying-hands
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quran"></i> las la-quran
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-and-crescent"></i> las la-star-and-crescent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-of-david"></i> las la-star-of-david
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-synagogue"></i> las la-synagogue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-torah"></i> las la-torah
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-torii-gate"></i> las la-torii-gate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vihara"></i> las la-vihara
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-yin-yang"></i> las la-yin-yang
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Science</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atom"></i> las la-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-biohazard"></i> las la-biohazard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-brain"></i> las la-brain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-burn"></i> las la-burn
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-capsules"></i> las la-capsules
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-clipboard-check"></i> las la-clipboard-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dna"></i> las la-dna
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-dropper"></i> las la-eye-dropper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-filter"></i> las la-filter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire"></i> las la-fire
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fire-alt"></i> las la-fire-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-flask"></i> las la-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frog"></i> las la-frog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-magnet"></i> las la-magnet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microscope"></i> las la-microscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mortar-pestle"></i> las la-mortar-pestle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pills"></i> las la-pills
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-prescription-bottle"></i> las la-prescription-bottle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation"></i> las la-radiation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-radiation-alt"></i> las la-radiation-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-seedling"></i> las la-seedling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-syringe"></i> las la-syringe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tablets"></i> las la-tablets
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-temperature-high"></i> las la-temperature-high
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-temperature-low"></i> las la-temperature-low
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vial"></i> las la-vial
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-vials"></i> las la-vials
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-galactic-republic"></i> lab la-galactic-republic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-galactic-senate"></i> lab la-galactic-senate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe"></i> las la-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-jedi"></i> las la-jedi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-jedi-order"></i> lab la-jedi-order
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-journal-whills"></i> las la-journal-whills
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meteor"></i> las la-meteor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-moon"></i> las la-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-old-republic"></i> lab la-old-republic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-robot"></i> las la-robot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rocket"></i> las la-rocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite"></i> las la-satellite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-satellite-dish"></i> las la-satellite-dish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-space-shuttle"></i> las la-space-shuttle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-astronaut"></i> las la-user-astronaut
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ban"></i> las la-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bug"></i> las la-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-closed"></i> las la-door-closed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-open"></i> las la-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dungeon"></i> las la-dungeon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-contract"></i> las la-file-contract
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-signature"></i> las la-file-signature
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fingerprint"></i> las la-fingerprint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-badge"></i> las la-id-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card"></i> las la-id-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card-alt"></i> las la-id-card-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-key"></i> las la-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock"></i> las la-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock-open"></i> las la-lock-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mask"></i> las la-mask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-passport"></i> las la-passport
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shield-alt"></i> las la-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock"></i> las la-unlock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock-alt"></i> las la-unlock-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-lock"></i> las la-user-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-secret"></i> las la-user-secret
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-shield"></i> las la-user-shield
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bookmark"></i> las la-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-certificate"></i> las la-certificate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-circle"></i> las la-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud"></i> las la-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment"></i> las la-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart-broken"></i> las la-heart-broken
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker"></i> las la-map-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-play"></i> las la-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shapes"></i> las la-shapes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-square"></i> las la-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-birthday-cake"></i> las la-birthday-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-camera"></i> las la-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment"></i> las la-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-alt"></i> las la-comment-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-envelope"></i> las la-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hashtag"></i> las la-hashtag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-heart"></i> las la-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-icons"></i> las la-icons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-image"></i> las la-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-images"></i> las la-images
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker"></i> las la-map-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker-alt"></i> las la-map-marker-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-photo-video"></i> las la-photo-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poll"></i> las la-poll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poll-h"></i> las la-poll-h
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-retweet"></i> las la-retweet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share"></i> las la-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-alt"></i> las la-share-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-share-square"></i> las la-share-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-down"></i> las la-thumbs-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-up"></i> las la-thumbs-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbtack"></i> las la-thumbtack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user"></i> las la-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-circle"></i> las la-user-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-friends"></i> las la-user-friends
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-plus"></i> las la-user-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-users"></i> las la-users
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video"></i> las la-video
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-asterisk"></i> las la-asterisk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atom"></i> las la-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-certificate"></i> las la-certificate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-circle-notch"></i> las la-circle-notch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cog"></i> las la-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compact-disc"></i> las la-compact-disc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-crosshairs"></i> las la-crosshairs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dharmachakra"></i> las la-dharmachakra
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fan"></i> las la-fan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-haykal"></i> las la-haykal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-life-ring"></i> las la-life-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-palette"></i> las la-palette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ring"></i> las la-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-slash"></i> las la-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowflake"></i> las la-snowflake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spinner"></i> las la-spinner
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stroopwafel"></i> las la-stroopwafel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sun"></i> las la-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync"></i> las la-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sync-alt"></i> las la-sync-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-yin-yang"></i> las la-yin-yang
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baseball-ball"></i> las la-baseball-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-basketball-ball"></i> las la-basketball-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-biking"></i> las la-biking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bowling-ball"></i> las la-bowling-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dumbbell"></i> las la-dumbbell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-football-ball"></i> las la-football-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-futbol"></i> las la-futbol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-golf-ball"></i> las la-golf-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hockey-puck"></i> las la-hockey-puck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-quidditch"></i> las la-quidditch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-running"></i> las la-running
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skating"></i> las la-skating
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing"></i> las la-skiing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing-nordic"></i> las la-skiing-nordic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowboarding"></i> las la-snowboarding
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimmer"></i> las la-swimmer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-table-tennis"></i> las la-table-tennis
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volleyball-ball"></i> las la-volleyball-ball
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-allergies"></i> las la-allergies
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-broom"></i> las la-broom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-sun"></i> las la-cloud-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-sun-rain"></i> las la-cloud-sun-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frog"></i> las la-frog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rainbow"></i> las la-rainbow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-seedling"></i> las la-seedling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella"></i> las la-umbrella
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ban"></i> las la-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-empty"></i> las la-battery-empty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-full"></i> las la-battery-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-half"></i> las la-battery-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-quarter"></i> las la-battery-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-battery-three-quarters"></i> las la-battery-three-quarters
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell"></i> las la-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bell-slash"></i> las la-bell-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar"></i> las la-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-alt"></i> las la-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-check"></i> las la-calendar-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-day"></i> las la-calendar-day
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-minus"></i> las la-calendar-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-plus"></i> las la-calendar-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-times"></i> las la-calendar-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-calendar-week"></i> las la-calendar-week
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cart-arrow-down"></i> las la-cart-arrow-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cart-plus"></i> las la-cart-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment"></i> las la-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-alt"></i> las la-comment-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-comment-slash"></i> las la-comment-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-compass"></i> las la-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-closed"></i> las la-door-closed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-door-open"></i> las la-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation"></i> las la-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-circle"></i> las la-exclamation-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-exclamation-triangle"></i> las la-exclamation-triangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye"></i> las la-eye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-eye-slash"></i> las la-eye-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file"></i> las la-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-file-alt"></i> las la-file-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder"></i> las la-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-folder-open"></i> las la-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-gas-pump"></i> las la-gas-pump
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info"></i> las la-info
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-info-circle"></i> las la-info-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lightbulb"></i> las la-lightbulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock"></i> las la-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-lock-open"></i> las la-lock-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker"></i> las la-map-marker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marker-alt"></i> las la-map-marker-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone"></i> las la-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt"></i> las la-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-alt-slash"></i> las la-microphone-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-microphone-slash"></i> las la-microphone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus"></i> las la-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus-circle"></i> las la-minus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-minus-square"></i> las la-minus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-parking"></i> las la-parking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone"></i> las la-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-alt"></i> las la-phone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-phone-slash"></i> las la-phone-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus"></i> las la-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-circle"></i> las la-plus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plus-square"></i> las la-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-print"></i> las la-print
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question"></i> las la-question
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-question-circle"></i> las la-question-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shield-alt"></i> las la-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shopping-cart"></i> las la-shopping-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-in-alt"></i> las la-sign-in-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sign-out-alt"></i> las la-sign-out-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-signal"></i> las la-signal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smoking-ban"></i> las la-smoking-ban
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star"></i> las la-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-half"></i> las la-star-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-star-half-alt"></i> las la-star-half-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-stream"></i> las la-stream
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer-empty"></i> las la-thermometer-empty
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer-full"></i> las la-thermometer-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer-half"></i> las la-thermometer-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer-quarter"></i> las la-thermometer-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thermometer-three-quarters"></i> las la-thermometer-three-quarters
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-down"></i> las la-thumbs-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-thumbs-up"></i> las la-thumbs-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint"></i> las la-tint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tint-slash"></i> las la-tint-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toggle-off"></i> las la-toggle-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-toggle-on"></i> las la-toggle-on
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock"></i> las la-unlock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-unlock-alt"></i> las la-unlock-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user"></i> las la-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-alt"></i> las la-user-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-alt-slash"></i> las la-user-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-slash"></i> las la-user-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video"></i> las la-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-video-slash"></i> las la-video-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-down"></i> las la-volume-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-mute"></i> las la-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-off"></i> las la-volume-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-volume-up"></i> las la-volume-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wifi"></i> las la-wifi
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Religion</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-acquisitions-incorporated"></i> lab la-acquisitions-incorporated
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-book-dead"></i> las la-book-dead
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-critical-role"></i> lab la-critical-role
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-d-and-d"></i> lab la-d-and-d
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-d-and-d-beyond"></i> lab la-d-and-d-beyond
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d20"></i> las la-dice-d20
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dice-d6"></i> las la-dice-d6
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dragon"></i> las la-dragon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dungeon"></i> las la-dungeon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-fantasy-flight-games"></i> lab la-fantasy-flight-games
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-fist-raised"></i> las la-fist-raised
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hat-wizard"></i> las la-hat-wizard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-penny-arcade"></i> lab la-penny-arcade
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-ring"></i> las la-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-scroll"></i> las la-scroll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skull-crossbones"></i> las la-skull-crossbones
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-wizards-of-the-coast"></i> lab la-wizards-of-the-coast
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Travel</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-archway"></i> las la-archway
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-atlas"></i> las la-atlas
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bus"></i> las la-bus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bus-alt"></i> las la-bus-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cocktail"></i> las la-cocktail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-concierge-bell"></i> las la-concierge-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-dumbbell"></i> las la-dumbbell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini"></i> las la-glass-martini
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-martini-alt"></i> las la-glass-martini-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe-africa"></i> las la-globe-africa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe-americas"></i> las la-globe-americas
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe-asia"></i> las la-globe-asia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-globe-europe"></i> las la-globe-europe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hot-tub"></i> las la-hot-tub
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hotel"></i> las la-hotel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-luggage-cart"></i> las la-luggage-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map"></i> las la-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marked"></i> las la-map-marked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-map-marked-alt"></i> las la-map-marked-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-monument"></i> las la-monument
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-passport"></i> las la-passport
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plane"></i> las la-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plane-arrival"></i> las la-plane-arrival
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-plane-departure"></i> las la-plane-departure
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-shuttle-van"></i> las la-shuttle-van
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-spa"></i> las la-spa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase"></i> las la-suitcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-suitcase-rolling"></i> las la-suitcase-rolling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimmer"></i> las la-swimmer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimming-pool"></i> las la-swimming-pool
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-taxi"></i> las la-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tram"></i> las la-tram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tv"></i> las la-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella-beach"></i> las la-umbrella-beach
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass"></i> las la-wine-glass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wine-glass-alt"></i> las la-wine-glass-alt
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Users & People</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="lab la-accessible-icon"></i> lab la-accessible-icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-book"></i> las la-address-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-address-card"></i> las la-address-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-baby"></i> las la-baby
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bed"></i> las la-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-biking"></i> las la-biking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-blind"></i> las la-blind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-chalkboard-teacher"></i> las la-chalkboard-teacher
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-child"></i> las la-child
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-female"></i> las la-female
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-frown"></i> las la-frown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-hiking"></i> las la-hiking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-badge"></i> las la-id-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card"></i> las la-id-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-id-card-alt"></i> las la-id-card-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-male"></i> las la-male
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meh"></i> las la-meh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-people-carry"></i> las la-people-carry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-person-booth"></i> las la-person-booth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poo"></i> las la-poo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-portrait"></i> las la-portrait
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-power-off"></i> las la-power-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-pray"></i> las la-pray
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-restroom"></i> las la-restroom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-running"></i> las la-running
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skating"></i> las la-skating
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing"></i> las la-skiing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing-nordic"></i> las la-skiing-nordic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smile"></i> las la-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowboarding"></i> las la-snowboarding
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-street-view"></i> las la-street-view
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-swimmer"></i> las la-swimmer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user"></i> las la-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-alt"></i> las la-user-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-alt-slash"></i> las la-user-alt-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-astronaut"></i> las la-user-astronaut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-check"></i> las la-user-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-circle"></i> las la-user-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-clock"></i> las la-user-clock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-cog"></i> las la-user-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-edit"></i> las la-user-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-friends"></i> las la-user-friends
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-graduate"></i> las la-user-graduate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-injured"></i> las la-user-injured
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-lock"></i> las la-user-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-md"></i> las la-user-md
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-minus"></i> las la-user-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-ninja"></i> las la-user-ninja
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-nurse"></i> las la-user-nurse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-plus"></i> las la-user-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-secret"></i> las la-user-secret
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-shield"></i> las la-user-shield
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-slash"></i> las la-user-slash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-tag"></i> las la-user-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-tie"></i> las la-user-tie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-user-times"></i> las la-user-times
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-users"></i> las la-users
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-users-cog"></i> las la-users-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-walking"></i> las la-walking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wheelchair"></i> las la-wheelchair
                            </b-col>
                        </b-row>

                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Weather</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-bolt"></i> las la-bolt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud"></i> las la-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-meatball"></i> las la-cloud-meatball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-moon"></i> las la-cloud-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-moon-rain"></i> las la-cloud-moon-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-rain"></i> las la-cloud-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-showers-heavy"></i> las la-cloud-showers-heavy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-sun"></i> las la-cloud-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-cloud-sun-rain"></i> las la-cloud-sun-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-meteor"></i> las la-meteor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-moon"></i> las la-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-poo-storm"></i> las la-poo-storm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-rainbow"></i> las la-rainbow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-smog"></i> las la-smog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowflake"></i> las la-snowflake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-sun"></i> las la-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-temperature-high"></i> las la-temperature-high
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-temperature-low"></i> las la-temperature-low
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-umbrella"></i> las la-umbrella
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-water"></i> las la-water
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-wind"></i> las la-wind
                            </b-col>
                        </b-row>


                        <h6 class="text-uppercase text-muted fw-semibold mt-4">Winter</h6>
                        <b-row>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-glass-whiskey"></i> las la-glass-whiskey
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-icicles"></i> las la-icicles
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-igloo"></i> las la-igloo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-mitten"></i> las la-mitten
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skating"></i> las la-skating
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing"></i> las la-skiing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-skiing-nordic"></i> las la-skiing-nordic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowboarding"></i> las la-snowboarding
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-snowplow"></i> las la-snowplow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="las la-tram"></i> las la-tram
                            </b-col>
                        </b-row>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>
