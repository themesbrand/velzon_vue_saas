<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Boxicons",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Boxicons",
            items: [
                {
                    text: "Icons",
                    href: "/",
                },
                {
                    text: "Boxicons",
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
            <b-col cols="12">
                <b-card no-body>
                    <b-card-header>
                        <h4 class="card-title">Examples</h4>
                        <p class="text-muted mb-0">Use <code>&lt;i class="bx bx-**">&lt;/i></code> class.</p>
                    </b-card-header>
                    <b-card-body>

                        <h5>Regular</h5>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lemon"></i> bx bx-lemon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cable-car"></i> bx bx-cable-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cricket-ball"></i> bx bx-cricket-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-male-female"></i> bx bx-male-female
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-baguette"></i> bx bx-baguette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fork"></i> bx bx-fork
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-knife"></i> bx bx-knife
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-circle-half"></i> bx bx-circle-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-circle-three-quarter"></i> bx bx-circle-three-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-circle-quarter"></i> bx bx-circle-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bowl-rice"></i> bx bx-bowl-rice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bowl-hot"></i> bx bx-bowl-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-popsicle"></i> bx bx-popsicle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cross"></i> bx bx-cross
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-scatter-chart"></i> bx bx-scatter-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-money-withdraw"></i> bx bx-money-withdraw
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-candles"></i> bx bx-candles
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-math"></i> bx bx-math
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-party"></i> bx bx-party
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-leaf"></i> bx bx-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-injection"></i> bx bx-injection
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-expand-vertical"></i> bx bx-expand-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-expand-horizontal"></i> bx bx-expand-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-collapse-vertical"></i> bx bx-collapse-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-collapse-horizontal"></i> bx bx-collapse-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-collapse-alt"></i> bx bx-collapse-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-qr"></i> bx bx-qr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-qr-scan"></i> bx bx-qr-scan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-podcast"></i> bx bx-podcast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-checkbox-minus"></i> bx bx-checkbox-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-speaker"></i> bx bx-speaker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-registered"></i> bx bx-registered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-phone-off"></i> bx bx-phone-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-buildings"></i> bx bx-buildings
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-store-alt"></i> bx bx-store-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bar-chart-alt-2"></i> bx bx-bar-chart-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-dots"></i> bx bx-message-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-dots"></i> bx bx-message-rounded-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-memory-card"></i> bx bx-memory-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wallet-alt"></i> bx bx-wallet-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-slideshow"></i> bx bx-slideshow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square"></i> bx bx-message-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-dots"></i> bx bx-message-square-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-content"></i> bx bx-book-content
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chat"></i> bx bx-chat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-edit-alt"></i> bx bx-edit-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mouse-alt"></i> bx bx-mouse-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bug-alt"></i> bx bx-bug-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-notepad"></i> bx bx-notepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-video-recording"></i> bx bx-video-recording
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shape-square"></i> bx bx-shape-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shape-triangle"></i> bx bx-shape-triangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-ghost"></i> bx bx-ghost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mail-send"></i> bx bx-mail-send
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-code-alt"></i> bx bx-code-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-grid"></i> bx bx-grid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-pin"></i> bx bx-user-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-run"></i> bx bx-run
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-copy-alt"></i> bx bx-copy-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-transfer-alt"></i> bx bx-transfer-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-open"></i> bx bx-book-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-landscape"></i> bx bx-landscape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment"></i> bx bx-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-dots"></i> bx bx-comment-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pyramid"></i> bx bx-pyramid"
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cylinder"></i> bx bx-cylinder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lock-alt"></i> bx bx-lock-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lock-open-alt"></i> bx bx-lock-open-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-arrow-alt"></i> bx bx-left-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-arrow-alt"></i> bx bx-right-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-up-arrow-alt"></i> bx bx-up-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-down-arrow-alt"></i> bx bx-down-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shape-circle"></i> bx bx-shape-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cycling"></i> bx bx-cycling
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dna"></i> bx bx-dna
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bowling-ball"></i> bx bx-bowling-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-search-alt-2"></i> bx bx-search-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-plus-medical"></i> bx bx-plus-medical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-street-view"></i> bx bx-street-view
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-droplet"></i> bx bx-droplet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paint-roll"></i> bx bx-paint-roll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shield-alt-2"></i> bx bx-shield-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-error-alt"></i> bx bx-error-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-square"></i> bx bx-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-square-rounded"></i> bx bx-square-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-polygon"></i> bx bx-polygon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cube-alt"></i> bx bx-cube-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cuboid"></i> bx bx-cuboid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-voice"></i> bx bx-user-voice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-accessibility"></i> bx bx-accessibility
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-building-house"></i> bx bx-building-house
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-doughnut-chart"></i> bx bx-doughnut-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-log-in-circle"></i> bx bx-log-in-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-log-out-circle"></i> bx bx-log-out-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-check-square"></i> bx bx-check-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt"></i> bx bx-message-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-dots"></i> bx bx-message-alt-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-no-entry"></i> bx bx-no-entry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-palette"></i> bx bx-palette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-basket"></i> bx bx-basket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-purchase-tag-alt"></i> bx bx-purchase-tag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-receipt"></i> bx bx-receipt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-line-chart"></i> bx bx-line-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-map-pin"></i> bx bx-map-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hive"></i> bx bx-hive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-band-aid"></i> bx bx-band-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-credit-card-alt"></i> bx bx-credit-card-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wifi-off"></i> bx bx-wifi-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-brightness-half"></i> bx bx-brightness-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-brightness"></i> bx bx-brightness
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-filter-alt"></i> bx bx-filter-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dialpad-alt"></i> bx bx-dialpad-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-right"></i> bx bx-border-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-left"></i> bx bx-border-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-top"></i> bx bx-border-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-bottom"></i> bx bx-border-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-all"></i> bx bx-border-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mobile-landscape"></i> bx bx-mobile-landscape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mobile-vibration"></i> bx bx-mobile-vibration
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-gas-pump"></i> bx bx-gas-pump
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pie-chart-alt-2"></i> bx bx-pie-chart-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-time-five"></i> bx bx-time-five
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-briefcase-alt-2"></i> bx bx-briefcase-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-brush-alt"></i> bx bx-brush-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-customize"></i> bx bx-customize
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-radio"></i> bx bx-radio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-printer"></i> bx bx-printer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort-a-z"></i> bx bx-sort-a-z
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort-z-a"></i> bx bx-sort-z-a
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-conversation"></i> bx bx-conversation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-exit"></i> bx bx-exit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-extension"></i> bx bx-extension
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-face"></i> bx bx-face
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-file-find"></i> bx bx-file-find
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-label"></i> bx bx-label
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-check-shield"></i> bx bx-check-shield
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-radius"></i> bx bx-border-radius
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-add-to-queue"></i> bx bx-add-to-queue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-archive-in"></i> bx bx-archive-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-archive-out"></i> bx bx-archive-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-alarm-add"></i> bx bx-alarm-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-space-bar"></i> bx bx-space-bar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-image-alt"></i> bx bx-image-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-image-add"></i> bx bx-image-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fridge"></i> bx bx-fridge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dish"></i> bx bx-dish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-spa"></i> bx bx-spa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cake"></i> bx bx-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bolt-circle"></i> bx bx-bolt-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tone"></i> bx bx-tone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bitcoin"></i> bx bx-bitcoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lira"></i> bx bx-lira
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-ruble"></i> bx bx-ruble
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rupee"></i> bx bx-rupee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-euro"></i> bx bx-euro
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pound"></i> bx bx-pound
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-won"></i> bx bx-won
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-yen"></i> bx bx-yen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shekel"></i> bx bx-shekel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-health"></i> bx bx-health
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-clinic"></i> bx bx-clinic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-male"></i> bx bx-male
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-female"></i> bx bx-female
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-male-sign"></i> bx bx-male-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-female-sign"></i> bx bx-female-sign
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-food-tag"></i> bx bx-food-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-food-menu"></i> bx bx-food-menu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-meh-alt"></i> bx bx-meh-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wink-tongue"></i> bx bx-wink-tongue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-happy-alt"></i> bx bx-happy-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cool"></i> bx bx-cool
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tired"></i> bx bx-tired
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-smile"></i> bx bx-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-angry"></i> bx bx-angry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-happy-heart-eyes"></i> bx bx-happy-heart-eyes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dizzy"></i> bx bx-dizzy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wink-smile"></i> bx bx-wink-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-confused"></i> bx bx-confused
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sleepy"></i> bx bx-sleepy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shocked"></i> bx bx-shocked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-happy-beaming"></i> bx bx-happy-beaming
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-meh-blank"></i> bx bx-meh-blank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-laugh"></i> bx bx-laugh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-upside-down"></i> bx bx-upside-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-diamond"></i> bx bx-diamond
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-align-left"></i> bx bx-align-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-align-middle"></i> bx bx-align-middle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-align-right"></i> bx bx-align-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-back"></i> bx bx-arrow-back
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bell-minus"></i> bx bx-bell-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bell-off"></i> bx bx-bell-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bell-plus"></i> bx bx-bell-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bell"></i> bx bx-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark"></i> bx bx-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmarks"></i> bx bx-bookmarks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bullseye"></i> bx bx-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-camera-off"></i> bx bx-camera-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-camera"></i> bx bx-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-captions"></i> bx bx-captions
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-checkbox-checked"></i> bx bx-checkbox-checked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-checkbox"></i> bx bx-checkbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-checkbox-square"></i> bx bx-checkbox-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-down"></i> bx bx-chevron-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-up"></i> bx bx-chevron-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-left"></i> bx bx-chevron-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-right"></i> bx bx-chevron-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevrons-down"></i> bx bx-chevrons-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevrons-up"></i> bx bx-chevrons-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevrons-right"></i> bx bx-chevrons-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevrons-left"></i> bx bx-chevrons-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-clipboard"></i> bx bx-clipboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-code-curly"></i> bx bx-code-curly
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-code"></i> bx bx-code
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-coffee"></i> bx bx-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-copy"></i> bx bx-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-copyright"></i> bx bx-copyright
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-down-arrow-circle"></i> bx bx-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-error-circle"></i> bx bx-error-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-error"></i> bx bx-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-exit-fullscreen"></i> bx bx-exit-fullscreen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fast-forward-circle"></i> bx bx-fast-forward-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fast-forward"></i> bx bx-fast-forward
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-first-page"></i> bx bx-first-page
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-folder-minus"></i> bx bx-folder-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-folder-plus"></i> bx bx-folder-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-folder"></i> bx bx-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fullscreen"></i> bx bx-fullscreen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hide"></i> bx bx-hide
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-image"></i> bx bx-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-info-circle"></i> bx bx-info-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-align-justify"></i> bx bx-align-justify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-key"></i> bx bx-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-last-page"></i> bx bx-last-page
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-arrow-circle"></i> bx bx-left-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-down-arrow-circle"></i> bx bx-left-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-indent"></i> bx bx-left-indent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-top-arrow-circle"></i> bx bx-left-top-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-menu"></i> bx bx-menu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-microphone"></i> bx bx-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-minus-circle"></i> bx bx-minus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-moon"></i> bx bx-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pause-circle"></i> bx bx-pause-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pause"></i> bx bx-pause
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-play-circle"></i> bx bx-play-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-play"></i> bx bx-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-plus-circle"></i> bx bx-plus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-question-mark"></i> bx bx-question-mark"
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-radio-circle-marked"></i> bx bx-radio-circle-marked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-radio-circle"></i> bx bx-radio-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rectangle"></i> bx bx-rectangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rewind"></i> bx bx-rewind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-reset"></i> bx bx-reset
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-arrow-circle"></i> bx bx-right-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-down-arrow-circle"></i> bx bx-right-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-indent"></i> bx bx-right-indent
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-top-arrow-circle"></i> bx bx-right-top-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rss"></i> bx bx-rss
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-search"></i> bx bx-search
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-show"></i> bx bx-show
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-skip-next"></i> bx bx-skip-next
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-skip-previous"></i> bx bx-skip-previous
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-stop-circle"></i> bx bx-stop-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-stop"></i> bx bx-stop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-stopwatch"></i> bx bx-stopwatch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sync"></i> bx bx-sync
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-time"></i> bx bx-time
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-toggle-left"></i> bx bx-toggle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-toggle-right"></i> bx bx-toggle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trending-down"></i> bx bx-trending-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trending-up"></i> bx bx-trending-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-up-arrow-circle"></i> bx bx-up-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-vertical-center"></i> bx bx-vertical-center
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-video"></i> bx bx-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-volume-full"></i> bx bx-volume-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-volume-low"></i> bx bx-volume-low
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-volume-mute"></i> bx bx-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-volume"></i> bx bx-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-x-circle"></i> bx bx-x-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-zoom-in"></i> bx bx-zoom-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-zoom-out"></i> bx bx-zoom-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-archive"></i> bx bx-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-at"></i> bx bx-at
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bar-chart-alt"></i> bx bx-bar-chart-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bar-chart-square"></i> bx bx-bar-chart-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bar-chart"></i> bx bx-bar-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-basketball"></i> bx bx-basketball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-block"></i> bx bx-block
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-bookmark"></i> bx bx-book-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book"></i> bx bx-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-minus"></i> bx bx-bookmark-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-plus"></i> bx bx-bookmark-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-briefcase"></i> bx bx-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-broadcast"></i> bx bx-broadcast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-building"></i> bx bx-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bug"></i> bx bx-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bluetooth"></i> bx bx-bluetooth
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bulb"></i> bx bx-bulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-buoy"></i> bx bx-buoy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-plus"></i> bx bx-calendar-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-check"></i> bx bx-calendar-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-minus"></i> bx bx-calendar-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-x"></i> bx bx-calendar-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar"></i> bx bx-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chart"></i> bx bx-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-download"></i> bx bx-cloud-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-upload"></i> bx bx-cloud-upload
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud"></i> bx bx-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-terminal"></i> bx bx-terminal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-crosshair"></i> bx bx-crosshair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-compass"></i> bx bx-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-data"></i> bx bx-data
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-desktop"></i> bx bx-desktop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-directions"></i> bx bx-directions
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dollar"></i> bx bx-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dots-horizontal-rounded"></i> bx bx-dots-horizontal-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dots-horizontal"></i> bx bx-dots-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dots-vertical-rounded"></i> bx bx-dots-vertical-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dots-vertical"></i> bx bx-dots-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-download"></i> bx bx-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-envelope"></i> bx bx-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-gift"></i> bx bx-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-globe"></i> bx bx-globe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-devices"></i> bx bx-devices
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-headphone"></i> bx bx-headphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-heart"></i> bx bx-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-home"></i> bx bx-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-laptop"></i> bx bx-laptop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-layer"></i> bx bx-layer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-link-alt"></i> bx bx-link-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-link"></i> bx bx-link
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-list-plus"></i> bx bx-list-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-list-ul"></i> bx bx-list-ul
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-list-minus"></i> bx bx-list-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lock-open"></i> bx bx-lock-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-lock"></i> bx bx-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-map-alt"></i> bx bx-map-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-map"></i> bx bx-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded"></i> bx bx-message-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message"></i> bx bx-message
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mobile-alt"></i> bx bx-mobile-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mobile"></i> bx bx-mobile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-navigation"></i> bx bx-navigation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-phone"></i> bx bx-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pie-chart"></i> bx bx-pie-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-send"></i> bx bx-send
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sidebar"></i> bx bx-sidebar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sitemap"></i> bx bx-sitemap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-spreadsheet"></i> bx bx-spreadsheet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tab"></i> bx bx-tab
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tag"></i> bx bx-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-target-lock"></i> bx bx-target-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tennis-ball"></i> bx bx-tennis-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-alarm"></i> bx bx-alarm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-upload"></i> bx bx-upload
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-usb"></i> bx bx-usb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-video-off"></i> bx bx-video-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-voicemail"></i> bx bx-voicemail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wifi"></i> bx bx-wifi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-window-open"></i> bx bx-window-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-window"></i> bx bx-window
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-windows"></i> bx bx-windows
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-duplicate"></i> bx bx-duplicate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-table"></i> bx bx-table
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-x"></i> bx bx-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-adjust"></i> bx bx-adjust
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-album"></i> bx bx-album
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-anchor"></i> bx bx-anchor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-award"></i> bx bx-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bold"></i> bx bx-bold
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calculator"></i> bx bx-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cart"></i> bx bx-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-check"></i> bx bx-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-drizzle"></i> bx bx-cloud-drizzle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-light-rain"></i> bx bx-cloud-light-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-lightning"></i> bx bx-cloud-lightning
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-rain"></i> bx bx-cloud-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cloud-snow"></i> bx bx-cloud-snow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cog"></i> bx bx-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-columns"></i> bx bx-columns
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-credit-card"></i> bx bx-credit-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-crop"></i> bx bx-crop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cube"></i> bx bx-cube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cut"></i> bx bx-cut
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-detail"></i> bx bx-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shield-quarter"></i> bx bx-shield-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-edit"></i> bx bx-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-file"></i> bx bx-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-filter"></i> bx bx-filter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-font"></i> bx bx-font
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-branch"></i> bx bx-git-branch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-commit"></i> bx bx-git-commit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-compare"></i> bx bx-git-compare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-merge"></i> bx bx-git-merge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-pull-request"></i> bx bx-git-pull-request
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-git-repo-forked"></i> bx bx-git-repo-forked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-group"></i> bx bx-group
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hash"></i> bx bx-hash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-heading"></i> bx bx-heading
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-home-alt"></i> bx bx-home-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-italic"></i> bx bx-italic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-joystick"></i> bx bx-joystick
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-link-external"></i> bx bx-link-external
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-log-in"></i> bx bx-log-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-log-out"></i> bx bx-log-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-microphone-off"></i> bx bx-microphone-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-minus"></i> bx bx-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mouse"></i> bx bx-mouse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-move"></i> bx bx-move
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-music"></i> bx bx-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-notification"></i> bx bx-notification
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-package"></i> bx bx-package
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paragraph"></i> bx bx-paragraph
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paste"></i> bx bx-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pencil"></i> bx bx-pencil
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pin"></i> bx bx-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-plus"></i> bx bx-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-power-off"></i> bx bx-power-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pulse"></i> bx bx-pulse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-save"></i> bx bx-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-screenshot"></i> bx bx-screenshot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-select-multiple"></i> bx bx-select-multiple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-share-alt"></i> bx bx-share-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-share"></i> bx bx-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shield-alt"></i> bx bx-shield-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shield"></i> bx bx-shield
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shopping-bag"></i> bx bx-shopping-bag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shuffle"></i> bx bx-shuffle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort"></i> bx bx-sort
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-star"></i> bx bx-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sun"></i> bx bx-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-text"></i> bx bx-text
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trash"></i> bx bx-trash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trophy"></i> bx bx-trophy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-underline"></i> bx bx-underline
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-check"></i> bx bx-user-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-circle"></i> bx bx-user-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-minus"></i> bx bx-user-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-plus"></i> bx bx-user-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user-x"></i> bx bx-user-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-user"></i> bx bx-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-barcode"></i> bx bx-barcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-crown"></i> bx bx-crown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dislike"></i> bx bx-dislike
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-down-arrow"></i> bx bx-down-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-export"></i> bx bx-export
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-first-aid"></i> bx bx-first-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-flag"></i> bx bx-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-history"></i> bx bx-history
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-joystick-alt"></i> bx bx-joystick-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-left-arrow"></i> bx bx-left-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-like"></i> bx bx-like
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-list-check"></i> bx bx-list-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-poll"></i> bx bx-poll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-radar"></i> bx bx-radar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-redo"></i> bx bx-redo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-reply-all"></i> bx bx-reply-all
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-reply"></i> bx bx-reply
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-repost"></i> bx bx-repost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-revision"></i> bx bx-revision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-right-arrow"></i> bx bx-right-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-subdirectory-left"></i> bx bx-subdirectory-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-subdirectory-right"></i> bx bx-subdirectory-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-support"></i> bx bx-support
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-timer"></i> bx bx-timer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-undo"></i> bx bx-undo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-up-arrow"></i> bx bx-up-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-phone-call"></i> bx bx-phone-call
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-aperture"></i> bx bx-aperture
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-film"></i> bx bx-film
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-folder-open"></i> bx bx-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-task"></i> bx bx-task
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-server"></i> bx bx-server
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-battery"></i> bx bx-battery
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-alt"></i> bx bx-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-import"></i> bx bx-import
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-ruler"></i> bx bx-ruler
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-horizontal-center"></i> bx bx-horizontal-center
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rotate-right"></i> bx bx-rotate-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rename"></i> bx bx-rename
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-collapse"></i> bx bx-collapse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-phone-incoming"></i> bx bx-phone-incoming
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-phone-outgoing"></i> bx bx-phone-outgoing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-body"></i> bx bx-body
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cast"></i> bx bx-cast
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chip"></i> bx bx-chip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-skip-next-circle"></i> bx bx-skip-next-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-skip-previous-circle"></i> bx bx-skip-previous-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hdd"></i> bx bx-hdd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-store"></i> bx bx-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-globe-alt"></i> bx bx-globe-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-upvote"></i> bx bx-upvote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-downvote"></i> bx bx-downvote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-news"></i> bx bx-news
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pie-chart-alt"></i> bx bx-pie-chart-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-images"></i> bx bx-images
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-purchase-tag"></i> bx bx-purchase-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pen"></i> bx bx-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-expand"></i> bx bx-expand
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paperclip"></i> bx bx-paperclip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-closet"></i> bx bx-closet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tv"></i> bx bx-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-collection"></i> bx bx-collection
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-station"></i> bx bx-station
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wallet"></i> bx bx-wallet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-briefcase-alt"></i> bx bx-briefcase-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hourglass"></i> bx bx-hourglass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-carousel"></i> bx bx-carousel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-infinite"></i> bx bx-infinite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-plug"></i> bx bx-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-notification-off"></i> bx bx-notification-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-window-close"></i> bx bx-window-close
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-command"></i> bx bx-command
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-grid-alt"></i> bx bx-grid-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trash-alt"></i> bx bx-trash-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chalkboard"></i> bx bx-chalkboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-loader"></i> bx bx-loader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-slider"></i> bx bx-slider
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paper-plane"></i> bx bx-paper-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-selection"></i> bx bx-selection
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-world"></i> bx bx-world
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dock-bottom"></i> bx bx-dock-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dock-right"></i> bx bx-dock-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dock-top"></i> bx bx-dock-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dock-left"></i> bx bx-dock-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-layout"></i> bx bx-layout
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-alarm-off"></i> bx bx-alarm-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wrench"></i> bx bx-wrench
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-loader-circle"></i> bx bx-loader-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-loader-alt"></i> bx bx-loader-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-car"></i> bx bx-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cart-alt"></i> bx bx-cart-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-happy"></i> bx bx-happy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-meh"></i> bx bx-meh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sad"></i> bx bx-sad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-slider-alt"></i> bx bx-slider-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-certification"></i> bx bx-certification
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rocket"></i> bx bx-rocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-check-circle"></i> bx bx-check-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bus"></i> bx bx-bus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-check-double"></i> bx bx-check-double
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dumbbell"></i> bx bx-dumbbell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bot"></i> bx bx-bot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-area"></i> bx bx-area
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bed"></i> bx bx-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bath"></i> bx bx-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-train"></i> bx bx-train
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-taxi"></i> bx bx-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-movie"></i> bx bx-movie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-hotel"></i> bx bx-hotel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-planet"></i> bx bx-planet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-list-ol"></i> bx bx-list-ol
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-video-plus"></i> bx bx-video-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-menu-alt-left"></i> bx bx-menu-alt-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-menu-alt-right"></i> bx bx-menu-alt-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-box"></i> bx bx-box
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-restaurant"></i> bx bx-restaurant
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-swim"></i> bx bx-swim
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-water"></i> bx bx-water
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wind"></i> bx bx-wind
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dialpad"></i> bx bx-dialpad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-handicap"></i> bx bx-handicap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-font-size"></i> bx bx-font-size
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-code-block"></i> bx bx-code-block
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-photo-album"></i> bx bx-photo-album
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-strikethrough"></i> bx bx-strikethrough
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-file-blank"></i> bx bx-file-blank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-highlight"></i> bx bx-highlight
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-font-color"></i> bx bx-font-color
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-fingerprint"></i> bx bx-fingerprint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-transfer"></i> bx bx-transfer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-circle"></i> bx bx-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-ball"></i> bx bx-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-football"></i> bx bx-football
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dollar-circle"></i> bx bx-dollar-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-search-alt"></i> bx bx-search-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-analyse"></i> bx bx-analyse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-disc"></i> bx bx-disc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-equalizer"></i> bx bx-equalizer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-stats"></i> bx bx-stats
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-move-horizontal"></i> bx bx-move-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-move-vertical"></i> bx bx-move-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-grid-horizontal"></i> bx bx-grid-horizontal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-grid-vertical"></i> bx bx-grid-vertical
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-grid-small"></i> bx bx-grid-small
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-badge"></i> bx bx-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-id-card"></i> bx bx-id-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort-up"></i> bx bx-sort-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort-down"></i> bx bx-sort-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-note"></i> bx bx-note
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-test-tube"></i> bx bx-test-tube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-help-circle"></i> bx bx-help-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-card"></i> bx bx-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rewind-circle"></i> bx bx-rewind-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-magnet"></i> bx bx-magnet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-event"></i> bx bx-calendar-event
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-left"></i> bx bx-caret-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-up"></i> bx bx-caret-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-right"></i> bx bx-caret-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-down"></i> bx bx-caret-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-show-alt"></i> bx bx-show-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-badge-check"></i> bx bx-badge-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-rotate-left"></i> bx bx-rotate-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-brush"></i> bx bx-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-unlink"></i> bx bx-unlink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-paint"></i> bx bx-paint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-joystick-button"></i> bx bx-joystick-button
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-font-family"></i> bx bx-font-family
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-repeat"></i> bx bx-repeat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-walk"></i> bx bx-walk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-money"></i> bx bx-money
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-home-circle"></i> bx bx-home-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-location-plus"></i> bx bx-location-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arch"></i> bx bx-arch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-atom"></i> bx bx-atom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-baseball"></i> bx bx-baseball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-beer"></i> bx bx-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bible"></i> bx bx-bible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bomb"></i> bx bx-bomb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bus-school"></i> bx bx-bus-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cabinet"></i> bx bx-cabinet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-edit"></i> bx bx-calendar-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-coffee-togo"></i> bx bx-coffee-togo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-pointer"></i> bx bx-pointer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-microchip"></i> bx bx-microchip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-heart-circle"></i> bx bx-heart-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-heart-square"></i> bx bx-heart-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-home-heart"></i> bx bx-home-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-info-square"></i> bx bx-info-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-layer-plus"></i> bx bx-layer-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-layer-minus"></i> bx bx-layer-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-recycle"></i> bx bx-recycle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-traffic-cone"></i> bx bx-traffic-cone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wifi-2"></i> bx bx-wifi-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wifi-1"></i> bx bx-wifi-1
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wifi-0"></i> bx bx-wifi-0
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-mask"></i> bx bx-mask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-low-vision"></i> bx bx-low-vision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-been-here"></i> bx bx-been-here
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-current-location"></i> bx bx-current-location
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-from-top"></i> bx bx-arrow-from-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-from-bottom"></i> bx bx-arrow-from-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-from-left"></i> bx bx-arrow-from-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-from-right"></i> bx bx-arrow-from-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-to-right"></i> bx bx-arrow-to-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-to-left"></i> bx bx-arrow-to-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-to-top"></i> bx bx-arrow-to-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-arrow-to-bottom"></i> bx bx-arrow-to-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-reader"></i> bx bx-book-reader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-scan"></i> bx bx-scan
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-week"></i> bx bx-calendar-week
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-glasses"></i> bx bx-glasses
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-glasses-alt"></i> bx bx-glasses-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-none"></i> bx bx-border-none
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-inner"></i> bx bx-border-inner
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-1"></i> bx bx-dice-1
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-2"></i> bx bx-dice-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-3"></i> bx bx-dice-3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-4"></i> bx bx-dice-4
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-5"></i> bx bx-dice-5
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-dice-6"></i> bx bx-dice-6
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-webcam"></i> bx bx-webcam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-spray-can"></i> bx bx-spray-can
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sticker"></i> bx bx-sticker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tachometer"></i> bx bx-tachometer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-game"></i> bx bx-game
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-abacus"></i> bx bx-abacus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-alarm-snooze"></i> bx bx-alarm-snooze
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-alarm-exclamation"></i> bx bx-alarm-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-medal"></i> bx bx-medal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-task-x"></i> bx bx-task-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-barcode-reader"></i> bx bx-barcode-reader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-blanket"></i> bx bx-blanket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bone"></i> bx bx-bone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bong"></i> bx bx-bong
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-alt"></i> bx bx-book-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-heart"></i> bx bx-book-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-book-add"></i> bx bx-book-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bracket"></i> bx bx-bracket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-brain"></i> bx bx-brain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-border-outer"></i> bx bx-border-outer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-braille"></i> bx bx-braille
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-window-alt"></i> bx bx-window-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-heart"></i> bx bx-calendar-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-wine"></i> bx bx-wine
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-vial"></i> bx bx-vial
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-color-fill"></i> bx bx-color-fill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-capsule"></i> bx bx-capsule
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-eraser"></i> bx bx-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-drink"></i> bx bx-drink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cctv"></i> bx bx-cctv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chair"></i> bx bx-chair
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-network-chart"></i> bx bx-network-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-vector"></i> bx bx-vector
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-exclamation"></i> bx bx-calendar-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-calendar-star"></i> bx bx-calendar-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-camera-home"></i> bx bx-camera-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-camera-movie"></i> bx bx-camera-movie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-right-circle"></i> bx bx-caret-right-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-left-circle"></i> bx bx-caret-left-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-up-circle"></i> bx bx-caret-up-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-down-circle"></i> bx bx-caret-down-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-right-square"></i> bx bx-caret-right-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-up-square"></i> bx bx-caret-up-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-left-square"></i> bx bx-caret-left-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-caret-down-square"></i> bx bx-caret-down-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shield-x"></i> bx bx-shield-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-line-chart-down"></i> bx bx-line-chart-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-down-circle"></i> bx bx-chevron-down-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-up-circle"></i> bx bx-chevron-up-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-left-circle"></i> bx bx-chevron-left-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-right-circle"></i> bx bx-chevron-right-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-down-square"></i> bx bx-chevron-down-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-up-square"></i> bx bx-chevron-up-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-left-square"></i> bx bx-chevron-left-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-chevron-right-square"></i> bx bx-chevron-right-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-church"></i> bx bx-church
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-coin"></i> bx bx-coin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-coin-stack"></i> bx bx-coin-stack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-unite"></i> bx bx-unite
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-minus-front"></i> bx bx-minus-front
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-intersect"></i> bx bx-intersect
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-exclude"></i> bx bx-exclude
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-minus-back"></i> bx bx-minus-back
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-merge"></i> bx bx-merge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trim"></i> bx bx-trim
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-outline"></i> bx bx-outline
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-meteor"></i> bx bx-meteor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-refresh"></i> bx bx-refresh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-home-smile"></i> bx bx-home-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-envelope-open"></i> bx bx-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-add"></i> bx bx-message-alt-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-check"></i> bx bx-message-alt-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-error"></i> bx bx-message-alt-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-x"></i> bx bx-message-alt-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-minus"></i> bx bx-message-alt-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-edit"></i> bx bx-message-alt-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-alt-detail"></i> bx bx-message-alt-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-check"></i> bx bx-message-rounded-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-error"></i> bx bx-message-rounded-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-x"></i> bx bx-message-rounded-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-minus"></i> bx bx-message-rounded-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-edit"></i> bx bx-message-rounded-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-add"></i> bx bx-message-rounded-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-rounded-detail"></i> bx bx-message-rounded-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-check"></i> bx bx-message-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-error"></i> bx bx-message-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-x"></i> bx bx-message-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-minus"></i> bx bx-message-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-edit"></i> bx bx-message-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-add"></i> bx bx-message-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-detail"></i> bx bx-message-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-check"></i> bx bx-message-square-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-error"></i> bx bx-message-square-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-x"></i> bx bx-message-square-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-minus"></i> bx bx-message-square-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-edit"></i> bx bx-message-square-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-add"></i> bx bx-message-square-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-message-square-detail"></i> bx bx-message-square-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-check"></i> bx bx-comment-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-error"></i> bx bx-comment-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-x"></i> bx bx-comment-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-edit"></i> bx bx-comment-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-minus"></i> bx bx-comment-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-add"></i> bx bx-comment-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-comment-detail"></i> bx bx-comment-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-cookie"></i> bx bx-cookie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-credit-card-front"></i> bx bx-credit-card-front
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-door-open"></i> bx bx-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-donate-heart"></i> bx bx-donate-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-donate-blood"></i> bx bx-donate-blood
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-shape-polygon"></i> bx bx-shape-polygon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-heart"></i> bx bx-bookmark-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-sort-alt-2"></i> bx bx-sort-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-category"></i> bx bx-category
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-category-alt"></i> bx bx-category-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-alt"></i> bx bx-bookmark-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-alt-plus"></i> bx bx-bookmark-alt-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-bookmark-alt-minus"></i> bx bx-bookmark-alt-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-tag-alt"></i> bx bx-tag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-movie-play"></i> bx bx-movie-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-expand-alt"></i> bx bx-expand-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-library"></i> bx bx-library
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bx-trip"></i> bx bx-trip
                            </b-col>
                        </b-row>

                        <h5 class="mt-5">Solid Icons</h5>
                        <p class="text-muted mb-0">Use class <code>&lt;i class="bx bxs-**">&lt;/i></code></p>

                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-lemon"></i> bx bxs-lemon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cable-car"></i> bx bxs-cable-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cricket-ball"></i> bx bxs-cricket-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tree-alt"></i> bx bxs-tree-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-invader"></i> bx bxs-invader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-baguette"></i> bx bxs-baguette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-circle-half"></i> bx bxs-circle-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-circle-three-quarter"></i> bx bxs-circle-three-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-circle-quarter"></i> bx bxs-circle-quarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bowl-rice"></i> bx bxs-bowl-rice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bowl-hot"></i> bx bxs-bowl-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-popsicle"></i> bx bxs-popsicle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-party"></i> bx bxs-party
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-leaf"></i> bx bxs-leaf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-injection"></i> bx bxs-injection
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dog"></i> bx bxs-dog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cat"></i> bx bxs-cat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hand"></i> bx bxs-hand
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-checkbox-minus"></i> bx bxs-checkbox-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-speaker"></i> bx bxs-speaker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-registered"></i> bx bxs-registered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-phone-off"></i> bx bxs-phone-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-buildings"></i> bx bxs-buildings
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-store-alt"></i> bx bxs-store-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bar-chart-alt-2"></i> bx bxs-bar-chart-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-dots"></i> bx bxs-message-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-dots"></i> bx bxs-message-rounded-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-devices"></i> bx bxs-devices
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-memory-card"></i> bx bxs-memory-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wallet-alt"></i> bx bxs-wallet-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bank"></i> bx bxs-bank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-slideshow"></i> bx bxs-slideshow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square"></i> bx bxs-message-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-dots"></i> bx bxs-message-square-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-content"></i> bx bxs-book-content
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chat"></i> bx bxs-chat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-edit-alt"></i> bx bxs-edit-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-mouse-alt"></i> bx bxs-mouse-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bug-alt"></i> bx bxs-bug-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-notepad"></i> bx bxs-notepad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-video-recording"></i> bx bxs-video-recording
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-direction-left"></i> bx bxs-direction-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ghost"></i> bx bxs-ghost
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-single-left"></i> bx bxs-quote-single-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-single-right"></i> bx bxs-quote-single-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-pin"></i> bx bxs-user-pin
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-copy-alt"></i> bx bxs-copy-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-doc"></i> bx bxs-file-doc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-html"></i> bx bxs-file-html
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-detail"></i> bx bxs-comment-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-add"></i> bx bxs-comment-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-css"></i> bx bxs-file-css
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-js"></i> bx bxs-file-js
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-json"></i> bx bxs-file-json
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-md"></i> bx bxs-file-md
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-txt"></i> bx bxs-file-txt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-png"></i> bx bxs-file-png
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-jpg"></i> bx bxs-file-jpg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-gif"></i> bx bxs-file-gif
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-analyse"></i> bx bxs-analyse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plane-take-off"></i> bx bxs-plane-take-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plane-land"></i> bx bxs-plane-land
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-parking"></i> bx bxs-parking
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-id-card"></i> bx bxs-id-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-adjust-alt"></i> bx bxs-adjust-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-landscape"></i> bx bxs-landscape
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-traffic"></i> bx bxs-traffic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment"></i> bx bxs-comment
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-dots"></i> bx bxs-comment-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wine"></i> bx bxs-wine
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pyramid"></i> bx bxs-pyramid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cylinder"></i> bx bxs-cylinder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-graduation"></i> bx bxs-graduation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-lock-alt"></i> bx bxs-lock-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-lock-open-alt"></i> bx bxs-lock-open-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hourglass-top"></i> bx bxs-hourglass-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hourglass-bottom"></i> bx bxs-hourglass-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bowling-ball"></i> bx bxs-bowling-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-search-alt-2"></i> bx bxs-search-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-droplet-half"></i> bx bxs-droplet-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-paint-roll"></i> bx bxs-paint-roll
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shield-alt-2"></i> bx bxs-shield-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-error-alt"></i> bx bxs-error-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-square"></i> bx bxs-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-square-rounded"></i> bx bxs-square-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-polygon"></i> bx bxs-polygon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cube-alt"></i> bx bxs-cube-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cuboid"></i> bx bxs-cuboid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-voice"></i> bx bxs-user-voice
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-building-house"></i> bx bxs-building-house
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-doughnut-chart"></i> bx bxs-doughnut-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-circle"></i> bx bxs-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-log-in-circle"></i> bx bxs-log-in-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-log-out-circle"></i> bx bxs-log-out-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-log-in"></i> bx bxs-log-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-log-out"></i> bx bxs-log-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-notification"></i> bx bxs-notification
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-notification-off"></i> bx bxs-notification-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-check-square"></i> bx bxs-check-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt"></i> bx bxs-message-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-dots"></i> bx bxs-message-alt-dots
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-no-entry"></i> bx bxs-no-entry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-traffic-barrier"></i> bx bxs-traffic-barrier
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-component"></i> bx bxs-component
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plane-alt"></i> bx bxs-plane-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-palette"></i> bx bxs-palette
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-basket"></i> bx bxs-basket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-purchase-tag-alt"></i> bx bxs-purchase-tag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-receipt"></i> bx bxs-receipt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-map-pin"></i> bx bxs-map-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-band-aid"></i> bx bxs-band-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-credit-card-alt"></i> bx bxs-credit-card-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-credit-card"></i> bx bxs-credit-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-paint"></i> bx bxs-paint
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-brightness-half"></i> bx bxs-brightness-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-brightness"></i> bx bxs-brightness
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-rectangle"></i> bx bxs-rectangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-arrow"></i> bx bxs-right-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-arrow"></i> bx bxs-left-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-up-arrow"></i> bx bxs-up-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-down-arrow"></i> bx bxs-down-arrow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-top-arrow-circle"></i> bx bxs-right-top-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-down-arrow-circle"></i> bx bxs-right-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-top-arrow-circle"></i> bx bxs-left-top-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-down-arrow-circle"></i> bx bxs-left-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-institution"></i> bx bxs-institution
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-school"></i> bx bxs-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chalkboard"></i> bx bxs-chalkboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-skip-previous-circle"></i> bx bxs-skip-previous-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-skip-next-circle"></i> bx bxs-skip-next-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-data"></i> bx bxs-data
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-mobile"></i> bx bxs-mobile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-folder-minus"></i> bx bxs-folder-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bell-plus"></i> bx bxs-bell-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bell-minus"></i> bx bxs-bell-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-search"></i> bx bxs-search
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-zoom-in"></i> bx bxs-zoom-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-zoom-out"></i> bx bxs-zoom-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-grid"></i> bx bxs-grid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-x"></i> bx bxs-user-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-check"></i> bx bxs-user-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-compass"></i> bx bxs-compass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-stopwatch"></i> bx bxs-stopwatch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-timer"></i> bx bxs-timer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-time"></i> bx bxs-time
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pie-chart-alt-2"></i> bx bxs-pie-chart-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-time-five"></i> bx bxs-time-five
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmarks"></i> bx bxs-bookmarks
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-minus"></i> bx bxs-bookmark-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-briefcase-alt-2"></i> bx bxs-briefcase-alt-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar"></i> bx bxs-calendar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-alt"></i> bx bxs-calendar-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-plus"></i> bx bxs-calendar-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-minus"></i> bx bxs-calendar-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-x"></i> bx bxs-calendar-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-check"></i> bx bxs-calendar-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-event"></i> bx bxs-calendar-event
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-customize"></i> bx bxs-customize
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-carousel"></i> bx bxs-carousel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-rewind-circle"></i> bx bxs-rewind-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-fast-forward-circle"></i> bx bxs-fast-forward-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-mobile-vibration"></i> bx bxs-mobile-vibration
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-alt-left"></i> bx bxs-quote-alt-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-alt-right"></i> bx bxs-quote-alt-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-layout"></i> bx bxs-layout
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-brush-alt"></i> bx bxs-brush-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-exit"></i> bx bxs-exit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-extension"></i> bx bxs-extension
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-find"></i> bx bxs-file-find
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-face"></i> bx bxs-face
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-label"></i> bx bxs-label
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-check-shield"></i> bx bxs-check-shield
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-add-to-queue"></i> bx bxs-add-to-queue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-archive-in"></i> bx bxs-archive-in
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-archive-out"></i> bx bxs-archive-out
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-alarm-add"></i> bx bxs-alarm-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-image-add"></i> bx bxs-image-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-fridge"></i> bx bxs-fridge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dish"></i> bx bxs-dish
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-spa"></i> bx bxs-spa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cake"></i> bx bxs-cake
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-city"></i> bx bxs-city
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bolt-circle"></i> bx bxs-bolt-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-up-circle"></i> bx bxs-caret-up-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-down-circle"></i> bx bxs-caret-down-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-left-circle"></i> bx bxs-caret-left-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-right-circle"></i> bx bxs-caret-right-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tone"></i> bx bxs-tone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-baby-carriage"></i> bx bxs-baby-carriage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hand-up"></i> bx bxs-hand-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hand-right"></i> bx bxs-hand-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hand-down"></i> bx bxs-hand-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hand-left"></i> bx bxs-hand-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-clinic"></i> bx bxs-clinic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-offer"></i> bx bxs-offer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-food-menu"></i> bx bxs-food-menu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-camera-plus"></i> bx bxs-camera-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-business"></i> bx bxs-business
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-angry"></i> bx bxs-angry
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-happy-heart-eyes"></i> bx bxs-happy-heart-eyes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dizzy"></i> bx bxs-dizzy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wink-smile"></i> bx bxs-wink-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-smile"></i> bx bxs-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-meh"></i> bx bxs-meh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-meh-alt"></i> bx bxs-meh-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-confused"></i> bx bxs-confused
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-sleepy"></i> bx bxs-sleepy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-sad"></i> bx bxs-sad
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-happy"></i> bx bxs-happy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shocked"></i> bx bxs-shocked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-happy-beaming"></i> bx bxs-happy-beaming
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tired"></i> bx bxs-tired
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cool"></i> bx bxs-cool
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-meh-blank"></i> bx bxs-meh-blank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-laugh"></i> bx bxs-laugh
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-happy-alt"></i> bx bxs-happy-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-upside-down"></i> bx bxs-upside-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wink-tongue"></i> bx bxs-wink-tongue
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-error"></i> bx bxs-comment-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-vial"></i> bx bxs-vial
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-adjust"></i> bx bxs-adjust
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-alarm"></i> bx bxs-alarm
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-alarm-off"></i> bx bxs-alarm-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-album"></i> bx bxs-album
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-archive"></i> bx bxs-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-camera"></i> bx bxs-camera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-camera-off"></i> bx bxs-camera-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-folder"></i> bx bxs-folder
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-folder-plus"></i> bx bxs-folder-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-award"></i> bx bxs-award
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bar-chart-square"></i> bx bxs-bar-chart-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-barcode"></i> bx bxs-barcode
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-battery"></i> bx bxs-battery
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-battery-charging"></i> bx bxs-battery-charging
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-battery-full"></i> bx bxs-battery-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bell"></i> bx bxs-bell
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bell-off"></i> bx bxs-bell-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bolt"></i> bx bxs-bolt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book"></i> bx bxs-book
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-bookmark"></i> bx bxs-book-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark"></i> bx bxs-bookmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-plus"></i> bx bxs-bookmark-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-open"></i> bx bxs-book-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-star"></i> bx bxs-bookmark-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-briefcase"></i> bx bxs-briefcase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-briefcase-alt"></i> bx bxs-briefcase-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bug"></i> bx bxs-bug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-building"></i> bx bxs-building
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bulb"></i> bx bxs-bulb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-buoy"></i> bx bxs-buoy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calculator"></i> bx bxs-calculator
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-captions"></i> bx bxs-captions
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car"></i> bx bxs-car
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cart-alt"></i> bx bxs-cart-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cart"></i> bx bxs-cart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chart"></i> bx bxs-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chip"></i> bx bxs-chip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cloud-download"></i> bx bxs-cloud-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cloud-upload"></i> bx bxs-cloud-upload
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cloud"></i> bx bxs-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coffee"></i> bx bxs-coffee
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cog"></i> bx bxs-cog
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-collection"></i> bx bxs-collection
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-contact"></i> bx bxs-contact
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-copy"></i> bx bxs-copy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coupon"></i> bx bxs-coupon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-crown"></i> bx bxs-crown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cube"></i> bx bxs-cube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-detail"></i> bx bxs-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-discount"></i> bx bxs-discount
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dislike"></i> bx bxs-dislike
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dock-bottom"></i> bx bxs-dock-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dock-left"></i> bx bxs-dock-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dock-right"></i> bx bxs-dock-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dock-top"></i> bx bxs-dock-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-down-arrow-circle"></i> bx bxs-down-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-download"></i> bx bxs-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-downvote"></i> bx bxs-downvote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-drink"></i> bx bxs-drink
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-droplet"></i> bx bxs-droplet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-duplicate"></i> bx bxs-duplicate
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-eject"></i> bx bxs-eject
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-envelope"></i> bx bxs-envelope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-error-circle"></i> bx bxs-error-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-error"></i> bx bxs-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-image"></i> bx bxs-file-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file"></i> bx bxs-file
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-filter-alt"></i> bx bxs-filter-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-first-aid"></i> bx bxs-first-aid
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-flag-alt"></i> bx bxs-flag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-flag"></i> bx bxs-flag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-gift"></i> bx bxs-gift
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-grid-alt"></i> bx bxs-grid-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-group"></i> bx bxs-group
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hdd"></i> bx bxs-hdd
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-heart"></i> bx bxs-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hide"></i> bx bxs-hide
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-home"></i> bx bxs-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hot"></i> bx bxs-hot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hourglass"></i> bx bxs-hourglass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-image"></i> bx bxs-image
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-inbox"></i> bx bxs-inbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-info-circle"></i> bx bxs-info-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-joystick-alt"></i> bx bxs-joystick-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-joystick"></i> bx bxs-joystick
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-layer"></i> bx bxs-layer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-arrow-circle"></i> bx bxs-left-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-like"></i> bx bxs-like
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-lock-open"></i> bx bxs-lock-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-lock"></i> bx bxs-lock
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-map-alt"></i> bx bxs-map-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-map"></i> bx bxs-map
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded"></i> bx bxs-message-rounded
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message"></i> bx bxs-message
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-microphone-off"></i> bx bxs-microphone-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-microphone"></i> bx bxs-microphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-minus-circle"></i> bx bxs-minus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-moon"></i> bx bxs-moon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-mouse"></i> bx bxs-mouse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-music"></i> bx bxs-music
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-navigation"></i> bx bxs-navigation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-news"></i> bx bxs-news
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-package"></i> bx bxs-package
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-paper-plane"></i> bx bxs-paper-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-paste"></i> bx bxs-paste
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pen"></i> bx bxs-pen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pencil"></i> bx bxs-pencil
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-phone-call"></i> bx bxs-phone-call
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-phone-incoming"></i> bx bxs-phone-incoming
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-phone-outgoing"></i> bx bxs-phone-outgoing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-phone"></i> bx bxs-phone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pie-chart-alt"></i> bx bxs-pie-chart-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pie-chart"></i> bx bxs-pie-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pin"></i> bx bxs-pin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-playlist"></i> bx bxs-playlist
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plug"></i> bx bxs-plug
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plus-circle"></i> bx bxs-plus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-printer"></i> bx bxs-printer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-purchase-tag"></i> bx bxs-purchase-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-left"></i> bx bxs-quote-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-quote-right"></i> bx bxs-quote-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-radio"></i> bx bxs-radio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-rename"></i> bx bxs-rename
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-report"></i> bx bxs-report
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-arrow-circle"></i> bx bxs-right-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ruler"></i> bx bxs-ruler
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-save"></i> bx bxs-save
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-sort-alt"></i> bx bxs-sort-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-select-multiple"></i> bx bxs-select-multiple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-send"></i> bx bxs-send
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-server"></i> bx bxs-server
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-share-alt"></i> bx bxs-share-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-share"></i> bx bxs-share
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shield"></i> bx bxs-shield
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shopping-bag-alt"></i> bx bxs-shopping-bag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shopping-bag"></i> bx bxs-shopping-bag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-show"></i> bx bxs-show
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-spreadsheet"></i> bx bxs-spreadsheet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-star"></i> bx bxs-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-store"></i> bx bxs-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-sun"></i> bx bxs-sun
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-t-shirt"></i> bx bxs-t-shirt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tag-x"></i> bx bxs-tag-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tag"></i> bx bxs-tag
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tennis-ball"></i> bx bxs-tennis-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-terminal"></i> bx bxs-terminal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-to-top"></i> bx bxs-to-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-toggle-left"></i> bx bxs-toggle-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-toggle-right"></i> bx bxs-toggle-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-torch"></i> bx bxs-torch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-trash-alt"></i> bx bxs-trash-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-trash"></i> bx bxs-trash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-trophy"></i> bx bxs-trophy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-truck"></i> bx bxs-truck
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-up-arrow-circle"></i> bx bxs-up-arrow-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-upvote"></i> bx bxs-upvote
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-circle"></i> bx bxs-user-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-detail"></i> bx bxs-user-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-minus"></i> bx bxs-user-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-plus"></i> bx bxs-user-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user"></i> bx bxs-user
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-video-off"></i> bx bxs-video-off
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-video"></i> bx bxs-video
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-videos"></i> bx bxs-videos
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-volume-full"></i> bx bxs-volume-full
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-volume-low"></i> bx bxs-volume-low
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-volume-mute"></i> bx bxs-volume-mute
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-volume"></i> bx bxs-volume
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wallet"></i> bx bxs-wallet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-watch-alt"></i> bx bxs-watch-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-watch"></i> bx bxs-watch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-widget"></i> bx bxs-widget
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-wrench"></i> bx bxs-wrench
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-x-circle"></i> bx bxs-x-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-zap"></i> bx bxs-zap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-folder-open"></i> bx bxs-folder-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-battery-low"></i> bx bxs-battery-low
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-conversation"></i> bx bxs-conversation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dashboard"></i> bx bxs-dashboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-plus"></i> bx bxs-file-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-certification"></i> bx bxs-certification
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-rocket"></i> bx bxs-rocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-check-circle"></i> bx bxs-check-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-checkbox"></i> bx bxs-checkbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-checkbox-checked"></i> bx bxs-checkbox-checked
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-star-half"></i> bx bxs-star-half
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bus"></i> bx bxs-bus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bot"></i> bx bxs-bot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-area"></i> bx bxs-area
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bed"></i> bx bxs-bed
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bath"></i> bx bxs-bath
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-train"></i> bx bxs-train
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-taxi"></i> bx bxs-taxi
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-movie"></i> bx bxs-movie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-planet"></i> bx bxs-planet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-video-plus"></i> bx bxs-video-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-box"></i> bx bxs-box
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-key"></i> bx bxs-key
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-photo-album"></i> bx bxs-photo-album
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bell-ring"></i> bx bxs-bell-ring
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-blank"></i> bx bxs-file-blank
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-edit"></i> bx bxs-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ball"></i> bx bxs-ball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-film"></i> bx bxs-film
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dollar-circle"></i> bx bxs-dollar-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-skull"></i> bx bxs-skull
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-image-alt"></i> bx bxs-image-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-microphone-alt"></i> bx bxs-microphone-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-x-square"></i> bx bxs-x-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plus-square"></i> bx bxs-plus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-minus-square"></i> bx bxs-minus-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-disc"></i> bx bxs-disc
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-flame"></i> bx bxs-flame
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-badge"></i> bx bxs-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-note"></i> bx bxs-note
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-help-circle"></i> bx bxs-help-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-card"></i> bx bxs-card
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-magnet"></i> bx bxs-magnet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ambulance"></i> bx bxs-ambulance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-arrow-square"></i> bx bxs-left-arrow-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-up-arrow-square"></i> bx bxs-up-arrow-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-down-arrow-square"></i> bx bxs-down-arrow-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-arrow-square"></i> bx bxs-right-arrow-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-badge"></i> bx bxs-user-badge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-gas-pump"></i> bx bxs-gas-pump
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-landmark"></i> bx bxs-landmark
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-badge-check"></i> bx bxs-badge-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coffee-alt"></i> bx bxs-coffee-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-brush"></i> bx bxs-brush
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-keyboard"></i> bx bxs-keyboard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-megaphone"></i> bx bxs-megaphone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-directions"></i> bx bxs-directions
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-direction-right"></i> bx bxs-direction-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-joystick-button"></i> bx bxs-joystick-button
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-flask"></i> bx bxs-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-capsule"></i> bx bxs-capsule
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-color-fill"></i> bx bxs-color-fill
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-hotel"></i> bx bxs-hotel
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-magic-wand"></i> bx bxs-magic-wand
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-eraser"></i> bx bxs-eraser
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cloud-rain"></i> bx bxs-cloud-rain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cloud-lightning"></i> bx bxs-cloud-lightning
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-eyedropper"></i> bx bxs-eyedropper
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-rectangle"></i> bx bxs-user-rectangle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-plane"></i> bx bxs-plane
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tree"></i> bx bxs-tree
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-factory"></i> bx bxs-factory
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ship"></i> bx bxs-ship
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-yin-yang"></i> bx bxs-yin-yang
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-pdf"></i> bx bxs-file-pdf
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-home-circle"></i> bx bxs-home-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-location-plus"></i> bx bxs-location-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arch"></i> bx bxs-arch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-badge-dollar"></i> bx bxs-badge-dollar
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-beer"></i> bx bxs-beer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bible"></i> bx bxs-bible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bomb"></i> bx bxs-bomb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bus-school"></i> bx bxs-bus-school
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cabinet"></i> bx bxs-cabinet
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-edit"></i> bx bxs-calendar-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car-wash"></i> bx bxs-car-wash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car-garage"></i> bx bxs-car-garage
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car-mechanic"></i> bx bxs-car-mechanic
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car-crash"></i> bx bxs-car-crash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coffee-togo"></i> bx bxs-coffee-togo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chess"></i> bx bxs-chess
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dryer"></i> bx bxs-dryer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-washer"></i> bx bxs-washer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pointer"></i> bx bxs-pointer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-microchip"></i> bx bxs-microchip
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-piano"></i> bx bxs-piano
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-export"></i> bx bxs-file-export
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-import"></i> bx bxs-file-import
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-flag-checkered"></i> bx bxs-flag-checkered
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-heart-circle"></i> bx bxs-heart-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-heart-square"></i> bx bxs-heart-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-home-heart"></i> bx bxs-home-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-info-square"></i> bx bxs-info-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-layer-plus"></i> bx bxs-layer-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-layer-minus"></i> bx bxs-layer-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-traffic-cone"></i> bx bxs-traffic-cone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-mask"></i> bx bxs-mask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-low-vision"></i> bx bxs-low-vision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-radiation"></i> bx bxs-radiation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-been-here"></i> bx bxs-been-here
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-from-top"></i> bx bxs-arrow-from-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-from-bottom"></i> bx bxs-arrow-from-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-from-left"></i> bx bxs-arrow-from-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-from-right"></i> bx bxs-arrow-from-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-to-right"></i> bx bxs-arrow-to-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-to-left"></i> bx bxs-arrow-to-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-to-top"></i> bx bxs-arrow-to-top
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-arrow-to-bottom"></i> bx bxs-arrow-to-bottom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-reader"></i> bx bxs-book-reader
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-edit-location"></i> bx bxs-edit-location
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-ev-station"></i> bx bxs-ev-station
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shapes"></i> bx bxs-shapes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-florist"></i> bx bxs-florist
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-pizza"></i> bx bxs-pizza
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-week"></i> bx bxs-calendar-week
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-1"></i> bx bxs-dice-1
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-2"></i> bx bxs-dice-2
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-3"></i> bx bxs-dice-3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-4"></i> bx bxs-dice-4
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-5"></i> bx bxs-dice-5
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-dice-6"></i> bx bxs-dice-6
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-webcam"></i> bx bxs-webcam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-spray-can"></i> bx bxs-spray-can
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-file-archive"></i> bx bxs-file-archive
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-sticker"></i> bx bxs-sticker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tachometer"></i> bx bxs-tachometer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-thermometer"></i> bx bxs-thermometer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-game"></i> bx bxs-game
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-alarm-snooze"></i> bx bxs-alarm-snooze
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-alarm-exclamation"></i> bx bxs-alarm-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevrons-left"></i> bx bxs-chevrons-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevrons-right"></i> bx bxs-chevrons-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevrons-up"></i> bx bxs-chevrons-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevrons-down"></i> bx bxs-chevrons-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-down"></i> bx bxs-chevron-down
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-up"></i> bx bxs-chevron-up
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-right"></i> bx bxs-chevron-right
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-left"></i> bx bxs-chevron-left
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-guitar-amp"></i> bx bxs-guitar-amp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-up-arrow-alt"></i> bx bxs-up-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-down-arrow-alt"></i> bx bxs-down-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-left-arrow-alt"></i> bx bxs-left-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-right-arrow-alt"></i> bx bxs-right-arrow-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-medal"></i> bx bxs-medal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shopping-bags"></i> bx bxs-shopping-bags
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-baseball"></i> bx bxs-baseball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-basketball"></i> bx bxs-basketball
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-blanket"></i> bx bxs-blanket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-binoculars"></i> bx bxs-binoculars
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bone"></i> bx bxs-bone
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bong"></i> bx bxs-bong
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-alt"></i> bx bxs-book-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-heart"></i> bx bxs-book-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-book-add"></i> bx bxs-book-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-brain"></i> bx bxs-brain
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-window-alt"></i> bx bxs-window-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-heart"></i> bx bxs-calendar-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cctv"></i> bx bxs-cctv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-network-chart"></i> bx bxs-network-chart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-vector"></i> bx bxs-vector
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-exclamation"></i> bx bxs-calendar-exclamation
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-calendar-star"></i> bx bxs-calendar-star
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-camera-home"></i> bx bxs-camera-home
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-camera-movie"></i> bx bxs-camera-movie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-backpack"></i> bx bxs-backpack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cart-download"></i> bx bxs-cart-download
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cart-add"></i> bx bxs-cart-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-car-battery"></i> bx bxs-car-battery
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-right-square"></i> bx bxs-caret-right-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-up-square"></i> bx bxs-caret-up-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-left-square"></i> bx bxs-caret-left-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-caret-down-square"></i> bx bxs-caret-down-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-shield-x"></i> bx bxs-shield-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-down-circle"></i> bx bxs-chevron-down-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-up-circle"></i> bx bxs-chevron-up-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-left-circle"></i> bx bxs-chevron-left-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-right-circle"></i> bx bxs-chevron-right-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-down-square"></i> bx bxs-chevron-down-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-up-square"></i> bx bxs-chevron-up-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-left-square"></i> bx bxs-chevron-left-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-chevron-right-square"></i> bx bxs-chevron-right-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-church"></i> bx bxs-church
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coin"></i> bx bxs-coin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-coin-stack"></i> bx bxs-coin-stack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bullseye"></i> bx bxs-bullseye
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-meteor"></i> bx bxs-meteor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-home-smile"></i> bx bxs-home-smile
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-envelope-open"></i> bx bxs-envelope-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-add"></i> bx bxs-message-alt-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-check"></i> bx bxs-message-alt-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-error"></i> bx bxs-message-alt-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-x"></i> bx bxs-message-alt-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-minus"></i> bx bxs-message-alt-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-edit"></i> bx bxs-message-alt-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-alt-detail"></i> bx bxs-message-alt-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-check"></i> bx bxs-message-rounded-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-error"></i> bx bxs-message-rounded-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-x"></i> bx bxs-message-rounded-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-minus"></i> bx bxs-message-rounded-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-edit"></i> bx bxs-message-rounded-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-add"></i> bx bxs-message-rounded-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-rounded-detail"></i> bx bxs-message-rounded-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-check"></i> bx bxs-message-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-error"></i> bx bxs-message-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-x"></i> bx bxs-message-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-minus"></i> bx bxs-message-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-edit"></i> bx bxs-message-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-add"></i> bx bxs-message-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-detail"></i> bx bxs-message-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-check"></i> bx bxs-message-square-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-error"></i> bx bxs-message-square-error
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-x"></i> bx bxs-message-square-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-minus"></i> bx bxs-message-square-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-edit"></i> bx bxs-message-square-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-add"></i> bx bxs-message-square-add
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-message-square-detail"></i> bx bxs-message-square-detail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-check"></i> bx bxs-comment-check
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-x"></i> bx bxs-comment-x
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-edit"></i> bx bxs-comment-edit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-comment-minus"></i> bx bxs-comment-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-cookie"></i> bx bxs-cookie
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-copyright"></i> bx bxs-copyright
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-credit-card-front"></i> bx bxs-credit-card-front
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-crop"></i> bx bxs-crop
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-diamond"></i> bx bxs-diamond
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-door-open"></i> bx bxs-door-open
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-donate-heart"></i> bx bxs-donate-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-donate-blood"></i> bx bxs-donate-blood
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-heart"></i> bx bxs-bookmark-heart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-category"></i> bx bxs-category
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-category-alt"></i> bx bxs-category-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-alt"></i> bx bxs-bookmark-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-alt-plus"></i> bx bxs-bookmark-alt-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-bookmark-alt-minus"></i> bx bxs-bookmark-alt-minus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-face-mask"></i> bx bxs-face-mask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tv"></i> bx bxs-tv
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-tag-alt"></i> bx bxs-tag-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-movie-play"></i> bx bxs-movie-play
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-user-account"></i> bx bxs-user-account
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-virus"></i> bx bxs-virus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxs-virus-block"></i> bx bxs-virus-block
                            </b-col>
                        </b-row>

                        <h4 class="mt-5">Logos</h4>
                        <p class="text-muted mb-0">Use class <code>&lt;i class="bx bl-**">&lt;/i></code></p>
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-meta"></i> bx bxl-meta
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-upwork"></i> bx bxl-upwork
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-netlify"></i> bx bxl-netlify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-java"></i> bx bxl-java
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-heroku"></i> bx bxl-heroku
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-go-lang"></i> bx bxl-go-lang
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-gmail"></i> bx bxl-gmail
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-flask"></i> bx bxl-flask
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-99designs"></i> bx bxl-99designs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-venmo"></i> bx bxl-venmo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-docker"></i> bx bxl-docker
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-aws"></i> bx bxl-aws
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-tiktok"></i> bx bxl-tiktok
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-sketch"></i> bx bxl-sketch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-steam"></i> bx bxl-steam
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-trip-advisor"></i> bx bxl-trip-advisor
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-visual-studio"></i> bx bxl-visual-studio
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-unity"></i> bx bxl-unity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-php"></i> bx bxl-php
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-discord-alt"></i> bx bxl-discord-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-flutter"></i> bx bxl-flutter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-mastodon"></i> bx bxl-mastodon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-tailwind-css"></i> bx bxl-tailwind-css
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-instagram-alt"></i> bx bxl-instagram-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-facebook-circle"></i> bx bxl-facebook-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-jquery"></i> bx bxl-jquery
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-imdb"></i> bx bxl-imdb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-pinterest-alt"></i> bx bxl-pinterest-alt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-adobe"></i> bx bxl-adobe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-algolia"></i> bx bxl-algolia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-audible"></i> bx bxl-audible
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-figma"></i> bx bxl-figma
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-etsy"></i> bx bxl-etsy
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-gitlab"></i> bx bxl-gitlab
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-patreon"></i> bx bxl-patreon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-redbubble"></i> bx bxl-redbubble
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-facebook"></i> bx bxl-facebook
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-github"></i> bx bxl-github
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-google"></i> bx bxl-google
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-instagram"></i> bx bxl-instagram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-twitter"></i> bx bxl-twitter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-youtube"></i> bx bxl-youtube
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-whatsapp"></i> bx bxl-whatsapp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-tumblr"></i> bx bxl-tumblr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-behance"></i> bx bxl-behance
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-dribbble"></i> bx bxl-dribbble
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-vimeo"></i> bx bxl-vimeo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-linkedin"></i> bx bxl-linkedin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-bitcoin"></i> bx bxl-bitcoin
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-facebook-square"></i> bx bxl-facebook-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-google-plus"></i> bx bxl-google-plus
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-google-plus-circle"></i> bx bxl-google-plus-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-linkedin-square"></i> bx bxl-linkedin-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-medium"></i> bx bxl-medium
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-medium-square"></i> bx bxl-medium-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-skype"></i> bx bxl-skype
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-slack-old"></i> bx bxl-slack-old
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-slack"></i> bx bxl-slack
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-twitch"></i> bx bxl-twitch
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-discord"></i> bx bxl-discord
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-reddit"></i> bx bxl-reddit
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-pinterest"></i> bx bxl-pinterest
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-blogger"></i> bx bxl-blogger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-apple"></i> bx bxl-apple
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-android"></i> bx bxl-android
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-play-store"></i> bx bxl-play-store
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-windows"></i> bx bxl-windows
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-vk"></i> bx bxl-vk
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-pocket"></i> bx bxl-pocket
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-messenger"></i> bx bxl-messenger
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-500px"></i> bx bxl-500px
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-angular"></i> bx bxl-angular
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-codepen"></i> bx bxl-codepen
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-creative-commons"></i> bx bxl-creative-commons
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-digitalocean"></i> bx bxl-digitalocean
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-deviantart"></i> bx bxl-deviantart
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-discourse"></i> bx bxl-discourse
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-dropbox"></i> bx bxl-dropbox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-drupal"></i> bx bxl-drupal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-ebay"></i> bx bxl-ebay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-amazon"></i> bx bxl-amazon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-digg"></i> bx bxl-digg
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-unsplash"></i> bx bxl-unsplash
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-wikipedia"></i> bx bxl-wikipedia
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-sass"></i> bx bxl-sass
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-foursquare"></i> bx bxl-foursquare
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-invision"></i> bx bxl-invision
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-opera"></i> bx bxl-opera
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-airbnb"></i> bx bxl-airbnb
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-yelp"></i> bx bxl-yelp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-quora"></i> bx bxl-quora
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-git"></i> bx bxl-git
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-html5"></i> bx bxl-html5
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-product-hunt"></i> bx bxl-product-hunt
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-magento"></i> bx bxl-magento
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-stack-overflow"></i> bx bxl-stack-overflow
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-firefox"></i> bx bxl-firefox
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-javascript"></i> bx bxl-javascript
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-nodejs"></i> bx bxl-nodejs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-kickstarter"></i> bx bxl-kickstarter
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-vuejs"></i> bx bxl-vuejs
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-bing"></i> bx bxl-bing
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-react"></i> bx bxl-react
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-periscope"></i> bx bxl-periscope
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-wordpress"></i> bx bxl-wordpress
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-telegram"></i> bx bxl-telegram
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-stripe"></i> bx bxl-stripe
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-edge"></i> bx bxl-edge
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-paypal"></i> bx bxl-paypal
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-internet-explorer"></i> bx bxl-internet-explorer
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-joomla"></i> bx bxl-joomla
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-dailymotion"></i> bx bxl-dailymotion
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-chrome"></i> bx bxl-chrome
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-baidu"></i> bx bxl-baidu
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-visa"></i> bx bxl-visa
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-mastercard"></i> bx bxl-mastercard
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-redux"></i> bx bxl-redux
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-bootstrap"></i> bx bxl-bootstrap
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-yahoo"></i> bx bxl-yahoo
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-microsoft"></i> bx bxl-microsoft
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-css3"></i> bx bxl-css3
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-jsfiddle"></i> bx bxl-jsfiddle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-shopify"></i> bx bxl-shopify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-flickr"></i> bx bxl-flickr
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-less"></i> bx bxl-less
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-snapchat"></i> bx bxl-snapchat
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-soundcloud"></i> bx bxl-soundcloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-spotify"></i> bx bxl-spotify
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-trello"></i> bx bxl-trello
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-wix"></i> bx bxl-wix
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-mailchimp"></i> bx bxl-mailchimp
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-medium-old"></i> bx bxl-medium-old
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-squarespace"></i> bx bxl-squarespace
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-whatsapp-square"></i> bx bxl-whatsapp-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-flickr-square"></i> bx bxl-flickr-square
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-dev-to"></i> bx bxl-dev-to
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-zoom"></i> bx bxl-zoom
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-microsoft-teams"></i> bx bxl-microsoft-teams
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-blender"></i> bx bxl-blender
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-kubernetes"></i> bx bxl-kubernetes
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-google-cloud"></i> bx bxl-google-cloud
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-django"></i> bx bxl-django
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-spring-boot"></i> bx bxl-spring-boot
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-tux"></i> bx bxl-tux
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-markdown"></i> bx bxl-markdown
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-python"></i> bx bxl-python
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-ok-ru"></i> bx bxl-ok-ru
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-firebase"></i> bx bxl-firebase
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <i class="bx bxl-c-plus-plus"></i> bx bxl-c-plus-plus
                            </b-col>
                        </b-row>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>
