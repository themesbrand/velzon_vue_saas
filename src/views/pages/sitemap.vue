<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Sitemap",
        meta: [{
            name: "description",
            content: appConfig.description
        }],
    },
    data() {
        return {
            title: "Sitemap",
            items: [{
                text: "Pages",
                href: "/",
            },
            {
                text: "Sitemap",
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
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title class="mb-0">Responsive Sitemap</b-card-title>
                    </b-card-header>
                    <b-card-body>
                        <div class="sitemap-content">
                            <figure class="sitemap-horizontal">
                                <ul class="administration">
                                    <li>
                                        <ul class="director">
                                            <li>
                                                <b-link href="javascript:void(0);" class="fw-semibold"><span>Velzon
                                                        Admin</span></b-link>
                                                <ul class="subdirector">
                                                    <li><b-link href="javascript:void(0);" class="fw-semibold"><span>Contact
                                                                Us</span></b-link></li>
                                                </ul>
                                                <ul class="departments">
                                                    <li><b-link href="javascript:void(0);" class="fw-semibold"><span>Main
                                                                Pages</span></b-link></li>

                                                    <li class="department">
                                                        <b-link href="javascript:void(0);" class="fw-semibold"><span>Account
                                                                Management</span></b-link>
                                                        <ul>
                                                            <li><b-link href="javascript:void(0);"><span>Sign Up</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Login</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Profile
                                                                        Settings</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Modify
                                                                        Reservation</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Cancel
                                                                        Reservation</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Write
                                                                        Reviews</span></b-link></li>
                                                        </ul>
                                                    </li>
                                                    <li class="department">
                                                        <b-link href="javascript:void(0);" class="fw-semibold"><span>About
                                                                Us</span></b-link>
                                                        <ul>
                                                            <li><b-link href="javascript:void(0);"><span>Overview</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Connect Via Social
                                                                        Media</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Careers</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Team
                                                                        Members</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Policies</span></b-link>
                                                            </li>
                                                        </ul>
                                                    </li>
                                                    <li class="department">
                                                        <b-link href="javascript:void(0);" class="fw-semibold"><span>Book a
                                                                Trip</span></b-link>
                                                        <ul>
                                                            <li><b-link href="javascript:void(0);"><span>Travel
                                                                        Details</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Reservation
                                                                        Process</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Payment
                                                                        Option</span></b-link></li>
                                                            <li><b-link
                                                                    href="javascript:void(0);"><span>Comfirmation</span></b-link>
                                                            </li>
                                                        </ul>
                                                    </li>
                                                    <li class="department">
                                                        <b-link href="javascript:void(0);"
                                                            class="fw-semibold"><span>Destination</span></b-link>
                                                        <ul>
                                                            <li><b-link
                                                                    href="javascript:void(0);"><span>Architecture</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Art</span></b-link></li>
                                                            <li><b-link
                                                                    href="javascript:void(0);"><span>Entertainment</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>History</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Science</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Sports</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Music</span></b-link>
                                                            </li>
                                                            <li><b-link href="javascript:void(0);"><span>Tracking
                                                                        Camp</span></b-link></li>
                                                        </ul>
                                                    </li>
                                                    <li class="department">
                                                        <b-link href="javascript:void(0);" class="fw-semibold"><span>Travel
                                                                Tips</span></b-link>
                                                        <ul>
                                                            <li><b-link href="javascript:void(0);"><span>General
                                                                        Travel</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Helpth
                                                                        Concerns</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>Safety
                                                                        Measures</span></b-link></li>
                                                            <li><b-link href="javascript:void(0);"><span>FAQ's</span></b-link>
                                                            </li>
                                                        </ul>
                                                    </li>
                                                </ul>
                                            </li>
                                        </ul>
                                    </li>
                                </ul>
                            </figure>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title class="mb-0">Horizontal</b-card-title>
                    </b-card-header>
                    <b-card-body>
                        <div class="hori-sitemap">
                            <ul class="list-unstyled mb-0">
                                <li class="p-0 parent-title"><b-link href="javascript: void(0);" class="fw-semibold fs-14">My
                                        Account</b-link></li>
                                <ul class="list-unstyled row g-0">
                                    <li class="col-sm-3">
                                        <b-link href="javascript: void(0);" class="fw-semibold sub-title">About Us</b-link>
                                        <ul class="list-unstyled row g-0 second-list">
                                            <li class="col-sm-6">
                                                <b-link href="javascript: void(0);">Overview</b-link>
                                            </li>
                                            <li class="col-sm-6">
                                                <b-link href="javascript: void(0);">History</b-link>
                                            </li>
                                        </ul>
                                    </li>
                                    <li class="col-sm-3">
                                        <b-link href="javascript: void(0);" class="fw-semibold">My self-care Plan</b-link>
                                        <ul class="list-unstyled second-list pt-0">
                                            <li>
                                                <div>
                                                    <b-link href="javascript: void(0);">Basic</b-link>
                                                    <b-link href="javascript: void(0);">Early Physiotherapy</b-link>
                                                    <b-link href="javascript: void(0);">Intermediate Physiotherapy</b-link>
                                                    <b-link href="javascript: void(0);">Return to Normal Activity</b-link>
                                                </div>
                                            </li>
                                        </ul>
                                    </li>
                                    <li class="col-sm-3">
                                        <b-link href="javascript: void(0);" class="fw-semibold sub-title">Support Us</b-link>
                                        <ul class="list-unstyled row g-0 sub-list">
                                            <li class="col-sm-6">
                                                <b-link href="javascript: void(0);">Contact Us</b-link>
                                            </li>
                                            <li class="col-sm-6">
                                                <b-link href="javascript: void(0);">Customer Services</b-link>
                                                <ul class="list-unstyled second-list">
                                                    <li>
                                                        <div>
                                                            <b-link href="javascript: void(0);">Chat With Us</b-link>
                                                            <b-link href="javascript: void(0);">Connect Information</b-link>
                                                            <b-link href="javascript: void(0);">FAQ'S</b-link>
                                                        </div>
                                                    </li>
                                                </ul>
                                            </li>
                                        </ul>
                                    </li>
                                    <li class="col-sm-3">
                                        <b-link href="javascript: void(0);" class="fw-semibold">Terms & Conditions</b-link>
                                    </li>
                                </ul>
                            </ul>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col lg="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title class="mb-0">Vertical</b-card-title>
                    </b-card-header>
                    <b-card-body>
                        <b-row>
                            <b-col sm="6">
                                <div class="verti-sitemap">
                                    <ul class="list-unstyled mb-0">
                                        <li class="p-0 parent-title"><b-link href="javascript: void(0);"
                                                class="fw-medium fs-14">Nancy Martino - Project Director</b-link>
                                        </li>
                                        <li>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary">Erica
                                                        Kernan - Team Leader</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li>
                                                        <b-link href="javascript: void(0);">Jason McQuaid -
                                                            Member</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link href="javascript: void(0);">Elwood Arter -
                                                            Member</b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary">Mary
                                                        Jones
                                                        - Project Manager</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li><b-link href="javascript: void(0);">Jordyn Jones -
                                                            Designer</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Ashlee Haney -
                                                            Developer</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Rashad Charles -
                                                            BackEnd Developer</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Walter Newman -
                                                            Frontend Developer</b-link>
                                                    </li>
                                                    <li><b-link href="javascript: void(0);">Adam Moss -
                                                            Designer</b-link></li>
                                                </ul>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary">Tilly
                                                        Kent
                                                        - Executive Manager</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li>
                                                        <b-link href="javascript: void(0);">Tyler Porter -
                                                            Account Executive</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link href="javascript: void(0);">Alicia Thompson -
                                                            Sales Executive</b-link>
                                                        <ul class="third-list list-unstyled">
                                                            <li><b-link href="javascript: void(0);">Jack
                                                                    Coates -
                                                                    Member</b-link></li>
                                                            <li><b-link href="javascript: void(0);">Owen
                                                                    Jarvis -
                                                                    Member</b-link></li>
                                                            <li><b-link href="javascript: void(0);">Ashlee
                                                                    Haney
                                                                    - Member</b-link></li>
                                                            <li><b-link href="javascript: void(0);">Archie
                                                                    Cook -
                                                                    Member</b-link></li>
                                                        </ul>
                                                    </li>
                                                </ul>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary">Rachel
                                                        Rose
                                                        - HR</b-link>
                                                </div>
                                            </div>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>

                            <b-col sm="6">
                                <div class="verti-sitemap">
                                    <ul class="list-unstyled mb-0">
                                        <li class="p-0 parent-title"><b-link href="javascript: void(0);"
                                                class="fw-medium fs-14">Velzon</b-link></li>
                                        <li>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary"><i
                                                            class="ri-airplay-line me-1 align-bottom"></i>
                                                        Dashboards</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li>
                                                        <b-link href="javascript: void(0);">Analytics</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link href="javascript: void(0);">CRM</b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary"><i
                                                            class="ri-pencil-ruler-2-line me-1 align-bottom"></i>
                                                        App Pages</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li><b-link href="javascript: void(0);">Calender</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Chat</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Email</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Ecommerce</b-link>
                                                    </li>
                                                    <li><b-link href="javascript: void(0);">Projects</b-link></li>
                                                    <li><b-link href="javascript: void(0);">Tasks</b-link></li>
                                                </ul>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary"><i
                                                            class="ri-file-list-3-line me-1 align-bottom"></i>
                                                        Pages</b-link>
                                                </div>
                                            </div>
                                            <div class="first-list">
                                                <div class="list-wrap">
                                                    <b-link href="javascript: void(0);" class="fw-medium text-primary"><i
                                                            class="ri-stack-line me-1 align-bottom"></i>
                                                        Components</b-link>
                                                </div>
                                                <ul class="second-list list-unstyled">
                                                    <li>
                                                        <b-link href="javascript: void(0);">Base UI</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link href="javascript: void(0);">Advance UI</b-link>
                                                        <ul class="third-list list-unstyled">
                                                            <li><b-link href="javascript: void(0);">Sweet
                                                                    Alerts</b-link></li>
                                                            <li><b-link href="javascript: void(0);">Range
                                                                    Slider</b-link></li>
                                                            <li><b-link href="javascript: void(0);">Nestable
                                                                    List</b-link></li>
                                                        </ul>
                                                    </li>
                                                </ul>
                                            </div>
                                        </li>
                                    </ul>
                                </div>
                            </b-col>
                        </b-row>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>