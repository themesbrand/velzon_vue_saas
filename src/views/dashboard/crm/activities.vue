<script>
export default {
    setup() {
        return {
            activities: [
                {
                    id: 1,
                    date: "25",
                    weekDay: "Tue",
                    time: "12:00am - 03:30pm",
                    caption: "Meeting for campaign with sales team",
                    subItem: [
                        { id: 1, img: require("@/assets/images/users/avatar-1.jpg") },
                        { id: 2, img: require("@/assets/images/users/avatar-2.jpg") },
                        { id: 3, img: require("@/assets/images/users/avatar-3.jpg") }],
                    imgNumber: "5",
                    bgcolor: "bg-info"
                },
                {
                    id: 2,
                    date: "20",
                    weekDay: "Wed",
                    time: "02:00pm - 03:45pm",
                    caption: "Adding a new event with attachments",
                    subItem: [
                        { id: 1, img: require("@/assets/images/users/avatar-4.jpg") },
                        { id: 2, img: require("@/assets/images/users/avatar-5.jpg") },
                        { id: 3, img: require("@/assets/images/users/avatar-6.jpg") },
                        { id: 4, img: require("@/assets/images/users/avatar-7.jpg") }],
                    imgNumber: "3",
                    bgcolor: "bg-success"
                },
                {
                    id: 3,
                    date: "17",
                    weekDay: "Wed",
                    time: "04:30pm - 07:15pm",
                    caption: "Create new project Bundling Product",
                    subItem: [
                        { id: 1, img: require("@/assets/images/users/avatar-8.jpg") },
                        { id: 2, img: require("@/assets/images/users/avatar-1.jpg") },
                        { id: 3, img: require("@/assets/images/users/avatar-2.jpg") }],
                    imgNumber: "4",
                    bgcolor: "bg-primary"
                },
                {
                    id: 4,
                    date: "12",
                    weekDay: "Tue",
                    time: "10:30am - 01:15pm",
                    caption: "Weekly closed sales won checking with sales team",
                    subItem: [
                        { id: 1, img: require("@/assets/images/users/avatar-1.jpg") },
                        { id: 2, img: require("@/assets/images/users/avatar-5.jpg") },
                        { id: 3, img: require("@/assets/images/users/avatar-2.jpg") }],
                    imgNumber: "9",
                    bgcolor: "bg-warning"
                },
            ]
        };
    }
};
</script>

<template>
    <b-card no-body>
        <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Upcoming Activities</b-card-title>
            <div class="flex-shrink-0">
                <div class="dropdown card-header-dropdown">
                    <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown" aria-haspopup="true"
                        aria-expanded="false">
                        <span class="text-muted fs-18"><i class="mdi mdi-dots-vertical"></i></span>
                    </b-link>
                    <div class="dropdown-menu dropdown-menu-end">
                        <b-link class="dropdown-item" href="#">Edit</b-link>
                        <b-link class="dropdown-item" href="#">Remove</b-link>
                    </div>
                </div>
            </div>
        </b-card-header>
        <b-card-body class="pt-0">
            <ul class="list-group list-group-flush border-dashed">
                <li class="list-group-item ps-0" v-for="(item, index) of activities" :key="index">
                    <b-row class="align-items-center g-3">
                        <div class="col-auto">
                            <div class="avatar-sm p-1 py-2 h-auto bg-light rounded-3">
                                <div class="text-center">
                                    <h5 class="mb-0">{{ item.date }}</h5>
                                    <div class="text-muted">{{ item.weekDay }}</div>
                                </div>
                            </div>
                        </div>
                        <b-col>
                            <h5 class="text-muted mt-0 mb-1 fs-13">{{ item.time }}</h5>
                            <b-link href="#" class="text-reset fs-14 mb-0">{{ item.caption }}</b-link>
                        </b-col>
                        <b-col sm="auto">
                            <div class="avatar-group">
                                <div class="avatar-group-item" v-for="(subitem, index) of item.subItem" :key="index">
                                    <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                                        data-bs-placement="top" title="" data-bs-original-title="Stine Nielsen">
                                        <img :src="`${subitem.img}`" alt="" class="rounded-circle avatar-xxs">
                                    </b-link>
                                </div>

                                <div class="avatar-group-item">
                                    <b-link href="javascript: void(0);">
                                        <div class="avatar-xxs">
                                            <span :class="`avatar-title rounded-circle ${item.bgcolor} text-white`">
                                                {{ item.imgNumber }}
                                            </span>
                                        </div>
                                    </b-link>
                                </div>
                            </div>
                        </b-col>
                    </b-row>
                </li>

            </ul>
            <b-row class="align-items-center mt-2 g-3 text-center text-sm-start">
                <b-col sm>
                    <div class="text-muted">Showing<span class="fw-semibold">4</span> of <span
                            class="fw-semibold">125</span> Results
                    </div>
                </b-col>
                <b-col sm="auto">
                    <ul
                        class="pagination pagination-separated pagination-sm justify-content-center justify-content-sm-start mb-0">
                        <li class="page-item disabled">
                            <b-link href="#" class="page-link">←</b-link>
                        </li>
                        <li class="page-item">
                            <b-link href="#" class="page-link">1</b-link>
                        </li>
                        <li class="page-item active">
                            <b-link href="#" class="page-link">2</b-link>
                        </li>
                        <li class="page-item">
                            <b-link href="#" class="page-link">3</b-link>
                        </li>
                        <li class="page-item">
                            <b-link href="#" class="page-link">→</b-link>
                        </li>
                    </ul>
                </b-col>
            </b-row>
        </b-card-body>
    </b-card>
</template>