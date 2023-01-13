<script>
import appConfig from "../../../app.config";
import SwiperCore, {
    Thumbs,
    Navigation,
    Pagination
} from "swiper";
import {
    Swiper,
    SwiperSlide
} from "swiper/vue";
import "swiper/swiper-bundle.css";
// import {
//     CountTo
// } from "vue3-count-to";

SwiperCore.use([Thumbs, Navigation, Pagination]);
export default {
    page: {
        title: "Starter",
        meta: [{
            name: "description",
            content: appConfig.description
        }],
    },
    data() {
        return {
            title: "Starter",
            items: [{
                text: "Pages",
                href: "/",
            },
            {
                text: "Starter",
                active: true,
            },
            ],
        };
    },
    components: {
        Swiper,
        SwiperSlide,
        // CountTo,
    },
    methods: {
        topFunction() {
            document.body.scrollTop = 0;
            document.documentElement.scrollTop = 0;
        }
    },
    mounted() {


        let backtoTop = document.getElementById("back-to-top");

        if (backtoTop) {
            backtoTop = document.getElementById("back-to-top");
            window.onscroll = function () {
                if (document.body.scrollTop > 100 || document.documentElement.scrollTop > 100) {
                    backtoTop.style.display = "block";
                } else {
                    backtoTop.style.display = "none";
                }
            };
        }

        window.addEventListener('scroll', function (ev) {
            ev.preventDefault();
            var navbar = document.getElementById("navbar");
            if (navbar) {
                if (document.body.scrollTop >= 50 || document.documentElement.scrollTop >= 50) {
                    navbar.classList.add("is-sticky");
                } else {
                    navbar.classList.remove("is-sticky");
                }
            }
        });

        // filter btn
        var filterBtns = document.querySelectorAll(".filter-btns .nav-link");
        var productItems = document.querySelectorAll(".product-item");

        filterBtns.forEach(function (button) {
            button.addEventListener("click", function (e) {
                e.preventDefault();

                for (var i = 0; i < filterBtns.length; i++) {
                    filterBtns[i].classList.remove("active");
                }
                this.classList.add("active");

                var filter = e.target.dataset.filter;

                productItems.forEach(function (item) {
                    if (filter === "all") {
                        item.style.display = "block";
                    } else {
                        if (item.classList.contains(filter)) {
                            item.style.display = "block";
                        } else {
                            item.style.display = "none";
                        }
                    }
                });
            });
        });
    },
};
</script>

<template>
    <div class="layout-wrapper landing">
        <nav class="navbar navbar-expand-lg navbar-landing navbar-light fixed-top" id="navbar">
            <b-container>
                <b-link class="navbar-brand" href="/">
                    <img src="@/assets/images/logo-dark.png" class="card-logo card-logo-dark" alt="logo dark"
                        height="17">
                    <img src="@/assets/images/logo-light.png" class="card-logo card-logo-light" alt="logo light"
                        height="17">
                </b-link>
                <button class="navbar-toggler py-0 fs-20 text-body" type="button" v-b-toggle.navbarSupportedContent>
                    <i class="mdi mdi-menu"></i>
                </button>

                <b-collapse class="navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav mx-auto mt-2 mt-lg-0" id="navbar-example">
                        <li class="nav-item">
                            <b-link class="nav-link fs-14 fw-semibold active" href="#hero">Home</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fs-14 fw-semibold" href="#wallet">Wallet</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fs-14 fw-semibold" href="#marketplace">Marketplace</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fs-14 fw-semibold" href="#categories">Categories</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fs-14 fw-semibold" href="#creators">Creators</b-link>
                        </li>
                    </ul>

                    <div class="">
                        <router-link to="/apps/nft-wallet" class="btn btn-success">Wallet Connect</router-link>
                    </div>
                </b-collapse>

            </b-container>
        </nav>
        <div class="bg-overlay bg-overlay-pattern"></div>

        <section class="section nft-hero" id="hero">
            <div class="bg-overlay"></div>
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8" sm="10">
                        <div class="text-center">
                            <h1 class="display-4 fw-semibold mb-4 lh-base text-white">Discover Digital Art & Collect
                                <span class="text-success">NFT Marketplace</span>
                            </h1>
                            <p class="lead text-white-50 lh-base mb-4 pb-2">Can artwork be NFT? NFTs (non-fungible
                                tokens) are one-of-a-kind digital assets. Given they're digital in nature, can
                                physical works of art be turned into NFTs?.</p>

                            <div class="hstack gap-2 justify-content-center">
                                <router-link to="/apps/nft-create" class="btn btn-primary">Create Own <i
                                        class="ri-arrow-right-line align-middle ms-1"></i></router-link>
                                <router-link to="/apps/nft-explore" class="btn btn-danger">Explore Now <i
                                        class="ri-arrow-right-line align-middle ms-1"></i></router-link>
                            </div>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section" id="wallet">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h2 class="mb-3 fw-bold lh-base">Connect NFT Marketplace</h2>
                            <p class="text-muted">A non-fungible token is a non-interchangeable unit of data stored
                                on a blockchain, a form of digital ledger, that can be sold and traded.</p>
                        </div>
                    </b-col>
                </b-row>

                <b-row class="g-4">
                    <b-col lg="4">
                        <b-card no-body class="text-center border shadow-none">
                            <b-card-body class="py-5 px-4">
                                <img src="@/assets/images/nft/wallet/metamask.png" alt="" height="55" class="mb-3 pb-2">
                                <h5>Metamask</h5>
                                <p class="text-muted pb-1">MetaMask is a software cryptocurrency wallet used to
                                    interact with the Ethereum blockchain.</p>
                                <b-link href="#!" class="btn btn-soft-info">Connect Wallet</b-link>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4">
                        <b-card no-body class="text-center border shadow-none">
                            <b-card-body class="py-5 px-4">
                                <img src="@/assets/images/nft/wallet/coinbase.png" alt="" height="55" class="mb-3 pb-2">
                                <h5>Coinbase Wallet</h5>
                                <p class="text-muted pb-1">Coinbase Wallet is a software product that gives you
                                    access to a wide spectrum.</p>
                                <b-link href="#!" class="btn btn-info">Change Wallet</b-link>
                            </b-card-body>
                        </b-card>
                    </b-col>

                    <b-col lg="4">
                        <b-card no-body class="text-center border shadow-none">
                            <b-card-body class="py-5 px-4">
                                <img src="@/assets/images/nft/wallet/binance.png" alt="" height="55" class="mb-3 pb-2">
                                <h5>Binance</h5>
                                <p class="text-muted pb-1">Binance offers a relatively secure, versatile way to
                                    invest in and trade cryptocurrencies.</p>
                                <b-link href="#!" class="btn btn-soft-info">Connect Wallet</b-link>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section bg-light" id="marketplace">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h2 class="mb-3 fw-bold lh-base">Explore Products</h2>
                            <p class="text-muted mb-4">Collection widgets specialize in displaying many elements of
                                the same type, such as a collection of pictures from a collection of articles.</p>
                            <ul class="nav nav-pills filter-btns justify-content-center" role="tablist">
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium active" type="button" data-filter="all">All
                                        Items</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium" type="button"
                                        data-filter="artwork">Artwork</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium" type="button" data-filter="music">Music</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium" type="button" data-filter="games">Games</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium" type="button" data-filter="crypto-card">Crypto
                                        Card</button>
                                </li>
                                <li class="nav-item" role="presentation">
                                    <button class="nav-link fw-medium" type="button" data-filter="3d-style">3d
                                        Style</button>
                                </li>
                            </ul>
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col lg="4" class="product-item artwork crypto-card 3d-style">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="@/assets/images/nft/img-03.jpg" alt="" class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 19.29k </p>

                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">Creative Filtered
                                        Portrait</router-link>
                                </h5>
                                <p class="text-muted mb-0">Photography</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">75.3ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">67.36 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                    <b-col lg="4" class="product-item music crypto-card games">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="@/assets/images/nft/img-02.jpg" alt="" class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 23.63k </p>
                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">The Chirstoper</router-link>
                                </h5>
                                <p class="text-muted mb-0">Music</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">412.30ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">394.7 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                    <b-col lg="4" class="product-item artwork music games">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="https://img.themesbrand.com/velzon/images/img-4.gif" alt=""
                                    class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 15.93k </p>
                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">Evolved Reality</router-link>
                                </h5>
                                <p class="text-muted mb-0">Video</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">2.75ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">3.167 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                    <b-col lg="4" class="product-item crypto-card 3d-style">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="@/assets/images/nft/img-01.jpg" alt="" class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 14.85k </p>

                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">Abstract Face Painting</router-link>
                                </h5>
                                <p class="text-muted mb-0">Collectibles</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">122.34ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">97.8 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                    <b-col lg="4" class="product-item games music 3d-style">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="@/assets/images/nft/img-05.jpg" alt="" class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 64.10k </p>

                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">Long-tailed Macaque</router-link>
                                </h5>
                                <p class="text-muted mb-0">Artwork</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">874.01ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">745.14 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                    <b-col lg="4" class="product-item artwork music crypto-card">
                        <b-card no-body class="explore-box card-animate">
                            <div class="bookmark-icon position-absolute top-0 end-0 p-2">
                                <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                    aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                            </div>
                            <div class="explore-place-bid-img">
                                <img src="@/assets/images/nft/img-06.jpg" alt="" class="card-img-top explore-img" />
                                <div class="bg-overlay"></div>
                                <div class="place-bid-btn">
                                    <b-link href="#!" class="btn btn-success"><i
                                            class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                </div>
                            </div>
                            <b-card-body>
                                <p class="fw-medium mb-0 float-end"><i
                                        class="mdi mdi-heart text-danger align-middle"></i> 36.42k </p>

                                <h5 class="mb-1">
                                    <router-link to="/apps/nft-item-detail" class="link-dark">Robotic Body Art</router-link>
                                </h5>
                                <p class="text-muted mb-0">Artwork</p>
                            </b-card-body>
                            <b-card-footer class="border-top border-top-dashed">
                                <div class="d-flex align-items-center">
                                    <div class="flex-grow-1 fs-14">
                                        <i class="ri-price-tag-3-fill text-warning align-bottom me-1"></i> Highest:
                                        <span class="fw-medium">41.658 ETH</span>
                                    </div>
                                    <h5 class="flex-shrink-0 fs-14 text-primary mb-0">34.81 ETH</h5>
                                </div>
                            </b-card-footer>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h2 class="mb-3 fw-bold lh-base">Create and Sell Your NFTs</h2>
                            <p class="text-muted">The process of creating an NFT may cost less than a dollar, but
                                the process of selling it can cost up to a thousand dollars. For example, Allen
                                Gannett, a software developer.</p>
                        </div>
                    </b-col>
                </b-row>

                <b-row>
                    <b-col lg="3">
                        <div class="b-card no-body shadow-none">
                            <b-card-body>
                                <img src="@/assets/images/nft/wallet.png" alt="" class="avatar-sm">
                                <h5 class="mt-4">Set up your wallet</h5>
                                <p class="text-muted fs-14">You have to choose whether to use a hot wallet a cold
                                    wallet.</p>
                                <b-link href="#!" class="link-success fs-14">Read More <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                            </b-card-body>
                        </div>
                    </b-col>
                    <b-col lg="3">
                        <div class="b-card no-body shadow-none">
                            <b-card-body>
                                <img src="@/assets/images/nft/money.png" alt="" class="avatar-sm">
                                <h5 class="mt-4">Create your collection</h5>
                                <p class="text-muted fs-14">Create a collection in Opensea and give it a proper art.
                                </p>
                                <b-link href="#!" class="link-success fs-14">Read More <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                            </b-card-body>
                        </div>
                    </b-col>
                    <b-col lg="3">
                        <div class="b-card no-body shadow-none">
                            <b-card-body>
                                <img src="@/assets/images/nft/add.png" alt="" class="avatar-sm">
                                <h5 class="mt-4">Add your NFT's</h5>
                                <p class="text-muted fs-14">Go to your profile icon and top right corner creation
                                    page.</p>
                                <b-link href="#!" class="link-success fs-14">Read More <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                            </b-card-body>
                        </div>
                    </b-col>
                    <b-col lg="3">
                        <div class="b-card no-body shadow-none">
                            <b-card-body>
                                <img src="@/assets/images/nft/sell.png" alt="" class="avatar-sm">
                                <h5 class="mt-4">Sell Your NFT's</h5>
                                <p class="text-muted fs-14">Create a collection in Opensea and give Add items and
                                    art.</p>
                                <b-link href="#!" class="link-success fs-14">Read More <i
                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                            </b-card-body>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section bg-light" id="categories">
            <b-container fluid>
                <b-row class="justify-content-center">
                    <b-col lg="5">
                        <div class="text-center mb-5">
                            <h2 class="mb-3 fw-bold lh-base">Trending All Categories</h2>
                            <p class="text-muted">The process of creating an NFT may cost less than a dollar, but
                                the process of selling it can cost up to a thousand dollars. For example, Allen
                                Gannett, a software developer.</p>
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col lg="12">
                        <div class="swiper mySwiper pb-4">
                            <swiper class="swiper responsive-swiper rounded gallery-light pb-4" :loop="true"
                                :slidesPerView="1" :spaceBetween="10" :pagination="{
                                    el: '.swiper-pagination',
                                    clickable: true,
                                }" :breakpoints="{
    640: {
        slidesPerView: 2,
        spaceBetween: 20,
    },
    768: {
        slidesPerView: 3,
        spaceBetween: 40,
    },
    1200: {
        slidesPerView: 4,
        spaceBetween: 50,
    },
}">
                                <swiper-slide>
                                    <b-card no-body>
                                        <b-card-body>
                                            <b-row class="g-1 mb-3">
                                                <b-col cols="6">
                                                    <img src="@/assets/images/nft/img-06.jpg" alt=""
                                                        class="img-fluid rounded">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-2.gif"
                                                        alt="" class="img-fluid rounded mt-1">
                                                </b-col>
                                                <b-col cols="6">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-5.gif"
                                                        alt="" class="img-fluid rounded mb-1">
                                                    <img src="@/assets/images/nft/img-03.jpg" alt=""
                                                        class="img-fluid rounded">
                                                </b-col>
                                            </b-row>
                                            <b-link href="#!" class="float-end"> View All <i
                                                    class="ri-arrow-right-line align-bottom"></i></b-link>
                                            <h5 class="mb-0 fs-16">
                                                <b-link href="#!">Artwork <b-badge variant="soft-success"
                                                        class="badge-soft-success">206</b-badge>
                                                </b-link>
                                            </h5>
                                        </b-card-body>
                                    </b-card>
                                </swiper-slide>
                                <swiper-slide>
                                    <b-card no-body>
                                        <b-card-body>
                                            <b-row class="g-1 mb-3">
                                                <b-col cols="6">
                                                    <img src="@/assets/images/nft/img-05.jpg" alt=""
                                                        class="img-fluid rounded">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-1.gif"
                                                        alt="" class="img-fluid rounded mt-1">
                                                </b-col>
                                                <b-col cols="6">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-4.gif"
                                                        alt="" class="img-fluid rounded mb-1">
                                                    <img src="@/assets/images/nft/img-04.jpg" alt=""
                                                        class="img-fluid rounded">
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
                                </swiper-slide>
                                <swiper-slide>
                                    <div class="swiper-slide">
                                        <b-card no-body>
                                            <b-card-body>
                                                <b-row class="g-1 mb-3">
                                                    <b-col cols="6">
                                                        <img src="@/assets/images/nft/img-02.jpg" alt=""
                                                            class="img-fluid rounded">
                                                        <img src="https://img.themesbrand.com/velzon/images/img-3.gif"
                                                            alt="" class="img-fluid rounded mt-1">
                                                    </b-col>
                                                    <b-col cols="6">
                                                        <img src="https://img.themesbrand.com/velzon/images/img-1.gif"
                                                            alt="" class="img-fluid rounded mb-1">
                                                        <img src="@/assets/images/nft/img-01.jpg" alt=""
                                                            class="img-fluid rounded">
                                                    </b-col>
                                                </b-row>
                                                <b-link href="#!" class="float-end"> View All <i
                                                        class="ri-arrow-right-line align-bottom"></i></b-link>
                                                <h5 class="mb-0 fs-16">
                                                    <b-link href="#!" class="link-dark">Music <b-badge variant="soft-success"
                                                            class="badge-soft-success">679</b-badge>
                                                    </b-link>
                                                </h5>
                                            </b-card-body>
                                        </b-card>
                                    </div>
                                </swiper-slide>
                                <swiper-slide>
                                    <b-card no-body>
                                        <b-card-body>
                                            <b-row class="g-1 mb-3">
                                                <b-col cols="6">
                                                    <img src="@/assets/images/nft/img-03.jpg" alt=""
                                                        class="img-fluid rounded">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-5.gif"
                                                        alt="" class="img-fluid rounded mt-1">
                                                </b-col>
                                                <b-col cols="6">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-2.gif"
                                                        alt="" class="img-fluid rounded mb-1">
                                                    <img src="@/assets/images/nft/img-05.jpg" alt=""
                                                        class="img-fluid rounded">
                                                </b-col>
                                            </b-row>
                                            <b-link href="#!" class="float-end"> View All <i
                                                    class="ri-arrow-right-line align-bottom"></i></b-link>
                                            <h5 class="mb-0 fs-16">
                                                <b-link href="#!" class="link-dark">Games <b-badge variant="soft-success"
                                                        class="badge-soft-success">341</b-badge>
                                                </b-link>
                                            </h5>
                                        </b-card-body>
                                    </b-card>
                                </swiper-slide>
                                <swiper-slide>
                                    <b-card no-body>
                                        <b-card-body>
                                            <b-row class="g-1 mb-3">
                                                <b-col cols="6">
                                                    <img src="@/assets/images/nft/img-02.jpg" alt=""
                                                        class="img-fluid rounded">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-3.gif"
                                                        alt="" class="img-fluid rounded mt-1">
                                                </b-col>
                                                <b-col cols="6">
                                                    <img src="https://img.themesbrand.com/velzon/images/img-1.gif"
                                                        alt="" class="img-fluid rounded mb-1">
                                                    <img src="@/assets/images/nft/img-01.jpg" alt=""
                                                        class="img-fluid rounded">
                                                </b-col>
                                            </b-row>
                                            <b-link href="#!" class="float-end"> View All <i
                                                    class="ri-arrow-right-line align-bottom"></i></b-link>
                                            <h5 class="mb-0 fs-16">
                                                <b-link href="#!" class="link-dark">Photography <b-badge variant="soft-success"
                                                        class="badge-soft-success">1452</b-badge>
                                                </b-link>
                                            </h5>
                                        </b-card-body>
                                    </b-card>
                                </swiper-slide>
                                <div class="swiper-pagination swiper-pagination-dark"></div>
                            </swiper>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="12">
                        <div class="d-flex align-items-center mb-5">
                            <h2 class="mb-0 fw-bold lh-base flex-grow-1">Discover Items</h2>
                            <router-link to="/apps/nft-explore" class="btn btn-primary">View All <i
                                    class="ri-arrow-right-line align-bottom"></i></router-link>
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col lg="4">
                        <b-card no-body class="explore-box card-animate border">
                            <b-card-body>
                                <div class="d-flex align-items-center mb-3">
                                    <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                        class="avatar-xs rounded-circle">
                                    <div class="ms-2 flex-grow-1">
                                        <b-link href="#!">
                                            <h6 class="mb-0 fs-15">Nancy Martino</h6>
                                        </b-link>
                                        <p class="mb-0 text-muted fs-13">Owners</p>
                                    </div>
                                    <div class="bookmark-icon">
                                        <button type="button" class="btn btn-icon active" data-bs-toggle="button"
                                            aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                                    </div>
                                </div>
                                <div class="explore-place-bid-img overflow-hidden rounded">
                                    <img src="@/assets/images/nft/img-05.jpg" alt="" class="explore-img w-100">
                                    <div class="bg-overlay"></div>
                                    <div class="place-bid-btn">
                                        <b-link href="#!" class="btn btn-success"><i
                                                class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                    </div>
                                </div>
                                <div class="mt-3">
                                    <p class="fw-medium mb-0 float-end"><i
                                            class="mdi mdi-heart text-danger align-middle"></i> 19.29k </p>
                                    <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 97.8 ETH </h5>

                                    <h6 class="fs-16 mb-0">
                                        <router-link to="/apps/nft-item-detail" class="link-dark">Patterns arts &amp;
                                            culture</router-link>
                                    </h6>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4">
                        <b-card no-body class="explore-box card-animate border">
                            <b-card-body>
                                <div class="d-flex align-items-center mb-3">
                                    <img src="@/assets/images/users/avatar-9.jpg" alt=""
                                        class="avatar-xs rounded-circle">
                                    <div class="ms-2 flex-grow-1">
                                        <b-link href="#!">
                                            <h6 class="mb-0 fs-15">Henry Baird</h6>
                                        </b-link>
                                        <p class="mb-0 text-muted fs-13">Creators</p>
                                    </div>
                                    <div class="bookmark-icon">
                                        <button type="button" class="btn btn-icon" data-bs-toggle="button"
                                            aria-pressed="true"><i class="mdi mdi-cards-heart fs-16"></i></button>
                                    </div>
                                </div>
                                <div class="explore-place-bid-img overflow-hidden rounded">
                                    <img src="@/assets/images/nft/img-03.jpg" alt="" class="explore-img w-100">
                                    <div class="bg-overlay"></div>
                                    <div class="place-bid-btn">
                                        <b-link href="#!" class="btn btn-success"><i
                                                class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                    </div>
                                </div>
                                <div class="mt-3">
                                    <p class="fw-medium mb-0 float-end"><i
                                            class="mdi mdi-heart text-danger align-middle"></i> 31.64k </p>
                                    <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 475.23 ETH </h5>

                                    <h6 class="fs-16 mb-0">
                                        <router-link to="/apps/nft-item-detail" class="link-dark">Evolved Reality</router-link>
                                    </h6>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4">
                        <b-card no-body class="explore-box card-animate border">
                            <b-card-body>
                                <div class="d-flex align-items-center mb-3">
                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                        class="avatar-xs rounded-circle">
                                    <div class="ms-2 flex-grow-1">
                                        <b-link href="#!">
                                            <h6 class="mb-0 fs-15">Diana Kohler</h6>
                                        </b-link>
                                        <p class="mb-0 text-muted fs-13">Owners</p>
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
                                                class="ri-auction-fill align-bottom me-1"></i> Place Bid</b-link>
                                    </div>
                                </div>
                                <div class="mt-3">
                                    <p class="fw-medium mb-0 float-end"><i
                                            class="mdi mdi-heart text-danger align-middle"></i> 8.34k </p>
                                    <h5 class="text-success"><i class="mdi mdi-ethereum"></i> 701.38 ETH </h5>

                                    <h6 class="fs-16 mb-0">
                                        <router-link to="/apps/nft-item-detail" class="link-dark">Long-tailed
                                            macaque</router-link>
                                    </h6>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section bg-light" id="creators">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h2 class="mb-3 fw-bold lh-base">Top Creator This Week</h2>
                            <p class="text-muted">NFTs are valuable because they verify the authenticity of a
                                non-fungible asset. This makes these assets unique and one of a kind.</p>
                        </div>
                    </b-col>
                </b-row>
                <b-row>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/nft/img-01.jpg" alt=""
                                            class="avatar-sm object-cover rounded" />
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">Timothy Smith</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            4,754 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                            class="avatar-sm object-cover rounded">
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">Alexis Clarke</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            81,369 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/nft/img-06.jpg" alt=""
                                            class="avatar-sm object-cover rounded">
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">Glen Matney</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            13,156 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="https://img.themesbrand.com/velzon/images/img-5.gif" alt=""
                                            class="avatar-sm object-cover rounded">
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">Herbert Stokes</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            34,754 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                            class="avatar-sm object-cover rounded">
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">Michael Morris</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            13,841 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col xl="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/nft/img-02.jpg" alt=""
                                            class="avatar-sm object-cover rounded">
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="pages-profile">
                                            <h5 class="mb-1">James Morris</h5>
                                        </b-link>
                                        <p class="text-muted mb-0"><i class="mdi mdi-ethereum text-primary fs-14"></i>
                                            63,710 ETH</p>
                                    </div>
                                    <div>
                                        <b-dropdown variant="ghost-primary" right toggle-class="arrow-none btn-icon"
                                            class="float-end" no-caret>
                                            <template #button-content><i
                                                    class="ri-more-fill align-middle fs-16"></i></template>
                                            <b-dropdown-item href="#">Share</b-dropdown-item>
                                            <b-dropdown-item href="#">Report</b-dropdown-item>
                                        </b-dropdown>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="py-5 bg-primary position-relative">
            <div class="bg-overlay bg-overlay-pattern opacity-50"></div>
            <b-container>
                <b-row class="align-items-center gy-4">
                    <b-col sm>
                        <div>
                            <h4 class="text-white mb-0 fw-bold">Create and Sell Your NFT's</h4>
                        </div>
                    </b-col>

                    <b-col sm="auto">
                        <div>
                            <router-link to="/apps/nft-create" class="btn bg-gradient btn-danger">Create NFT
                            </router-link>
                            <router-link to="/apps/nft-explore" class="btn bg-gradient btn-info">Discover More
                            </router-link>
                        </div>
                    </b-col>

                </b-row>

            </b-container>

        </section>
        <footer class="custom-footer bg-dark py-5 position-relative">
            <b-container>
                <b-row>
                    <b-col lg="4" class="mt-4">
                        <div>
                            <div>
                                <img src="@/assets/images/logo-light.png" alt="logo light" height="17">
                            </div>
                            <div class="mt-4 fs-13">
                                <p>Premium Multipurpose Admin & Dashboard Template</p>
                                <p class="ff-secondary">You can build any type of web application like eCommerce, CRM,
                                    CMS, Project
                                    management apps, Admin Panels, etc using Velzon.</p>
                            </div>
                        </div>
                    </b-col>

                    <b-col lg="7" class="ms-lg-auto">
                        <b-row>
                            <b-col sm="4" class="mt-4">
                                <h5 class="text-white mb-0">Company</h5>
                                <div class="text-muted mt-3">
                                    <ul class="list-unstyled ff-secondary footer-list">
                                        <li>
                                            <router-link to="/pages/profile">About US</router-link>
                                        </li>
                                        <li>
                                            <router-link to="">Gallery</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/apps/projects-list">Projects</router-link>
                                        </li>
                                        <li>
                                            <router-link to="">Timeline</router-link>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                            <b-col sm="4" class="mt-4">
                                <h5 class="text-white mb-0">Apps Pages</h5>
                                <div class="text-muted mt-3">
                                    <ul class="list-unstyled ff-secondary footer-list">
                                        <li>
                                            <router-link to="/calendar">Calendar</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/mailbox">Mailbox</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/chat">Chat</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/apps/crm-deals">Deals</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/apps/tasks-kanban">kanban board</router-link>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                            <b-col sm="4" class="mt-4">
                                <h5 class="text-white mb-0">Support</h5>
                                <div class="text-muted mt-3">
                                    <ul class="list-unstyled ff-secondary footer-list">
                                        <li>
                                            <router-link to="/pages/faqs">FAQ's</router-link>
                                        </li>
                                        <li>
                                            <router-link to="/pages/faqs">Contacts</router-link>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                        </b-row>
                    </b-col>

                </b-row>

                <b-row class="text-center text-sm-start align-items-center mt-5">
                    <b-col sm="6">

                        <div>
                            <p class="copy-rights mb-0 currentyear">{{ new Date().getFullYear() }} © Velzon -
                                Themesbrand
                            </p>
                        </div>
                    </b-col>
                    <b-col sm="6">
                        <div class="text-sm-end mt-3 mt-sm-0">
                            <ul class="list-inline mb-0 footer-social-link">
                                <li class="list-inline-item">
                                    <b-link href="javascript: void(0);" class="avatar-xs d-block">
                                        <div class="avatar-title rounded-circle">
                                            <i class="ri-facebook-fill"></i>
                                        </div>
                                    </b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="javascript: void(0);" class="avatar-xs d-block">
                                        <div class="avatar-title rounded-circle">
                                            <i class="ri-github-fill"></i>
                                        </div>
                                    </b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="javascript: void(0);" class="avatar-xs d-block">
                                        <div class="avatar-title rounded-circle">
                                            <i class="ri-linkedin-fill"></i>
                                        </div>
                                    </b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="javascript: void(0);" class="avatar-xs d-block">
                                        <div class="avatar-title rounded-circle">
                                            <i class="ri-google-fill"></i>
                                        </div>
                                    </b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="javascript: void(0);" class="avatar-xs d-block">
                                        <div class="avatar-title rounded-circle">
                                            <i class="ri-dribbble-line"></i>
                                        </div>
                                    </b-link>
                                </li>
                            </ul>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </footer>
        <b-button variant="info" @click="topFunction" class="btn-icon" id="back-to-top">
            <i class="ri-arrow-up-line"></i>
        </b-button>
    </div>
</template>