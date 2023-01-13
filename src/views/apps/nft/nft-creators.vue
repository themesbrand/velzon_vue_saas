<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";

export default {
    data() {
        return {
            title: "Creators",
            items: [{
                text: "NFT Marketplace",
                href: "/",
            },
            {
                text: "Creators",
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
    mounted() {

    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row class="g-4 mb-3">
            <b-col sm>
                <div>
                    <b-link href="/apps/projects-create" class="btn btn-success"><i
                            class="ri-add-line align-bottom me-1"></i> Add New</b-link>
                </div>
            </b-col>
            <b-col sm="auto">
                <div class="d-flex justify-content-sm-end gap-2">
                    <div class="search-box ms-2">
                        <input type="text" class="form-control" placeholder="Search...">
                        <i class="ri-search-line search-icon"></i>
                    </div>

                    <select class="form-control w-md" data-choices data-choices-search-false>
                        <option value="All">All</option>
                        <option value="Today">Today</option>
                        <option value="Yesterday" selected>Yesterday</option>
                        <option value="Last 7 Days">Last 7 Days</option>
                        <option value="Last 30 Days">Last 30 Days</option>
                        <option value="This Month">This Month</option>
                        <option value="Last Year">Last Year</option>
                    </select>
                </div>
            </b-col>
        </b-row>

        <b-row>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/nft/img-01.jpg" alt="" class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Timothy Smith</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 4,754 ETH
                                </p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                    class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Alexis Clarke</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 81,369
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/nft/img-06.jpg" alt="" class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Glen Matney</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 13,156
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                    class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Herbert Stokes</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 34,754
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                    class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Michael Morris</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 13,841
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/nft/img-04.jpg" alt="" class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Nancy Martino</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 26,834
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">Mary Cousar</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 18,034
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xl="3" lg="4" md="6">
                <b-card no-body>
                    <b-card-body>
                        <div class="d-flex">
                            <div class="flex-shrink-0">
                                <img src="@/assets/images/nft/img-02.jpg" alt="" class="avatar-sm object-cover rounded">
                            </div>
                            <div class="ms-3 flex-grow-1">
                                <b-link href="/pages/profile">
                                    <h5 class="mb-1">James Morris</h5>
                                </b-link>
                                <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i> 63,710
                                    ETH</p>
                            </div>
                            <div>
                                <div class="dropdown float-end">
                                    <button class="btn btn-ghost-primary btn-icon dropdown" type="button"
                                        data-bs-toggle="dropdown" aria-expanded="false">
                                        <i class="ri-more-fill align-middle fs-16"></i>
                                    </button>
                                    <ul class="dropdown-menu dropdown-menu-end">
                                        <li><b-link class="dropdown-item view-item-btn"
                                                href="javascript:void(0);">Share</b-link>
                                        </li>
                                        <li><b-link class="dropdown-item edit-item-btn" href="#!">Report</b-link></li>
                                    </ul>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <h5 class="card-title mb-4 fw-semibold fs-16">Creators Grid Lists</h5>
            </b-col>
        </b-row>

        <b-row class="row-cols-xl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-03.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-2.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Michael Morris</h5>
                        </b-link>
                        <p class="text-muted mb-2">9784 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                        class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-6.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Charles Kubik</h5>
                        </b-link>
                        <p class="text-muted mb-2">4678 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="success" class="w-100">Follow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-05.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/nft/img-06.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Alexis Clarke</h5>
                        </b-link>
                        <p class="text-muted mb-2">861 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-06.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">James Morris</h5>
                        </b-link>
                        <p class="text-muted mb-2">30174 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="https://img.themesbrand.com/velzon/images/img-3.gif" alt=""
                        class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Herbert Stokes</h5>
                        </b-link>
                        <p class="text-muted mb-2">6487 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="success" class="w-100">Follow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-03.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-2.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Michael Morris</h5>
                        </b-link>
                        <p class="text-muted mb-2">10137/ Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                        class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-6.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Tonya Noble</h5>
                        </b-link>
                        <p class="text-muted mb-2">364 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="success" class="w-100">Follow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-05.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/nft/img-06.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Nancy Martino</h5>
                        </b-link>
                        <p class="text-muted mb-2">9513 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-01.jpg" alt="" class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Kevin Dawson</h5>
                        </b-link>
                        <p class="text-muted mb-2">6374 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="success" class="w-100">Follow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                        class="object-cover card-img-top" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                            class="avatar-md rounded-circle object-cover mt-n5 border border-5 border-white mx-auto d-block">
                        <b-link href="/pages/profile">
                            <h5 class="mt-2 mb-1">Glen Matney</h5>
                        </b-link>
                        <p class="text-muted mb-2">7809 Products</p>
                        <p class="text-muted">You can make an NFT of a digital painting, a text, a piece of music, a
                            video.</p>
                        <b-button variant="soft-success" class="w-100">Unfollow</b-button>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row class="g-0 text-center text-sm-start align-items-center mb-4">
            <b-col sm="6">
                <div>
                    <p class="mb-sm-0 text-muted">Showing <span class="fw-semibold">1</span> to <span
                            class="fw-semibold">10</span> of <span
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