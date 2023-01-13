<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";

export default {
    data() {
        return {
            title: "Marketplace",
            items: [{
                text: "NFT Marketplace",
                href: "/",
            },
            {
                text: "Marketplace",
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
        <b-row>
            <b-col xl="8">
                <b-row>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <b-row class="g-1 mb-3">
                                    <b-col lg="6">
                                        <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid rounded">
                                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                            class="img-fluid rounded mt-1">
                                    </b-col>
                                    <b-col lg="6">
                                        <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                                            class="img-fluid rounded mb-1">
                                        <img src="@/assets/images/nft/img-04.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                </b-row>
                                <b-link href="#!" class="float-end"> View All <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                                <h5 class="mb-0 fs-16">
                                    <b-link href="#!" class="link-dark">Crypto Card <b-badge variant="soft-success"
                                            class="badge-soft-success">743</b-badge>
                                    </b-link>
                                </h5>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <b-row class="g-1 mb-3">
                                    <b-col lg="6">
                                        <img src="@/assets/images/nft/img-06.jpg" alt="" class="img-fluid rounded">
                                        <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                                            class="img-fluid rounded mt-1">
                                    </b-col>
                                    <b-col lg="6">
                                        <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                            class="img-fluid rounded mb-1">
                                        <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                </b-row>
                                <b-link href="#!" class="float-end"> View All <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                                <h5 class="mb-0 fs-16">
                                    <b-link href="#!" class="link-dark">Artwork <b-badge variant="soft-success"
                                            class="badge-soft-success">206</b-badge></b-link>
                                </h5>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <b-row class="g-1 mb-3">
                                    <b-col lg="6">
                                        <img src="@/assets/images/nft/img-02.jpg" alt="" class="img-fluid rounded">
                                        <img src="https://img.themesbrand.com/velzon/images/img-3.gif" alt=""
                                            class="img-fluid rounded mt-1">
                                    </b-col>
                                    <b-col lg="6">
                                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                            class="img-fluid rounded mb-1">
                                        <img src="@/assets/images/nft/img-01.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                </b-row>
                                <b-link href="#!" class="float-end"> View All <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                                <h5 class="mb-0 fs-16">
                                    <b-link href="#!" class="link-dark">Music <b-badge variant="soft-success"
                                            class="badge-soft-success">679</b-badge></b-link>
                                </h5>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-col>
            <b-col xl="4">
                <b-alert variant="danger" show>
                    Up to <b>50% OFF</b>, Hurry up before the stock ends
                </b-alert>
                <b-card no-body class="bg-primary pattern">
                    <b-card-body class="p-4">
                        <b-badge class="bg-info fw-medium mb-3 fs-12">Trending Artwork</b-badge>
                        <h3 class="text-white lh-base">Discover, Collect, Sell and Create your own NFT</h3>
                        <p class="text-white-75 mb-3">Take advantage of the first text-based NFT. Select a text or write
                            your own and let it live forever on the Ethereum blockchain you or future owners can add
                            text to an existing ChainText token..</p>
                        <div class="hstack gap-2">
                            <b-link href="/apps/nft-create" class="btn btn-success">Create NFT</b-link>
                            <b-link href="/apps/nft-explore" class="btn btn-danger">Explore Now</b-link>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body class="overflow-hidden shadow-none">
                    <b-card-body class="bg-soft-success text-success fw-semibold d-flex">
                        <marquee class="fs-14">
                            NFT art is a digital asset that is collectable, unique, and non-transferrable, Cortes
                            explained. Every NFT is unique in it's creative design and cannot be duplicated, making them
                            limited and rare. NFTs get their value because the transaction proves ownership of the art.
                        </marquee>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <div class="d-lg-flex align-items-center mb-4">
                    <div class="flex-grow-1">
                        <h5 class="card-title mb-0 fw-semibold fs-16">Trending Artwork</h5>
                    </div>
                    <div class="flex-shrink-0 mt-4 mt-lg-0">
                        <b-link href="/apps/nft-explore" class="btn btn-soft-primary">View All <i
                                class="ri-arrow-right-line align-bottom"></i></b-link>
                    </div>
                </div>
            </b-col>
        </b-row>

        <b-row class="row-cols-xl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
            <b-col>
                <b-card no-body class="explore-box">
                    <b-card-body>
                        <div class="d-flex align-items-center mb-3">
                            <img src="@/assets/images/users/avatar-2.jpg" alt="" class="avatar-xs rounded-circle" />
                            <div class="ms-2 flex-grow-1">
                                <h6 class="mb-0 fs-15">Nancy Martino</h6>
                                <p class="mb-0 text-muted">Owners</p>
                            </div>
                            <div class="bookmark-icon">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                        </div>
                        <div class="explore-place-bid-img overflow-hidden rounded">
                            <img src="@/assets/images/nft/img-05.jpg" alt="" class="img-fluid explore-img">
                            <div class="bg-overlay"></div>
                            <div class="place-bid-btn">
                                <b-link href="#!" class="btn btn-success"><i
                                        class="ri-auction-fill align-bottom me-1"></i>
                                    Place Bid</b-link>
                            </div>
                        </div>
                        <div class="mt-3">
                            <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                                19.29k </p>
                            <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 97.8 ETH </h5>
                            <h6 class="fs-16 mb-0">
                                <b-link href="/apps/nft-item-detail" class="link-dark">Patterns arts & culture</b-link>
                            </h6>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box">
                    <b-card-body>
                        <div class="d-flex align-items-center mb-3">
                            <img src="@/assets/images/users/avatar-9.jpg" alt="" class="avatar-xs rounded-circle" />
                            <div class="ms-2 flex-grow-1">
                                <h6 class="mb-0 fs-15">Henry Baird</h6>
                                <p class="mb-0 text-muted">Creators</p>
                            </div>
                            <div class="bookmark-icon">
                                <button type="button" class="btn btn-icon" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                        </div>
                        <div class="explore-place-bid-img overflow-hidden rounded">
                            <img src="@/assets/images/nft/img-03.jpg" alt="" class="img-fluid explore-img">
                            <div class="bg-overlay"></div>
                            <div class="place-bid-btn">
                                <b-link href="#!" class="btn btn-success"><i
                                        class="ri-auction-fill align-bottom me-1"></i>
                                    Place Bid</b-link>
                            </div>
                        </div>
                        <div class="mt-3">
                            <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                                31.64k </p>
                            <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 475.23 ETH </h5>
                            <h6 class="fs-16 mb-0">
                                <b-link href="/apps/nft-item-detail" class="link-dark">Evolved Reality</b-link>
                            </h6>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box">
                    <b-card-body>
                        <div class="d-flex align-items-center mb-3">
                            <img src="@/assets/images/users/avatar-10.jpg" alt="" class="avatar-xs rounded-circle" />
                            <div class="ms-2 flex-grow-1">
                                <h6 class="mb-0 fs-15">Diana Kohler</h6>
                                <p class="mb-0 text-muted">Owners</p>
                            </div>
                            <div class="bookmark-icon">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                        </div>
                        <div class="explore-place-bid-img overflow-hidden rounded">
                            <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                                class="img-fluid explore-img">
                            <div class="bg-overlay"></div>
                            <div class="place-bid-btn">
                                <b-link href="#!" class="btn btn-success"><i
                                        class="ri-auction-fill align-bottom me-1"></i>
                                    Place Bid</b-link>
                            </div>
                        </div>
                        <div class="mt-3">
                            <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                                8.34k </p>
                            <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 701.38 ETH </h5>
                            <h6 class="fs-16 mb-0">
                                <b-link href="/apps/nft-item-detail" class="link-dark">Long-tailed macaque</b-link>
                            </h6>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box">
                    <b-card-body>
                        <div class="d-flex align-items-center mb-3">
                            <img src="@/assets/images/users/avatar-8.jpg" alt="" class="avatar-xs rounded-circle" />
                            <div class="ms-2 flex-grow-1">
                                <h6 class="mb-0 fs-15">James Price</h6>
                                <p class="mb-0 text-muted">Owners</p>
                            </div>
                            <div class="bookmark-icon">
                                <button type="button" class="btn btn-icon" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                        </div>
                        <div class="explore-place-bid-img overflow-hidden rounded">
                            <img src="@/assets/images/nft/img-06.jpg" alt="" class="img-fluid explore-img">
                            <div class="bg-overlay"></div>
                            <div class="place-bid-btn">
                                <b-link href="#!" class="btn btn-success"><i
                                        class="ri-auction-fill align-bottom me-1"></i>
                                    Place Bid</b-link>
                            </div>
                        </div>
                        <div class="mt-3">
                            <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                                29.20k </p>
                            <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 917.83 ETH </h5>
                            <h6 class="fs-16 mb-0">
                                <b-link href="/apps/nft-item-detail" class="link-dark">Robotic Body Art</b-link>
                            </h6>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box">
                    <b-card-body>
                        <div class="d-flex align-items-center mb-3">
                            <img src="@/assets/images/users/avatar-2.jpg" alt="" class="avatar-xs rounded-circle" />
                            <div class="ms-2 flex-grow-1">
                                <h6 class="mb-0 fs-15">Rickey Teran</h6>
                                <p class="mb-0 text-muted">Creators</p>
                            </div>
                            <div class="bookmark-icon">
                                <button type="button" class="btn btn-icon" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                        </div>
                        <div class="explore-place-bid-img overflow-hidden rounded">
                            <img src="https://img.themesbrand.com/velzon/images/img-3.gif" alt=""
                                class="img-fluid explore-img">
                            <div class="bg-overlay"></div>
                            <div class="place-bid-btn">
                                <b-link href="#!" class="btn btn-success"><i
                                        class="ri-auction-fill align-bottom me-1"></i>
                                    Place Bid</b-link>
                            </div>
                        </div>

                        <div class="mt-3">
                            <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                                78.34k </p>
                            <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 571.24 ETH </h5>
                            <h6 class="fs-16 mb-0">
                                <b-link href="/apps/nft-item-detail" class="link-dark">Creative filtered
                                    portrait</b-link>
                            </h6>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <div class="d-lg-flex align-items-center mb-4">
                    <div class="flex-grow-1">
                        <h5 class="card-title mb-0 fw-bold fs-16">Recent NFTs Artwork</h5>
                    </div>
                    <div class="flex-shrink-0 mt-4 mt-lg-0">
                        <b-link href="/apps/nft-creators" class="btn btn-soft-primary">View All <i
                                class="ri-arrow-right-line align-bottom"></i></b-link>
                    </div>
                </div>
            </b-col>
        </b-row>

        <b-row class="row-cols-xl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
            <b-col>
                <b-card no-body class="explore-box card-animate">
                    <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                        <button type="button" class="btn btn-icon active" data-bs-toggle="button" aria-pressed="true"><i
                                class="mdi mdi-cards-heart fs-16"></i></button>
                    </div>
                    <div class="explore-place-bid-img">
                        <img src="@/assets/images/nft/img-02.jpg" alt="" class="card-img-top explore-img" />
                        <div class="bg-overlay"></div>
                        <div class="place-bid-btn">
                            <b-link href="#!" class="btn btn-success"><i class="ri-auction-fill align-bottom me-1"></i>
                                Place
                                Bid</b-link>
                        </div>
                    </div>
                    <b-card-body>
                        <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                            23.63k </p>
                        <h5 class="mb-1">
                            <b-link href="/apps/nft-item-detail" class="link-dark">The Chirstoper</b-link>
                        </h5>
                        <p class="text-muted mb-0">Music</p>
                    </b-card-body>
                    <b-card-footer class="border-top border-top-dashed">
                        <div class="d-flex align-items-center">
                            <div class="flex-grow-1 fs-14">
                                <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest: <span
                                    class="fw-medium">412.30ETH</span>
                            </div>
                            <h5 class="flex-shrink-0 fs-14 text-primary mb-0">394.7 ETH</h5>
                        </div>
                    </b-card-footer>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box card-animate">
                    <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                        <button type="button" class="btn btn-icon active" data-bs-toggle="button" aria-pressed="true"><i
                                class="mdi mdi-cards-heart fs-16"></i></button>
                    </div>
                    <div class="explore-place-bid-img">
                        <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                            class="card-img-top explore-img" />
                        <div class="bg-overlay"></div>
                        <div class="place-bid-btn">
                            <b-link href="#!" class="btn btn-success"><i class="ri-auction-fill align-bottom me-1"></i>
                                Place
                                Bid</b-link>
                        </div>
                    </div>
                    <b-card-body>
                        <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i> 94.1k
                        </p>
                        <h5 class="mb-1">
                            <b-link href="/apps/nft-item-detail" class="link-dark">Trendy fashion portraits</b-link>
                        </h5>
                        <p class="text-muted mb-0">3d Style</p>
                    </b-card-body>
                    <b-card-footer class="border-top border-top-dashed">
                        <div class="d-flex align-items-center">
                            <div class="flex-grow-1 fs-14">
                                <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest: <span
                                    class="fw-medium">674.92 ETH</span>
                            </div>
                            <h5 class="flex-shrink-0 fs-14 text-primary mb-0">563.81 ETH</h5>
                        </div>
                    </b-card-footer>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box card-animate">
                    <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                        <button type="button" class="btn btn-icon active" data-bs-toggle="button" aria-pressed="true"><i
                                class="mdi mdi-cards-heart fs-16"></i></button>
                    </div>
                    <div class="explore-place-bid-img">
                        <img src="@/assets/images/nft/img-04.jpg" alt="" class="card-img-top explore-img" />
                        <div class="bg-overlay"></div>
                        <div class="place-bid-btn">
                            <b-link href="#!" class="btn btn-success"><i class="ri-auction-fill align-bottom me-1"></i>
                                Place
                                Bid</b-link>
                        </div>
                    </div>
                    <b-card-body>
                        <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                            34.12k </p>
                        <h5 class="mb-1">
                            <b-link href="/apps/nft-item-detail" class="link-dark">Smillevers Crypto</b-link>
                        </h5>
                        <p class="text-muted mb-0">Crypto Card</p>
                    </b-card-body>
                    <b-card-footer class="border-top border-top-dashed">
                        <div class="d-flex align-items-center">
                            <div class="flex-grow-1 fs-14">
                                <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest: <span
                                    class="fw-medium">41.658 ETH</span>
                            </div>
                            <h5 class="flex-shrink-0 fs-14 text-primary mb-0">34.81 ETH</h5>
                        </div>
                    </b-card-footer>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box card-animate">
                    <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                        <button type="button" class="btn btn-icon active" data-bs-toggle="button" aria-pressed="true"><i
                                class="mdi mdi-cards-heart fs-16"></i></button>
                    </div>
                    <div class="explore-place-bid-img">
                        <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                            class="card-img-top explore-img" />
                        <div class="bg-overlay"></div>
                        <div class="place-bid-btn">
                            <b-link href="#!" class="btn btn-success"><i class="ri-auction-fill align-bottom me-1"></i>
                                Place
                                Bid</b-link>
                        </div>
                    </div>
                    <b-card-body>
                        <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                            15.93k </p>
                        <h5 class="mb-1">
                            <b-link href="/apps/nft-item-detail" class="link-dark">Evolved Reality</b-link>
                        </h5>
                        <p class="text-muted mb-0">Video</p>
                    </b-card-body>
                    <b-card-footer class="border-top border-top-dashed">
                        <div class="d-flex align-items-center">
                            <div class="flex-grow-1 fs-14">
                                <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest: <span
                                    class="fw-medium">2.75ETH</span>
                            </div>
                            <h5 class="flex-shrink-0 fs-14 text-primary mb-0">3.167 ETH</h5>
                        </div>
                    </b-card-footer>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body class="explore-box card-animate">
                    <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                        <button type="button" class="btn btn-icon active" data-bs-toggle="button" aria-pressed="true"><i
                                class="mdi mdi-cards-heart fs-16"></i></button>
                    </div>
                    <div class="explore-place-bid-img">
                        <img src="@/assets/images/nft/img-01.jpg" alt="" class="card-img-top explore-img" />
                        <div class="bg-overlay"></div>
                        <div class="place-bid-btn">
                            <b-link href="#!" class="btn btn-success"><i class="ri-auction-fill align-bottom me-1"></i>
                                Place
                                Bid</b-link>
                        </div>
                    </div>
                    <b-card-body>
                        <p class="fw-medium mb-0 float-end"><i class="mdi mdi-heart text-danger align-middle"></i>
                            14.85k </p>
                        <h5 class="mb-1">
                            <b-link href="/apps/nft-item-detail" class="link-dark">Abstract face painting</b-link>
                        </h5>
                        <p class="text-muted mb-0">Collectibles</p>
                    </b-card-body>
                    <b-card-footer class="border-top border-top-dashed">
                        <div class="d-flex align-items-center">
                            <div class="flex-grow-1 fs-14">
                                <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest: <span
                                    class="fw-medium">122.34ETH</span>
                            </div>
                            <h5 class="flex-shrink-0 fs-14 text-primary mb-0">97.8 ETH</h5>
                        </div>
                    </b-card-footer>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <div class="d-lg-flex align-items-center mb-4">
                    <div class="flex-grow-1">
                        <h5 class="card-title mb-0 fw-semibold fs-16">Popular Creators</h5>
                    </div>
                    <div class="flex-shrink-0 mt-4 mt-lg-0">
                        <b-link href="/apps/nft-creators" class="btn btn-soft-primary">View All <i
                                class="ri-arrow-right-line align-bottom"></i></b-link>
                    </div>
                </div>
            </b-col>
        </b-row>

        <b-row class="row-cols-xl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-03.jpg" alt="" class="card-img-top object-cover" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/users/avatar-1.jpg" alt=""
                            class="avatar-md mt-n5 rounded-circle mx-auto d-block object-cover">
                        <h5 class="mt-3 mb-1">
                            <b-link href="#!" class="link-dark">Tonya Noble</b-link>
                        </h5>
                        <p class="text-muted">5048 Products</p>
                        <div>
                            <b-button variant="primary" size="sm">Follow</b-button>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                        class="card-img-top object-cover" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/nft/img-04.jpg" alt=""
                            class="avatar-md mt-n5 rounded-circle mx-auto d-block object-cover">
                        <h5 class="mt-3 mb-1">
                            <b-link href="#!" class="link-dark">Kevin Dawson</b-link>
                        </h5>
                        <p class="text-muted">649 Products</p>
                        <div>
                            <b-button variant="soft-primary" size="sm">Unfollow</b-button>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-01.jpg" alt="" class="card-img-top object-cover" height="120">
                    <b-card-body class="text-center">
                        <img src="@/assets/images/nft/img-06.jpg" alt=""
                            class="avatar-md mt-n5 rounded-circle mx-auto d-block object-cover">
                        <h5 class="mt-3 mb-1">
                            <b-link href="#!" class="link-dark">Herbert Stokes</b-link>
                        </h5>
                        <p class="text-muted">918 Products</p>
                        <div>
                            <b-button variant="soft-primary" size="sm">Unfollow</b-button>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-05.jpg" alt="" class="card-img-top object-cover" height="120">
                    <b-card-body class="text-center">
                        <img src="https://img.themesbrand.com/velzon/images/img-2.gif" alt=""
                            class="avatar-md mt-n5 rounded-circle mx-auto d-block object-cover">
                        <h5 class="mt-3 mb-1">
                            <b-link href="#!" class="link-dark">Thomas Taylor</b-link>
                        </h5>
                        <p class="text-muted">345 Products</p>
                        <div>
                            <b-button variant="primary" size="sm">Follow</b-button>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col>
                <b-card no-body>
                    <img src="@/assets/images/nft/img-02.jpg" alt="" class="card-img-top object-cover" height="120">
                    <b-card-body class="text-center">
                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif" alt=""
                            class="avatar-md mt-n5 rounded-circle mx-auto d-block object-cover">
                        <h5 class="mt-3 mb-1">
                            <b-link href="#!" class="link-dark">James Price</b-link>
                        </h5>
                        <p class="text-muted">745 Products</p>
                        <div>
                            <b-button variant="primary" size="sm">Follow</b-button>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>
<style scoped>
.pattern {
    background-image: url('../../../assets/images/nft/bg-pattern.png');
}
</style>