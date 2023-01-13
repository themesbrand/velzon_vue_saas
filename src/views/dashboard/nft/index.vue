<script>
function getChartColorsArray(colors) {
    colors = JSON.parse(colors);
    return colors.map(function (value) {
        var newValue = value.replace(" ", "");
        if (newValue.indexOf(",") === -1) {
            var color = getComputedStyle(document.documentElement).getPropertyValue(newValue);
            if (color) {
                color = color.replace(" ", "");
                return color;
            } else return newValue;
        } else {
            var val = value.split(',');
            if (val.length == 2) {
                var rgbaColor = getComputedStyle(document.documentElement).getPropertyValue(val[0]);
                rgbaColor = "rgba(" + rgbaColor + "," + val[1] + ")";
                return rgbaColor;
            } else {
                return newValue;
            }
        }
    });
}

import {
    CountTo
} from "vue3-count-to";

import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import Marketplace from "./marketplace.vue";
import Popularity from "./popularity.vue";
import Historyofbids from "./historyofbids.vue";
import Featurednft from "./featurednft.vue";
import Topartworks from "./topartworks.vue";
import Recentnfts from "./recentnfts.vue";
import Topcollaction from "./topcollaction.vue";
import Worldwidetopcrearor from "./worldwidetopcrearor.vue";

// import Revenue from "./revenue";
// import SalesLocation from "./sales-location";

export default {
    components: {
        CountTo,
        Layout,
        // Swiper,
        // SwiperSlide,
        PageHeader,
        Marketplace,
        Popularity,
        Historyofbids,
        Featurednft,
        Topartworks,
        Recentnfts,
        Topcollaction,
        Worldwidetopcrearor
    },
    data() {
        return {
            title: "NFT Dashboard",
            items: [{
                text: "Dashboards",
                href: "/",
            },
            {
                text: "NFT Dashboard",
                active: true,
            },
            ],
            date: null,
            config: {
                mode: "range",
            },
            series: [44, 55, 41, 17, 15],
            chartOptions: {
                labels: ["Direct", "Social", "Email", "Other", "Referrals"],
                chart: {
                    height: 333,
                    type: "donut",
                },
                legend: {
                    position: "bottom",
                },
                stroke: {
                    show: false,
                },
                dataLabels: {
                    dropShadow: {
                        enabled: false,
                    },
                },
                colors: getChartColorsArray('["--vz-primary", "--vz-success", "--vz-warning", "--vz-danger", "--vz-info"]'),
            },
        };
    },
    methods: {
    }

};
</script>
  
<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row class="dash-nft">
            <b-col xxl="9">
                <b-row>
                    <b-col xl="6">
                        <b-card no-body class="overflow-hidden">
                            <b-card-body class="bg-marketplace d-flex">
                                <div class="flex-grow-1">
                                    <h4 class="fs-18 lh-base fw-bold mb-0">Discover, Collect, Sell and Create <br> your
                                        own <span class="text-success">NFTs.</span> </h4>
                                    <p class="mb-0 mt-2 pt-1 text-muted">The world's first and largest digital
                                        marketplace.</p>
                                    <div class="d-flex gap-3 mt-4">
                                        <b-link href="" class="btn btn-primary">Discover Now </b-link>
                                        <b-link href="" class="btn btn-success">Create Your Own</b-link>
                                    </div>
                                </div>
                                <img src="@/assets/images/bg-d.png" alt="" class="img-fluid" />
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="3" md="6">
                        <b-card no-body class="card-height-100">
                            <b-card-body>
                                <div class="float-end">
                                    <div class="dropdown card-header-dropdown">
                                        <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                            aria-haspopup="true" aria-expanded="false">
                                            <span class="text-muted fs-18"><i
                                                    class="mdi mdi-dots-vertical align-middle"></i></span>
                                        </b-link>
                                        <div class="dropdown-menu dropdown-menu-end">
                                            <b-link class="dropdown-item" href="#">Today</b-link>
                                            <b-link class="dropdown-item" href="#">Last Week</b-link>
                                            <b-link class="dropdown-item" href="#">Last Month</b-link>
                                            <b-link class="dropdown-item" href="#">Current Year</b-link>
                                        </div>
                                    </div>
                                </div>
                                <div class="d-flex align-items-center">
                                    <div class="avatar-sm flex-shrink-0">
                                        <span class="avatar-title bg-soft-info rounded fs-3">
                                            <i class="bx bx-dollar-circle text-info"></i>
                                        </span>
                                    </div>
                                    <div class="flex-grow-1 ps-3">
                                        <h5 class="text-muted text-uppercase fs-13 mb-0">Total Revenue</h5>
                                    </div>
                                </div>
                                <div class="mt-4 pt-1">
                                    <h4 class="fs-22 fw-semibold ff-secondary mb-0">
                                        $<count-to :startVal='20000' :endVal='559526' :duration='2000'></count-to>
                                    </h4>
                                    <p class="mt-4 mb-0 text-muted"><b-badge variant="soft-danger"
                                            class="text-danger mb-0 me-1"> <i
                                                class="ri-arrow-down-line align-middle"></i> 3.96 % </b-badge> vs. previous
                                        month</p>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="3" md="6">
                        <b-card no-body class="card-height-100">
                            <b-card-body>
                                <div class="float-end">
                                    <div class="dropdown card-header-dropdown">
                                        <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                            aria-haspopup="true" aria-expanded="false">
                                            <span class="text-muted fs-18"><i
                                                    class="mdi mdi-dots-vertical align-middle"></i></span>
                                        </b-link>
                                        <div class="dropdown-menu dropdown-menu-end">
                                            <b-link class="dropdown-item" href="#">Today</b-link>
                                            <b-link class="dropdown-item" href="#">Last Week</b-link>
                                            <b-link class="dropdown-item" href="#">Last Month</b-link>
                                            <b-link class="dropdown-item" href="#">Current Year</b-link>
                                        </div>
                                    </div>
                                </div>
                                <div class="d-flex align-items-center">
                                    <div class="avatar-sm flex-shrink-0">
                                        <span class="avatar-title bg-soft-info rounded fs-3">
                                            <i class="bx bx-wallet text-info"></i>
                                        </span>
                                    </div>
                                    <div class="flex-grow-1 ps-3">
                                        <h5 class="text-muted text-uppercase fs-13 mb-0">Estimated</h5>
                                    </div>
                                </div>
                                <div class="mt-4 pt-1">
                                    <h4 class="fs-22 fw-semibold ff-secondary mb-0">
                                        $<count-to :startVal='20000' :endVal='624562' :duration='2000'></count-to>
                                    </h4>
                                    <p class="mt-4 mb-0 text-muted"><b-badge variant="soft-success"
                                            class="text-success mb-0"> <i
                                                class="ri-arrow-up-line align-middle"></i> 16.24 % </b-badge> vs. previous
                                        month</p>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>

                <b-row>
                    <b-col xxl="12">
                        <Marketplace />
                    </b-col>
                </b-row>
            </b-col>

            <b-col xxl="3">
                <Popularity />

                <Historyofbids />
            </b-col>
        </b-row>


        <b-row>
            <Featurednft />
            <Topartworks />
        </b-row>

        <b-row>
            <b-col xxl="6">
                <Recentnfts />
            </b-col>
            <b-col xxl="3" lg="6">
                <Worldwidetopcrearor />
            </b-col>
            <b-col xxl="3" lg="6">
                <Topcollaction />
            </b-col>
        </b-row>
    </Layout>
</template>