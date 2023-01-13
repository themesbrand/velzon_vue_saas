<script>
import appConfig from "../../../app.config";
import SwiperCore, {
    Thumbs,
    Navigation,
    Pagination
} from "swiper";
import {
    Swiper, SwiperSlide
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
        Swiper, SwiperSlide,
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
    },
};
</script>

<template>
    <div class="layout-wrapper landing">
        <nav class="navbar navbar-expand-lg navbar-landing fixed-top job-navbar" id="navbar">
            <b-container fluid class="custom-container">
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
                            <b-link class="nav-link fw-semibold fs-15 active" href="#hero">Home</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fw-semibold fs-15" href="#process">Process</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fw-semibold fs-15" href="#categories">Categories</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fw-semibold fs-15" href="#findJob">Find Jobs</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fw-semibold fs-15" href="#candidates">Candidates</b-link>
                        </li>
                        <li class="nav-item">
                            <b-link class="nav-link fw-semibold fs-15" href="#blog">Blog</b-link>
                        </li>
                    </ul>

                    <div class="">
                        <b-link href="/auth/signin-basic" class="btn btn-soft-primary"><i
                                class="ri-user-3-line align-bottom me-1"></i> Login & Register</b-link>
                    </div>
                </b-collapse>

            </b-container>
        </nav>

        <section class="section job-hero-section bg-light pb-0" id="hero">
            <b-container>
                <b-row class="justify-content-between align-items-center">
                    <b-col lg="6">
                        <div>
                            <h1 class="display-6 fw-bold text-capitalize mb-3 lh-base">Find your next job and build
                                your dream here</h1>
                            <p class="lead text-muted lh-base mb-4">Find jobs, create trackable resumes and enrich your
                                applications. Carefully crafted after analyzing the needs of different industries.</p>
                            <form action="#" class="job-panel-filter">
                                <b-row class="g-md-0 g-2">
                                    <b-col md="4">
                                        <div>
                                            <input type="search" id="job-title" class="form-control filter-input-box"
                                                placeholder="Job, Company name...">
                                        </div>
                                    </b-col>
                                    <b-col md="4">
                                        <div>
                                            <select class="form-control" data-choices>
                                                <option value="">Select job type</option>
                                                <option value="Full Time">Full Time</option>
                                                <option value="Part Time">Part Time</option>
                                                <option value="Freelance">Freelance</option>
                                                <option value="Intership">Intership</option>
                                            </select>
                                        </div>
                                    </b-col>
                                    <b-col md="4">
                                        <div class="h-100">
                                            <b-button variant="primary" class="submit-btn w-100 h-100" type="submit"><i
                                                    class="ri-search-2-line align-bottom me-1"></i> Find Job</b-button>
                                        </div>
                                    </b-col>
                                </b-row>
                            </form>

                            <ul class="treding-keywords list-inline mb-0 mt-3 fs-13">
                                <li class="list-inline-item text-danger fw-semibold"><i
                                        class="mdi mdi-tag-multiple-outline align-middle"></i> Trending Keywords:</li>
                                <li class="list-inline-item">
                                    <b-link href="#">Design,</b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="#">Development,</b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="#">Manager,</b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="#">Senior</b-link>
                                </li>
                            </ul>
                        </div>
                    </b-col>
                    <b-col lg="4">
                        <div class="position-relative home-img text-center mt-5 mt-lg-0">
                            <b-card no-body class="p-3 rounded shadow-lg inquiry-box">
                                <div class="d-flex align-items-center">
                                    <div class="avatar-sm flex-shrink-0 me-3">
                                        <div class="avatar-title bg-soft-warning text-warning rounded fs-18">
                                            <i class="ri-mail-send-line"></i>
                                        </div>
                                    </div>
                                    <h5 class="fs-15 lh-base mb-0">Work Inquiry from velzon</h5>
                                </div>
                            </b-card>

                            <b-card no-body class="p-3 rounded shadow-lg application-box">
                                <h5 class="fs-15 lh-base mb-3">Applications</h5>
                                <div class="avatar-group">
                                    <b-link href="#" class="avatar-group-item" v-b-tooltip.hover title="Brent Gonzalez">
                                        <div class="avatar-xs">
                                            <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                                class="rounded-circle img-fluid">
                                        </div>
                                    </b-link>
                                    <b-link href="#" class="avatar-group-item" v-b-tooltip.hover title="Ellen Smith">
                                        <div class="avatar-xs">
                                            <div class="avatar-title rounded-circle bg-danger">
                                                S
                                            </div>
                                        </div>
                                    </b-link>
                                    <b-link href="#" class="avatar-group-item" v-b-tooltip.hover title="Ellen Smith">
                                        <div class="avatar-xs">
                                            <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                class="rounded-circle img-fluid">
                                        </div>
                                    </b-link>
                                    <b-link href="#" class="avatar-group-item">
                                        <div class="avatar-xs">
                                            <div class="avatar-title rounded-circle bg-success">
                                                Z
                                            </div>
                                        </div>
                                    </b-link>
                                    <b-link href="#" class="avatar-group-item" v-b-tooltip.hover title="Brent Gonzalez">
                                        <div class="avatar-xs">
                                            <img src="@/assets/images/users/avatar-9.jpg" alt=""
                                                class="rounded-circle img-fluid">
                                        </div>
                                    </b-link>
                                    <b-link href="#" class="avatar-group-item" v-b-tooltip.hover
                                        title="More Appliances">
                                        <div class="avatar-xs">
                                            <div
                                                class="avatar-title fs-13 rounded-circle bg-light border-dashed border text-primary">
                                                2k+
                                            </div>
                                        </div>
                                    </b-link>
                                </div>
                            </b-card>
                            <img src="@/assets/images/job-profile2.png" alt="" class="user-img">

                            <div class="circle-effect">
                                <div class="circle"></div>
                                <div class="circle2"></div>
                                <div class="circle3"></div>
                                <div class="circle4"></div>
                            </div>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section" id="process">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h1 class="mb-3 ff-secondary fw-bold lh-base">How <span class="text-primary">it's
                                    work</span> creative jobs & quickly features</h1>
                            <p class="text-muted">A creative person has the ability to invent and develop original
                                ideas, especially in the arts. Like so many creative people, he was never satisfied.</p>
                        </div>
                    </b-col>

                </b-row>
                <b-row>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body class="p-4">
                                <h1 class="fw-bold display-5 ff-secondary mb-4 text-success position-relative">
                                    <div class="job-icon-effect"></div>
                                    <span>1</span>
                                </h1>
                                <h6 class="fs-17 mb-2">Register Account</h6>
                                <p class="text-muted mb-0 fs-15">First, You need to make a account.</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none">
                            <b-card-body class="p-4">
                                <h1 class="fw-bold display-5 ff-secondary mb-4 text-success position-relative">
                                    <div class="job-icon-effect"></div>
                                    <span>2</span>
                                </h1>
                                <h6 class="fs-17 mb-2">Create Resume</h6>
                                <p class="text-muted mb-0 fs-15">Create a resume for your job.</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none">
                            <b-card-body class="p-4">
                                <h1 class="fw-bold display-5 ff-secondary mb-4 text-success position-relative">
                                    <div class="job-icon-effect"></div>
                                    <span>3</span>
                                </h1>

                                <h6 class="fs-17 mb-2">Find Job</h6>
                                <p class="text-muted mb-0 fs-15">Search for your dream jobs from velzon.</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none">
                            <b-card-body class="p-4">
                                <h1 class="fw-bold display-5 ff-secondary mb-4 text-success position-relative">
                                    <div class="job-icon-effect"></div>
                                    <span>4</span>
                                </h1>
                                <h6 class="fs-17 mb-2">Apply Job</h6>
                                <p class="text-muted mb-0 fs-15">Apply to the compnay and wait for interview.</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section">
            <b-container>
                <b-row class="align-items-center justify-content-lg-between justify-content-center gy-4">
                    <b-col lg="5" sm="7">
                        <div class="about-img-section mb-5 mb-lg-0 text-center">
                            <b-card no-body class="rounded shadow-lg inquiry-box d-none d-lg-block">
                                <b-card-body class="d-flex align-items-center">
                                    <div class="avatar-sm flex-shrink-0 me-3">
                                        <div class="avatar-title bg-soft-secondary text-secondary rounded-circle fs-18">
                                            <i class="ri-briefcase-2-line"></i>
                                        </div>
                                    </div>
                                    <h5 class="fs-15 lh-base mb-0">Search Over <span
                                            class="text-secondary fw-semibold">1,00,000+</span> Jobs</h5>
                                </b-card-body>
                            </b-card>

                            <b-card no-body class="feedback-box">
                                <b-card-body class="d-flex shadow-lg">
                                    <div class="flex-shrink-0 me-3">
                                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                            class="avatar-sm rounded-circle">
                                    </div>
                                    <div class="flex-grow-1">
                                        <h5 class="fs-14 lh-base mb-0">Tonya Noble</h5>
                                        <p class="text-muted fs-11 mb-1">UI/UX Designer</p>

                                        <div class="text-warning">
                                            <i class="ri-star-s-fill"></i>
                                            <i class="ri-star-s-fill"></i>
                                            <i class="ri-star-s-fill"></i>
                                            <i class="ri-star-s-fill"></i>
                                            <i class="ri-star-s-line"></i>
                                        </div>
                                    </div>
                                </b-card-body>
                            </b-card>
                            <img src="@/assets/images/about.jpg" alt="" class="img-fluid mx-auto rounded-3" />
                        </div>
                    </b-col>
                    <b-col lg="6">
                        <div class="text-muted">
                            <h1 class="mb-3 lh-base">Find Your <span class="text-primary">Dream Job</span> in One Place
                            </h1>
                            <p class="ff-secondary fs-16 mb-2">The first step in finding your <b>dream job </b> is
                                deciding where to look for first-hand insight. Contact professionals who are already
                                working in industries or positions that interest you.</p>
                            <p class="ff-secondary fs-16">Schedule informational interviews and phone calls or ask for
                                the opportunity to shadow them on the job.</p>

                            <div class="vstack gap-2 mb-4 pb-1">
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-2">
                                        <div class="avatar-xs icon-effect">
                                            <div class="avatar-title bg-transparent text-success rounded-circle h2">
                                                <i class="ri-check-fill"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1">
                                        <p class="mb-0">Dynamic Conetnt</p>
                                    </div>
                                </div>
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-2">
                                        <div class="avatar-xs icon-effect">
                                            <div class="avatar-title bg-transparent text-success rounded-circle h2">
                                                <i class="ri-check-fill"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1">
                                        <p class="mb-0">Setup plugin's information.</p>
                                    </div>
                                </div>
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-2">
                                        <div class="avatar-xs icon-effect">
                                            <div class="avatar-title bg-transparent text-success rounded-circle h2">
                                                <i class="ri-check-fill"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1">
                                        <p class="mb-0">Themes customization information</p>
                                    </div>
                                </div>
                            </div>

                            <div>
                                <b-link href="#!" class="btn btn-primary">Find Your Jobs <i
                                        class="ri-arrow-right-line align-bottom ms-1"></i></b-link>
                            </div>
                        </div>
                    </b-col>

                </b-row>
            </b-container>
        </section>

        <section class="section bg-light" id="categories">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="7">
                        <div class="text-center mb-5">
                            <h1 class="mb-3 ff-secondary fw-bold text-capitalize lh-base">High demand jobs <span
                                    class="text-primary">Categories</span> fratured</h1>
                            <p class="text-muted">Post a job to tell us about your project. We'll quickly match you with
                                the right freelancers.</p>
                        </div>
                    </b-col>

                </b-row>

                <b-row class="justify-content-center">
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-pencil-ruler-2-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">IT & Software</h5>
                                </b-link>
                                <p class="mb-0 text-muted">1543 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-airplay-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Construction / Facilities</h5>
                                </b-link>
                                <p class="mb-0 text-muted">3241 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm mb-4 mx-auto position-relative">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-bank-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Government</h5>
                                </b-link>
                                <p class="mb-0 text-muted">876 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-focus-2-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Marketing & Advertising</h5>
                                </b-link>
                                <p class="mb-0 text-muted">465 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-pencil-ruler-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Education & training</h5>
                                </b-link>
                                <p class="mb-0 text-muted">105 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-line-chart-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Digital Marketing</h5>
                                </b-link>
                                <p class="mb-0 text-muted">377 Jobs</p>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="3" md="6">
                        <b-card no-body class="shadow-none text-center py-3">
                            <b-card-body class="py-4">
                                <div class="avatar-sm position-relative mb-4 mx-auto">
                                    <div class="job-icon-effect"></div>
                                    <div class="avatar-title bg-transparent text-success rounded-circle">
                                        <i class="ri-briefcase-2-line fs-1"></i>
                                    </div>
                                </div>
                                <b-link href="#!" class="stretched-link">
                                    <h5 class="fs-17 pt-1">Catering & Tourism</h5>
                                </b-link>
                                <p class="mb-0 text-muted">85 Jobs</p>
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
                            <h4 class="text-white mb-2">Ready to Started?</h4>
                            <p class="text-white-50 mb-0">Create new account and refer your friend</p>
                        </div>
                    </b-col>

                    <b-col sm="auto">
                        <div>
                            <b-link href="#!" class="btn bg-gradient btn-danger">Create Free Account</b-link>
                        </div>
                    </b-col>

                </b-row>
            </b-container>
        </section>

        <section class="section" id="findJob">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="7">
                        <div class="text-center mb-5">
                            <h1 class="mb-3 ff-secondary fw-bold text-capitalize lh-base">Find Your <span
                                    class="text-primary">Career</span> You Deserve it</h1>
                            <p class="text-muted">Post a job to tell us about your project. We'll quickly match you with
                                the right freelancers.</p>
                        </div>
                    </b-col>

                </b-row>

                <b-row>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-warning rounded">
                                            <img src="@/assets/images/companies/img-3.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>UI/UX designer</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Nesta Technologies
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> USA
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $23k - 35k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-success" class="badge-soft-success">Design</b-badge>
                                            <b-badge variant="soft-danger" class="badge-soft-danger">UI/UX</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Adobe XD</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary" class="btn-icon custom-toggle"
                                            data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-primary rounded">
                                            <img src="@/assets/images/companies/img-2.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Product Sales Specialist</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Digitech Galaxy
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> Spain
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $10k - 15k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Sales</b-badge>
                                            <b-badge variant="soft-secondary" class="badge-soft-secondary">Product</b-badge>
                                            <b-badge variant="soft-info" class="badge-soft-info">Bussiness</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary"
                                            class="btn-icon custom-toggle active" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-danger rounded">
                                            <img src="@/assets/images/companies/img-4.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Marketing Director</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Meta4Systems
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> Sweden
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $20k - 25k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-warning" class="badge-soft-warning">Marketing</b-badge>
                                            <b-badge variant="soft-info" class="badge-soft-info">Bussiness</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary"
                                            class="btn-icon custom-toggle active" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-success rounded">
                                            <img src="@/assets/images/companies/img-9.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Product Designer</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Themesbrand
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> USA
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $40k+
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-success" class="badge-soft-success">Design</b-badge>
                                            <b-badge variant="soft-danger" class="badge-soft-danger">UI/UX</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Adobe XD</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary" class="btn-icon custom-toggle" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-info rounded">
                                            <img src="@/assets/images/companies/img-1.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Project Manager</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Syntyce Solutions
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> Germany
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $18k - 26k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-danger" class="badge-soft-danger">HR</b-badge>
                                            <b-badge variant="soft-success" class="badge-soft-success">Manager</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary" class="btn-icon custom-toggle" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-success rounded">
                                            <img src="@/assets/images/companies/img-7.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Business Associate</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Nesta Technologies
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> USA
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $23k - 35k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-success" class="badge-soft-success">Design</b-badge>
                                            <b-badge variant="soft-danger" class="badge-soft-danger">UI/UX</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Adobe XD</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary"
                                            class="btn-icon custom-toggle active" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-info rounded">
                                            <img src="@/assets/images/companies/img-8.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Recruiting Coordinator</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Zoetic Fashion
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> Namibia
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $12k - 15k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-success" class="badge-soft-success">Full Time</b-badge>
                                            <b-badge variant="soft-info" class="badge-soft-info">Remote</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Fashion</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary"
                                            class="btn-icon custom-toggle active" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="6">
                        <b-card no-body class="shadow-lg">
                            <b-card-body>
                                <div class="d-flex">
                                    <div class="avatar-sm">
                                        <div class="avatar-title bg-soft-warning rounded">
                                            <img src="@/assets/images/companies/img-5.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <div class="ms-3 flex-grow-1">
                                        <b-link href="#!">
                                            <h5>Customs officer</h5>
                                        </b-link>
                                        <ul class="list-inline text-muted mb-3">
                                            <li class="list-inline-item">
                                                <i class="ri-building-line align-bottom me-1"></i> Nesta Technologies
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-map-pin-2-line align-bottom me-1"></i> USA
                                            </li>
                                            <li class="list-inline-item">
                                                <i class="ri-money-dollar-circle-line align-bottom me-1"></i> $41k - 45k
                                            </li>
                                        </ul>
                                        <div class="hstack gap-2">
                                            <b-badge variant="soft-success" class="badge-soft-success">Design</b-badge>
                                            <b-badge variant="soft-danger" class="badge-soft-danger">UI/UX</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Adobe XD</b-badge>
                                        </div>
                                    </div>
                                    <div>
                                        <b-button type="button" variant="ghost-primary" class="btn-icon custom-toggle" data-bs-toggle="button">
                                            <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                                            <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                                        </b-button>
                                    </div>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="12">
                        <div class="text-center mt-4">
                            <b-link href="#!" class="btn btn-ghost-primary">View More Jobs <i
                                    class="ri-arrow-right-line align-bottom"></i></b-link>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section">
            <b-container>
                <b-row class="align-items-center gy-4">
                    <b-col lg="6" class="order-2 order-lg-1">
                        <div class="text-muted mt-5 mt-lg-0">
                            <h5 class="fs-12 text-uppercase text-success">Hot Featured Company</h5>
                            <h1 class="mb-3 ff-secondary fw-bold text-capitalize lh-base">Get <span
                                    class="text-primary">10,000+</span> Featured Companies</h1>
                            <p class="ff-secondary mb-2">The demand for content writing services is growing. This is
                                because content is required in almost every industry. <b>Many companies have discovered
                                    how effective content marketing is.</b> This is a major reason for this increase in
                                demand.</p>
                            <p class="mb-4 ff-secondary">A Content Writer is a professional who writes informative and
                                engaging articles to help brands showcase their products.</p>

                            <div class="mt-4">
                                <b-link href="/" class="btn btn-primary">View More Companies <i
                                        class="ri-arrow-right-line align-middle ms-1"></i></b-link>
                            </div>
                        </div>
                    </b-col>

                    <b-col lg="4" sm="7" cols="10" order="1" order-lg="2" class="ms-lg-auto mx-auto">
                        <div>
                            <b-card no-body class="shadow-lg">
                                <b-card-body>
                                    <b-button variant="soft-primary" type="button" class="btn-icon float-end"
                                        data-bs-toggle="button" aria-pressed="true"><i
                                            class="mdi mdi-cards-heart fs-16"></i></b-button>
                                    <div class="avatar-sm mb-4">
                                        <div class="avatar-title bg-soft-secondary rounded">
                                            <img src="@/assets/images/companies/img-1.png" alt="" class="avatar-xxs">
                                        </div>
                                    </div>
                                    <b-link href="#!">
                                        <h5>New Web designer</h5>
                                    </b-link>
                                    <p class="text-muted">Themesbrand</p>

                                    <div class="d-flex gap-4 mb-3">
                                        <div>
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido,California
                                        </div>

                                        <div>
                                            <i class="ri-time-line text-primary me-1 align-bottom"></i> 3 min ago
                                        </div>
                                    </div>

                                    <p class="text-muted">As a Product Designer, you will work within a Product Delivery
                                        Team fused with UX, engineering, product and data talent.</p>

                                    <div class="hstack gap-2">
                                        <b-badge variant="soft-success" class="badge-soft-success">Full Time</b-badge>
                                        <b-badge variant="soft-primary" class="badge-soft-primary">Freelance</b-badge>
                                        <b-badge variant="soft-danger" class="badge-soft-danger">Urgent</b-badge>
                                    </div>

                                    <div class="mt-4 hstack gap-2">
                                        <b-link href="#!" class="btn btn-soft-primary w-100">Apply Job</b-link>
                                        <b-link href="#!" class="btn btn-soft-success w-100">Overview</b-link>
                                    </div>
                                </b-card-body>
                            </b-card>
                            <b-card no-body class="shadow-lg bg-info mb-0 features-company-widgets rounded-3">
                                <b-card-body>
                                    <h5 class="text-white fs-16 mb-4">10,000+ Featured Companies</h5>

                                    <div class="d-flex gap-1">
                                        <b-link href="#" v-b-tooltip.hover title="Brent Gonzalez">
                                            <div class="avatar-xs">
                                                <div class="avatar-title bg-light bg-opacity-25 rounded-circle">
                                                    <img src="@/assets/images/companies/img-5.png" alt="" height="15">
                                                </div>
                                            </div>
                                        </b-link>
                                        <b-link href="#" v-b-tooltip.hover title="Brent Gonzalez">
                                            <div class="avatar-xs">
                                                <div class="avatar-title bg-light bg-opacity-25 rounded-circle">
                                                    <img src="@/assets/images/companies/img-2.png" alt="" height="15">
                                                </div>
                                            </div>
                                        </b-link>
                                        <b-link href="#" v-b-tooltip.hover title="Brent Gonzalez">
                                            <div class="avatar-xs">
                                                <div class="avatar-title bg-light bg-opacity-25 rounded-circle">
                                                    <img src="@/assets/images/companies/img-8.png" alt="" height="15">
                                                </div>
                                            </div>
                                        </b-link>
                                        <b-link href="#" v-b-tooltip.hover title="Brent Gonzalez">
                                            <div class="avatar-xs">
                                                <div class="avatar-title bg-light bg-opacity-25 rounded-circle">
                                                    <img src="@/assets/images/companies/img-7.png" alt="" height="15">
                                                </div>
                                            </div>
                                        </b-link>
                                        <b-link href="#" v-b-tooltip.hover title="More Companies">
                                            <div class="avatar-xs">
                                                <div
                                                    class="avatar-title fs-11 rounded-circle bg-light bg-opacity-25 text-white">
                                                    1k+
                                                </div>
                                            </div>
                                        </b-link>
                                    </div>
                                </b-card-body>
                            </b-card>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section bg-light" id="candidates">
            <div class="bg-overlay bg-overlay-pattern"></div>
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h1 class="mb-3 ff-secondary fw-bold text-capitalize lh-base">Hire Experts <span
                                    class="text-primary">Team</span></h1>
                            <p class="text-muted mb-4">Hiring experts costs more per hour than hiring entry- or
                                mid-level freelancers, but they can usually get the work done faster—and better.</p>
                        </div>
                    </b-col>

                </b-row>
                <b-row>
                    <b-col lg="12">
                        <swiper class="swiper candidate-swiper" :loop="true" :slidesPerView="1" :spaceBetween="10"
                            :pagination="{
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
                                <b-card no-body class="text-center">
                                    <b-card-body class="p-4">
                                        <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                            class="rounded-circle avatar-md mx-auto d-block">
                                        <h5 class="fs-17 mt-3 mb-2">Nancy Martino</h5>
                                        <p class="text-muted fs-13 mb-3">Creative Designer</p>

                                        <p class="text-muted mb-4 fs-14">
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido, California
                                        </p>

                                        <b-link href="#!" class="btn btn-primary w-100">View Profile</b-link>
                                    </b-card-body>
                                </b-card>
                            </swiper-slide>
                            <swiper-slide>
                                <b-card no-body class="text-center">
                                    <b-card-body class="p-4">
                                        <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                            class="rounded-circle avatar-md mx-auto d-block">
                                        <h5 class="fs-17 mt-3 mb-2">Glen Matney</h5>
                                        <p class="text-muted fs-13 mb-3">Marketing Director</p>

                                        <p class="text-muted mb-4 fs-14">
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido, California
                                        </p>

                                        <b-link href="#!" class="btn btn-primary w-100">View Profile</b-link>
                                    </b-card-body>
                                </b-card>
                            </swiper-slide>
                            <swiper-slide>
                                <b-card no-body class="text-center">
                                    <b-card-body class="p-4">
                                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                            class="rounded-circle avatar-md mx-auto d-block">
                                        <h5 class="fs-17 mt-3 mb-2">Alexis Clarke</h5>
                                        <p class="text-muted fs-13 mb-3">Product Manager</p>

                                        <p class="text-muted mb-4 fs-14">
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido, California
                                        </p>

                                        <b-link href="#!" class="btn btn-primary w-100">View Profile</b-link>
                                    </b-card-body>
                                </b-card>
                            </swiper-slide>
                            <swiper-slide>
                                <b-card no-body class="text-center">
                                    <b-card-body class="p-4">
                                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                            class="rounded-circle avatar-md mx-auto d-block" />
                                        <h5 class="fs-17 mt-3 mb-2">James Price</h5>
                                        <p class="text-muted fs-13 mb-3">Product Designer</p>

                                        <p class="text-muted mb-4 fs-14">
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido, California
                                        </p>

                                        <b-link href="#!" class="btn btn-primary w-100">View Profile</b-link>
                                    </b-card-body>
                                </b-card>
                            </swiper-slide>
                            <swiper-slide>
                                <b-card no-body class="text-center">
                                    <b-card-body class="p-4">
                                        <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                            class="rounded-circle avatar-md mx-auto d-block" />
                                        <h5 class="fs-17 mt-3 mb-2">Michael Morris</h5>
                                        <p class="text-muted fs-13 mb-3">Full Stack Developer</p>

                                        <p class="text-muted mb-4 fs-14">
                                            <i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i>
                                            Escondido, California
                                        </p>

                                        <b-link href="#!" class="btn btn-primary w-100">View Profile</b-link>
                                    </b-card-body>
                                </b-card>
                            </swiper-slide>
                        </swiper>
                    </b-col>
                </b-row>
            </b-container>
        </section>

        <section class="section" id="blog">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col lg="8">
                        <div class="text-center mb-5">
                            <h1 class="mb-3 ff-secondary fw-bold text-capitalize lh-base">Our Latest <span
                                    class="text-primary">News</span></h1>
                            <p class="text-muted mb-4">We thrive when coming up with innovative ideas but also
                                understand that a smart concept should be supported with faucibus sapien odio measurable
                                results.</p>
                        </div>
                    </b-col>
                </b-row>

                <b-row>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <img src="@/assets/images/small/img-8.jpg" alt="" class="img-fluid rounded" />
                            </b-card-body>
                            <b-card-body>
                                <ul class="list-inline fs-14 text-muted">
                                    <li class="list-inline-item">
                                        <i class="ri-calendar-line align-bottom me-1"></i> 30 Oct, 2021
                                    </li>
                                    <li class="list-inline-item">
                                        <i class="ri-message-2-line align-bottom me-1"></i> 364 Comment
                                    </li>
                                </ul>
                                <b-link href="#;">
                                    <h5>Design your apps in your own way ?</h5>
                                </b-link>
                                <p class="text-muted fs-14">One disadvantage of Lorum Ipsum is that in Latin certain
                                    letters appear more frequently than others.</p>

                                <div>
                                    <b-link href="#!" class="link-success">Learn More <i
                                            class="ri-arrow-right-line align-bottom ms-1"></i></b-link>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <img src="@/assets/images/small/img-6.jpg" alt="" class="img-fluid rounded" />
                            </b-card-body>
                            <b-card-body>
                                <ul class="list-inline fs-14 text-muted">
                                    <li class="list-inline-item">
                                        <i class="ri-calendar-line align-bottom me-1"></i> 02 Oct, 2021
                                    </li>
                                    <li class="list-inline-item">
                                        <i class="ri-message-2-line align-bottom me-1"></i> 245 Comment
                                    </li>
                                </ul>
                                <b-link href="#;">
                                    <h5>Smartest Applications for Business ?</h5>
                                </b-link>
                                <p class="text-muted fs-14">Due to its widespread use as filler text for layouts,
                                    non-readability is of great importance: human perception.</p>

                                <div>
                                    <b-link href="#!" class="link-success">Learn More <i
                                            class="ri-arrow-right-line align-bottom ms-1"></i></b-link>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                    <b-col lg="4" md="6">
                        <b-card no-body>
                            <b-card-body>
                                <img src="@/assets/images/small/img-9.jpg" alt="" class="img-fluid rounded" />
                            </b-card-body>
                            <b-card-body>
                                <ul class="list-inline fs-14 text-muted">
                                    <li class="list-inline-item">
                                        <i class="ri-calendar-line align-bottom me-1"></i> 23 Sept, 2021
                                    </li>
                                    <li class="list-inline-item">
                                        <i class="ri-message-2-line align-bottom me-1"></i> 354 Comment
                                    </li>
                                </ul>
                                <b-link href="#;">
                                    <h5>How apps is changing the IT world</h5>
                                </b-link>
                                <p class="text-muted fs-14">Intrinsically incubate intuitive opportunities and real-time
                                    potentialities Appropriately communicate one-to-one technology.</p>

                                <div>
                                    <b-link href="#!" class="link-success">Learn More <i
                                            class="ri-arrow-right-line align-bottom ms-1"></i></b-link>
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
                            <h4 class="text-white fw-semibold">Get New Jobs Notification!</h4>
                            <p class="text-white-75 mb-0">Subscribe & get all related jobs notification.</p>
                        </div>
                    </b-col>

                    <b-col sm="auto">
                        <b-button type="button" variant="danger">Subscribe Now <i class="ri-arrow-right-line align-bottom"></i></b-button>
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
                                <img src="@/assets/images/logo-light.png" alt="logo light" height="17" />
                            </div>
                            <div class="mt-4 fs-13">
                                <p>Premium Multipurpose Admin & Dashboard Template</p>
                                <p>You can build any type of web application like eCommerce, CRM, CMS, Project
                                    management apps, Admin Panels, etc using Velzon.</p>
                                <ul class="list-inline mb-0 footer-social-link">
                                    <li class="list-inline-item">
                                        <b-link href="#" class="avatar-xs d-block">
                                            <div class="avatar-title rounded-circle">
                                                <i class="ri-facebook-fill"></i>
                                            </div>
                                        </b-link>
                                    </li>
                                    <li class="list-inline-item">
                                        <b-link href="#" class="avatar-xs d-block">
                                            <div class="avatar-title rounded-circle">
                                                <i class="ri-github-fill"></i>
                                            </div>
                                        </b-link>
                                    </li>
                                    <li class="list-inline-item">
                                        <b-link href="#" class="avatar-xs d-block">
                                            <div class="avatar-title rounded-circle">
                                                <i class="ri-linkedin-fill"></i>
                                            </div>
                                        </b-link>
                                    </li>
                                    <li class="list-inline-item">
                                        <b-link href="#" class="avatar-xs d-block">
                                            <div class="avatar-title rounded-circle">
                                                <i class="ri-google-fill"></i>
                                            </div>
                                        </b-link>
                                    </li>
                                    <li class="list-inline-item">
                                        <b-link href="#" class="avatar-xs d-block">
                                            <div class="avatar-title rounded-circle">
                                                <i class="ri-dribbble-line"></i>
                                            </div>
                                        </b-link>
                                    </li>
                                </ul>
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
                                            <b-link href="/pages/profile">About Us</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#">Gallery</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/pages/team">Team</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/pages/pricing">Pricing</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/pages/timeline">Timeline</b-link>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                            <b-col sm="4" class="mt-4">
                                <h5 class="text-white mb-0">For Jobs</h5>
                                <div class="text-muted mt-3">
                                    <ul class="list-unstyled ff-secondary footer-list">
                                        <li>
                                            <b-link href="/jobs/lists">Job List</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/jobs/application">application</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/jobs/new">New Job</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/jobs/companies-list">Company List</b-link>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                            <b-col sm="4" class="mt-4">
                                <h5 class="text-white mb-0">Support</h5>
                                <div class="text-muted mt-3">
                                    <ul class="list-unstyled ff-secondary footer-list">
                                        <li>
                                            <b-link href="/pages/faqs">FAQ</b-link>
                                        </li>
                                        <li>
                                            <b-link href="/pages/faqs">Contact</b-link>
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
                            <p class="copy-rights mb-0">
                                {{ new Date().getFullYear() }} © Velzon - Themesbrand
                            </p>
                        </div>
                    </b-col>
                    <b-col sm="6">
                        <div class="text-sm-end mt-3 mt-sm-0">
                            <ul class="list-inline mb-0 footer-list gap-4 fs-13">
                                <li class="list-inline-item">
                                    <b-link href="/pages/privacy-policy">Privacy Policy</b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="/pages/term-conditions">Terms & Conditions</b-link>
                                </li>
                                <li class="list-inline-item">
                                    <b-link href="/pages/privacy-policy">Security</b-link>
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