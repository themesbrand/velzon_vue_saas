<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";

export default {
    data() {
        return {
            title: "Collections",
            items: [{
                text: "NFT Marketplace",
                href: "/",
            },
            {
                text: "Collections",
                active: true,
            },
            ],
        };
    },
    components: {
        Layout,
        PageHeader,
    },
    methods: {

    },
    mounted() { },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row class="g-4 mb-3 align-items-center">
            <b-col sm="auto">
                <div>
                    <h5 class="mb-0">Top Collections</h5>
                </div>
            </b-col>
            <b-col sm>
                <div class="d-flex justify-content-sm-end gap-2">
                    <div class="search-box ms-2">
                        <input type="text" class="form-control" placeholder="Search...">
                        <i class="ri-search-line search-icon"></i>
                    </div>
                    <div class="w-md">
                        <select class="form-control" data-choices data-choices-search-false>
                            <option value="All">All</option>
                            <option value="Today" selected>Today</option>
                            <option value="Yesterday">Yesterday</option>
                            <option value="Last 7 Days">Last 7 Days</option>
                            <option value="Last 30 Days">Last 30 Days</option>
                            <option value="This Month">This Month</option>
                            <option value="Last Year">Last Year</option>
                        </select>
                    </div>
                </div>
            </b-col>
        </b-row>

        <b-row>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-06.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Artwork <b-badge variant="soft-success" class="badge-soft-success">206</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-04.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Crypto Card <b-badge variant="soft-success" class="badge-soft-success">743</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-02.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-3.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-01.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Music <b-badge variant="soft-success" class="badge-soft-success">679</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Games <b-badge variant="soft-success" class="badge-soft-success">341</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-02.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-3.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-01.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Photography <b-badge variant="soft-success" class="badge-soft-success">1452</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-04.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">3d Style <b-badge variant="soft-success" class="badge-soft-success">4781</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-06.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Collectibles <b-badge variant="soft-success" class="badge-soft-success">3468</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" md="4" sm="6">
                <b-card no-body>
                    <b-card-body>
                        <b-row class="g-1 mb-3">
                            <b-col cols="6">
                                <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid rounded">
                                <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                    class="img-fluid rounded mt-1">
                            </b-col>
                            <b-col cols="6">
                                <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                                    class="img-fluid rounded mb-1">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid rounded">
                            </b-col>
                        </b-row>
                        <b-link href="#!" class="float-end"> View All <i class="ri-arrow-right-line align-bottom"></i>
                        </b-link>
                        <h5 class="mb-0 fs-16">
                            <b-link href="#!" class="link-dark">Videos <b-badge variant="soft-success" class="badge-soft-success">1674</b-badge></b-link>
                        </h5>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row class="g-0 text-center text-sm-start align-items-center mb-4">
            <b-col sm="6">
                <div>
                    <p class="mb-sm-0 text-muted">Showing <span class="fw-semibold">1</span> to <span
                            class="fw-semibold">8</span> of <span
                            class="fw-semibold text-decoration-underline">12</span> entries</p>
                </div>
            </b-col>
            <b-col sm="6">
                <ul class="pagination pagination-separated justify-content-center justify-content-sm-end mb-sm-0">
                    <li class="page-item disabled">
                        <b-link href="#" class="page-link">Previous</b-link>
                    </li>
                    <li class="page-item active">
                        <b-link href="#" class="page-link">1</b-link>
                    </li>
                    <li class="page-item ">
                        <b-link href="#" class="page-link">2</b-link>
                    </li>
                    <li class="page-item">
                        <b-link href="#" class="page-link">3</b-link>
                    </li>
                    <li class="page-item">
                        <b-link href="#" class="page-link">4</b-link>
                    </li>
                    <li class="page-item">
                        <b-link href="#" class="page-link">5</b-link>
                    </li>
                    <li class="page-item">
                        <b-link href="#" class="page-link">Next</b-link>
                    </li>
                </ul>
            </b-col>
        </b-row>
    </Layout>
</template>