<script>
var echarts = require("echarts");
import worldJson from "../../../components/widgets/world.json";
export default {
    mounted() {
        let chartuser = document.getElementById("users-by-country");

        let userChart = echarts.init(chartuser);
        let useroption;
        echarts.registerMap("world", worldJson, {
            Alaska: {
                left: -131,
                top: 25,
                width: 15,
            },
            Hawaii: {
                left: -110,
                top: 28,
                width: 5,
            },
            "Puerto Rico": {
                left: -76,
                top: 26,
                width: 2,
            },
        });
        useroption = {
            tooltip: {
                trigger: "item",
                showDelay: 0,
                transitionDuration: 0.2,
            },
            series: [{
                name: "World",
                type: "map",
                map: "world",
                label: {
                    show: false,
                },
            },],
        };

        userChart.setOption(useroption);
        useroption && userChart.setOption(useroption);
    }
};
</script>
<template>
    <b-card no-body>
        <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Worldwide Top Creators</b-card-title>
            <div class="flex-shrink-0">
                <b-button type="button" variant="soft-primary" size="sm">
                    Export Report
                </b-button>
            </div>
        </b-card-header>

        <b-card-body>

            <div id="users-by-country" style="height: 269px"></div>
            <div class="mt-1">
                <p class="mb-1"><img src="@/assets/images/flags/us.svg" alt="" height="15" class="rounded me-2"> United
                    States <span class="float-end">34%</span></p>
                <p class="mb-1"><img src="@/assets/images/flags/russia.svg" alt="" height="15" class="rounded me-2">
                    Russia <span class="float-end">27%</span></p>
                <p class="mb-1"><img src="@/assets/images/flags/spain.svg" alt="" height="15" class="rounded me-2">
                    Spain
                    <span class="float-end">21%</span>
                </p>
                <p class="mb-1"><img src="@/assets/images/flags/italy.svg" alt="" height="15" class="rounded me-2">
                    Italy
                    <span class="float-end">13%</span>
                </p>
                <p class="mb-0"><img src="@/assets/images/flags/germany.svg" alt="" height="15" class="rounded me-2">
                    Germany <span class="float-end">5%</span></p>
            </div>
        </b-card-body>
    </b-card>
</template>