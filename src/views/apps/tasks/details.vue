<script>
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";

import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import animationData from "@/components/widgets/kbtmbyzy.json";
import Lottie from "@/components/widgets/lottie.vue";

export default {
    page: {
        title: "Tasks Details",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Tasks Details",
            items: [
                {
                    text: "Tasks",
                    href: "/",
                },
                {
                    text: "Tasks Details",
                    active: true,
                },
            ],
            modalShow: false,
            value: null,
            defaultOptions: { animationData: animationData },
        };
    },
    components: {
        Layout,
        PageHeader,
        lottie: Lottie,
        Multiselect
    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row>
            <b-col xxl="3">
                <b-card no-body>
                    <b-card-body class="text-center">
                        <h6 class="card-title mb-3 flex-grow-1 text-start">Time Tracking</h6>
                        <div class="mb-2">
                            <lottie colors="primary:#405189,secondary:#02a8b5" :options="defaultOptions" :height="90"
                                :width="90" />
                        </div>
                        <h3 class="mb-1">9 hrs 13 min</h3>
                        <h5 class="fs-14 mb-4">Profile Page Satructure</h5>
                        <div class="hstack gap-2 justify-content-center">
                            <b-button variant="danger" size="sm"><i class="ri-stop-circle-line align-bottom me-1"></i>
                                Stop</b-button>
                            <b-button variant="success" size="sm"><i class="ri-play-circle-line align-bottom me-1"></i>
                                Start</b-button>
                        </div>
                    </b-card-body>
                </b-card>
                <b-card no-body class="mb-3">
                    <b-card-body>
                        <div class="mb-4">
                            <Multiselect class="form-control" v-model="value" :close-on-select="true" :searchable="true"
                                :create-option="true" :options="[
                                    { value: '', label: 'Select Task board' },
                                    { value: 'Unassigned', label: 'Unassigned' },
                                    { value: 'To Do', label: 'To Do' },
                                    { value: 'Inprogress', label: 'Inprogress' },
                                    { value: 'In Reviews', label: 'In Reviews' },
                                    { value: 'Completed', label: 'Completed' }
                                ]" />
                        </div>
                        <div class="table-card">
                            <table class="table mb-0">
                                <tbody>
                                    <tr>
                                        <td class="fw-medium">Tasks No</td>
                                        <td>#VLZ456</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Tasks Title</td>
                                        <td>Profile Page Satructure</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Project Name</td>
                                        <td>Velzon - Admin Dashboard</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Priority</td>
                                        <td><b-badge variant="soft-danger" class="badge-soft-danger">High</b-badge></td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Status</td>
                                        <td><b-badge variant="soft-secondary" class="badge-soft-secondary">Inprogress</b-badge></td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Due Date</td>
                                        <td>05 Jan, 2022</td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </b-card-body>
                </b-card>
                <b-card no-body class="mb-3">
                    <b-card-body>
                        <div class="d-flex mb-3">
                            <h6 class="card-title mb-0 flex-grow-1">Assigned To</h6>
                            <div class="flex-shrink-0">
                                <b-button type="button" variant="soft-danger" size="sm" @click="modalShow = !modalShow">
                                    <i class="ri-share-line me-1 align-bottom"></i>
                                    Assigned Member
                                </b-button>
                            </div>
                        </div>
                        <ul class="list-unstyled vstack gap-3 mb-0">
                            <li>
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                            class="avatar-xs rounded-circle">
                                    </div>
                                    <div class="flex-grow-1 ms-2">
                                        <h6 class="mb-1">
                                            <router-link to="/pages/profile" class="text-body">Tonya Noble</router-link>
                                        </h6>
                                        <p class="text-muted mb-0">Full Stack Developer</p>
                                    </div>
                                    <div class="flex-shrink-0">
                                        <div class="dropdown">
                                            <button class="btn btn-icon btn-sm fs-16 text-muted dropdown" type="button"
                                                data-bs-toggle="dropdown" aria-expanded="false">
                                                <i class="ri-more-fill"></i>
                                            </button>
                                            <ul class="dropdown-menu">
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-eye-fill text-muted me-2 align-bottom"></i>View
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-star-fill text-muted me-2 align-bottom"></i>Favourite
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-delete-bin-5-fill text-muted me-2 align-bottom"></i>Delete
                                                    </b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                            class="avatar-xs rounded-circle">
                                    </div>
                                    <div class="flex-grow-1 ms-2">
                                        <h6 class="mb-1">
                                            <router-link to="/pages/profile" class="text-body">Thomas Taylor</router-link>
                                        </h6>
                                        <p class="text-muted mb-0">UI/UX Designer</p>
                                    </div>
                                    <div class="flex-shrink-0">
                                        <div class="dropdown">
                                            <button class="btn btn-icon btn-sm fs-16 text-muted dropdown" type="button"
                                                data-bs-toggle="dropdown" aria-expanded="false">
                                                <i class="ri-more-fill"></i>
                                            </button>
                                            <ul class="dropdown-menu">
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-eye-fill text-muted me-2 align-bottom"></i>View
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-star-fill text-muted me-2 align-bottom"></i>Favourite
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-delete-bin-5-fill text-muted me-2 align-bottom"></i>Delete
                                                    </b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                            class="avatar-xs rounded-circle">
                                    </div>
                                    <div class="flex-grow-1 ms-2">
                                        <h6 class="mb-1">
                                            <router-link to="/pages/profile" class="text-body">Nancy Martino</router-link>
                                        </h6>
                                        <p class="text-muted mb-0">Web Designer</p>
                                    </div>
                                    <div class="flex-shrink-0">
                                        <div class="dropdown">
                                            <button class="btn btn-icon btn-sm fs-16 text-muted dropdown" type="button"
                                                data-bs-toggle="dropdown" aria-expanded="false">
                                                <i class="ri-more-fill"></i>
                                            </button>
                                            <ul class="dropdown-menu">
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-eye-fill text-muted me-2 align-bottom"></i>View
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-star-fill text-muted me-2 align-bottom"></i>Favourite
                                                    </b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                            class="ri-delete-bin-5-fill text-muted me-2 align-bottom"></i>Delete
                                                    </b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </b-card-body>
                </b-card>
                <b-card no-body>
                    <b-card-body>
                        <h5 class="card-title mb-3">Attachments</h5>
                        <div class="vstack gap-2">
                            <div class="border rounded border-dashed p-2">
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-3">
                                        <div class="avatar-sm">
                                            <div class="avatar-title bg-light text-secondary rounded fs-24">
                                                <i class="ri-folder-zip-line"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1 overflow-hidden">
                                        <h5 class="fs-13 mb-1">
                                            <b-link href="javascript:void(0);" class="text-body text-truncate d-block">
                                                App pages.zip</b-link>
                                        </h5>
                                        <div class="text-muted">2.2MB</div>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                        <div class="d-flex gap-1">
                                            <button type="button" class="btn btn-icon text-muted btn-sm fs-18"><i
                                                    class="ri-download-2-line"></i></button>
                                            <div class="dropdown">
                                                <button class="btn btn-icon text-muted btn-sm fs-18 dropdown"
                                                    type="button" data-bs-toggle="dropdown" aria-expanded="false">
                                                    <i class="ri-more-fill"></i>
                                                </button>
                                                <ul class="dropdown-menu">
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-pencil-fill align-bottom me-2 text-muted"></i>
                                                            Rename</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-delete-bin-fill align-bottom me-2 text-muted"></i>
                                                            Delete</b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="border rounded border-dashed p-2">
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-3">
                                        <div class="avatar-sm">
                                            <div class="avatar-title bg-light text-secondary rounded fs-24">
                                                <i class="ri-file-ppt-2-line"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1 overflow-hidden">
                                        <h5 class="fs-13 mb-1">
                                            <b-link href="javascript:void(0);" class="text-body text-truncate d-block">
                                                Velzon admin.ppt</b-link>
                                        </h5>
                                        <div class="text-muted">2.4MB</div>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                        <div class="d-flex gap-1">
                                            <button type="button" class="btn btn-icon text-muted btn-sm fs-18"><i
                                                    class="ri-download-2-line"></i></button>
                                            <div class="dropdown">
                                                <button class="btn btn-icon text-muted btn-sm fs-18 dropdown"
                                                    type="button" data-bs-toggle="dropdown" aria-expanded="false">
                                                    <i class="ri-more-fill"></i>
                                                </button>
                                                <ul class="dropdown-menu">
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-pencil-fill align-bottom me-2 text-muted"></i>
                                                            Rename</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-delete-bin-fill align-bottom me-2 text-muted"></i>
                                                            Delete</b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>

                            <div class="border rounded border-dashed p-2">
                                <div class="d-flex align-items-center">
                                    <div class="flex-shrink-0 me-3">
                                        <div class="avatar-sm">
                                            <div class="avatar-title bg-light text-secondary rounded fs-24">
                                                <i class="ri-folder-zip-line"></i>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="flex-grow-1 overflow-hidden">
                                        <h5 class="fs-13 mb-1">
                                            <b-link href="javascript:void(0);" class="text-body text-truncate d-block">
                                                Images.zip</b-link>
                                        </h5>
                                        <div class="text-muted">1.2MB</div>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                        <div class="d-flex gap-1">
                                            <button type="button" class="btn btn-icon text-muted btn-sm fs-18"><i
                                                    class="ri-download-2-line"></i></button>
                                            <div class="dropdown">
                                                <button class="btn btn-icon text-muted btn-sm fs-18 dropdown"
                                                    type="button" data-bs-toggle="dropdown" aria-expanded="false">
                                                    <i class="ri-more-fill"></i>
                                                </button>
                                                <ul class="dropdown-menu">
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-pencil-fill align-bottom me-2 text-muted"></i>
                                                            Rename</b-link>
                                                    </li>
                                                    <li>
                                                        <b-link class="dropdown-item" href="javascript:void(0);"><i
                                                                class="ri-delete-bin-fill align-bottom me-2 text-muted"></i>
                                                            Delete</b-link>
                                                    </li>
                                                </ul>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="mt-2 text-center">
                                <b-button type="button" variant="success">View more</b-button>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xxl="9">
                <b-card no-body>
                    <b-card-body>
                        <div class="text-muted">
                            <h6 class="mb-3 text-uppercase">Summary</h6>
                            <p>It will be as simple as occidental in fact, it will be Occidental. To an English person,
                                it will seem like simplified English, as a skeptical Cambridge friend of mine told me
                                what Occidental is. The European languages are members of the same family. Their
                                separate existence is a myth. For science, music, sport, etc, Europe uses the same
                                vocabulary. The languages only differ in their grammar, their pronunciation and their
                                most common words.</p>

                            <h6 class="mb-3 text-uppercase">Sub-tasks</h6>
                            <ul class=" ps-3 list-unstyled vstack gap-2">
                                <li>
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" value="" id="productTask">
                                        <label class="form-check-label" for="productTask">
                                            Product Design, Figma (Software), Prototype
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" value="" id="dashboardTask"
                                            checked>
                                        <label class="form-check-label" for="dashboardTask">
                                            Dashboards : Ecommerce, Analytics, Project,etc.
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" value="" id="calenderTask">
                                        <label class="form-check-label" for="calenderTask">
                                            Create calendar, chat and email app pages
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" value=""
                                            id="authenticationTask">
                                        <label class="form-check-label" for="authenticationTask">
                                            Add authentication pages
                                        </label>
                                    </div>
                                </li>
                            </ul>

                            <div class="pt-3 border-top border-top-dashed mt-4">
                                <h6 class="mb-3 text-uppercase">Tasks Tags</h6>
                                <div class="hstack flex-wrap gap-2 fs-15">
                                    <b-badge variant="soft-info" tag="div" class="fw-medium badge-soft-info">UI/UX</b-badge>
                                    <b-badge variant="soft-info" tag="div" class="fw-medium badge-soft-info">Dashboard</b-badge>
                                    <b-badge variant="soft-info" tag="div" class="fw-medium badge-soft-info">Design</b-badge>
                                </div>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
                <b-card no-body>
                    <b-card-header>
                        <div>
                            <ul class="nav nav-tabs-custom rounded card-header-tabs border-bottom-0" role="tablist">
                                <li class="nav-item">
                                    <b-link class="nav-link text-body active" data-bs-toggle="tab" href="#home-1" role="tab">
                                        Comments (5)
                                    </b-link>
                                </li>
                                <li class="nav-item">
                                    <b-link class="nav-link text-body" data-bs-toggle="tab" href="#messages-1" role="tab">
                                        Attachments File (4)
                                    </b-link>
                                </li>
                                <li class="nav-item">
                                    <b-link class="nav-link text-body" data-bs-toggle="tab" href="#profile-1" role="tab">
                                        Time Entries (9 hrs 13 min)
                                    </b-link>
                                </li>
                            </ul>
                        </div>
                    </b-card-header>
                    <b-card-body>
                        <div class="tab-content">
                            <div class="tab-pane active" id="home-1" role="tabpanel">
                                <h5 class="card-title mb-4">Comments</h5>
                                <div data-simplebar style="height: 508px;" class="px-3 mx-n3 mb-2">
                                    <div class="d-flex mb-4">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">
                                                <router-link to="/pages/profile" class="text-body">Joseph Parker</router-link> <small
                                                    class="text-muted">20 Dec 2021 - 05:47AM</small>
                                            </h5>
                                            <p class="text-muted">I am getting message from customers that when they
                                                place order always get error message .</p>
                                            <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                                    class="mdi mdi-reply"></i> Reply</b-link>
                                            <div class="d-flex mt-4">
                                                <div class="flex-shrink-0">
                                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                        class="avatar-xs rounded-circle" />
                                                </div>
                                                <div class="flex-grow-1 ms-3">
                                                    <h5 class="fs-13">
                                                        <router-link to="/pages/profile" class="text-body">Tonya Noble</router-link> <small class="text-muted">22 Dec 2021 - 02:32PM</small>
                                                    </h5>
                                                    <p class="text-muted">Please be sure to check your Spam mailbox to
                                                        see if your email filters have identified the email from Dell as
                                                        spam.</p>
                                                    <b-link href="javascript: void(0);"
                                                        class="badge text-muted bg-light"><i class="mdi mdi-reply"></i>
                                                        Reply</b-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                    <div class="d-flex mb-4">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">
                                                <router-link to="/pages/profile" class="text-body">Thomas Taylor</router-link> <small
                                                    class="text-muted">24 Dec 2021 - 05:20PM</small>
                                            </h5>
                                            <p class="text-muted">If you have further questions, please contact Customer
                                                Support from the “Action Menu” on your <b-link
                                                    href="javascript:void(0);" class="text-decoration-underline">Online
                                                    Order Support</b-link>.</p>
                                            <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                                    class="mdi mdi-reply"></i> Reply</b-link>
                                        </div>
                                    </div>
                                    <div class="d-flex">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">
                                                <router-link to="/pages/profile" class="text-body">Tonya Noble</router-link> <small
                                                    class="text-muted">26 min ago</small>
                                            </h5>
                                            <p class="text-muted">Your <b-link href="javascript:void(0)"
                                                    class="text-decoration-underline">Online Order Support</b-link>
                                                provides
                                                you with the most current status of your order. To help manage your
                                                order refer to the “Action Menu” to initiate return, contact Customer
                                                Support and more.</p>
                                            <b-row class="g-2 mb-3">
                                                <b-col lg="1" sm="2" cols="6">
                                                    <img src="@/assets/images/small/img-4.jpg" alt=""
                                                        class="img-fluid rounded">
                                                </b-col>
                                                <b-col lg="1" sm="2" cols="6">
                                                    <img src="@/assets/images/small/img-5.jpg" alt=""
                                                        class="img-fluid rounded">
                                                </b-col>
                                            </b-row>
                                            <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                                    class="mdi mdi-reply"></i> Reply</b-link>
                                            <div class="d-flex mt-4">
                                                <div class="flex-shrink-0">
                                                    <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                                        class="avatar-xs rounded-circle" />
                                                </div>
                                                <div class="flex-grow-1 ms-3">
                                                    <h5 class="fs-13">
                                                        <router-link to="/pages/profile" class="text-body">Nancy Martino</router-link>
                                                        <small class="text-muted">8 sec ago</small>
                                                    </h5>
                                                    <p class="text-muted">Other shipping methods are available at
                                                        checkout if you want your purchase delivered faster.</p>
                                                    <b-link href="javascript: void(0);"
                                                        class="badge text-muted bg-light"><i class="mdi mdi-reply"></i>
                                                        Reply</b-link>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                                <form class="mt-4">
                                    <b-row class="g-3">
                                        <b-col lg="12">
                                            <label for="exampleFormControlTextarea1" class="form-label">Leave a
                                                Comments</label>
                                            <textarea class="form-control bg-light border-light"
                                                id="exampleFormControlTextarea1" rows="3"
                                                placeholder="Enter comments"></textarea>
                                        </b-col>
                                        <b-col cols="12" class="text-end">
                                            <b-button type="button" variant="ghost-secondary" class="btn-icon me-1"><i
                                                    class="ri-attachment-line fs-16"></i></b-button>
                                            <b-link href="javascript:void(0);" class="btn btn-success">Post Comments
                                            </b-link>
                                        </b-col>
                                    </b-row>
                                </form>
                            </div>
                            <div class="tab-pane" id="messages-1" role="tabpanel">
                                <div class="table-responsive table-card">
                                    <table class="table table-borderless align-middle mb-0">
                                        <thead class="table-light text-muted">
                                            <tr>
                                                <th scope="col">File Name</th>
                                                <th scope="col">Type</th>
                                                <th scope="col">Size</th>
                                                <th scope="col">Upload Date</th>
                                                <th scope="col">Action</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr>
                                                <td>
                                                    <div class="d-flex align-items-center">
                                                        <div class="avatar-sm">
                                                            <div
                                                                class="avatar-title bg-soft-primary text-primary rounded fs-20">
                                                                <i class="ri-file-zip-fill"></i>
                                                            </div>
                                                        </div>
                                                        <div class="ms-3 flex-grow-1">
                                                            <h6 class="fs-15 mb-0">
                                                                <b-link href="javascript:void(0)">App
                                                                    pages.zip</b-link>
                                                            </h6>
                                                        </div>
                                                    </div>
                                                </td>
                                                <td>Zip File</td>
                                                <td>2.22 MB</td>
                                                <td>21 Dec, 2021</td>
                                                <td>
                                                    <div class="dropdown">
                                                        <b-link href="javascript:void(0);"
                                                            class="btn btn-light btn-icon" id="dropdownMenuLink1"
                                                            data-bs-toggle="dropdown" aria-expanded="true">
                                                            <i class="ri-equalizer-fill"></i>
                                                        </b-link>
                                                        <ul class="dropdown-menu dropdown-menu-end"
                                                            aria-labelledby="dropdownMenuLink1"
                                                            data-popper-placement="bottom-end"
                                                            style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                                                </b-link>
                                                            </li>
                                                            <li class="dropdown-divider"></li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                                                </b-link>
                                                            </li>
                                                        </ul>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>
                                                    <div class="d-flex align-items-center">
                                                        <div class="avatar-sm">
                                                            <div
                                                                class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                                                <i class="ri-file-pdf-fill"></i>
                                                            </div>
                                                        </div>
                                                        <div class="ms-3 flex-grow-1">
                                                            <h6 class="fs-15 mb-0">
                                                                <b-link href="javascript:void(0);">Velzon
                                                                    admin.ppt</b-link>
                                                            </h6>
                                                        </div>
                                                    </div>
                                                </td>
                                                <td>PPT File</td>
                                                <td>2.24 MB</td>
                                                <td>25 Dec, 2021</td>
                                                <td>
                                                    <div class="dropdown">
                                                        <b-link href="javascript:void(0);"
                                                            class="btn btn-light btn-icon" id="dropdownMenuLink2"
                                                            data-bs-toggle="dropdown" aria-expanded="true">
                                                            <i class="ri-equalizer-fill"></i>
                                                        </b-link>
                                                        <ul class="dropdown-menu dropdown-menu-end"
                                                            aria-labelledby="dropdownMenuLink2"
                                                            data-popper-placement="bottom-end"
                                                            style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                                                </b-link>
                                                            </li>
                                                            <li class="dropdown-divider"></li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                                                </b-link>
                                                            </li>
                                                        </ul>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>
                                                    <div class="d-flex align-items-center">
                                                        <div class="avatar-sm">
                                                            <div
                                                                class="avatar-title bg-soft-info text-info rounded fs-20">
                                                                <i class="ri-folder-line"></i>
                                                            </div>
                                                        </div>
                                                        <div class="ms-3 flex-grow-1">
                                                            <h6 class="fs-15 mb-0">
                                                                <b-link href="javascript:void(0);">Images.zip</b-link>
                                                            </h6>
                                                        </div>
                                                    </div>
                                                </td>
                                                <td>ZIP File</td>
                                                <td>1.02 MB</td>
                                                <td>28 Dec, 2021</td>
                                                <td>
                                                    <div class="dropdown">
                                                        <b-link href="javascript:void(0);"
                                                            class="btn btn-light btn-icon" id="dropdownMenuLink3"
                                                            data-bs-toggle="dropdown" aria-expanded="true">
                                                            <i class="ri-equalizer-fill"></i>
                                                        </b-link>
                                                        <ul class="dropdown-menu dropdown-menu-end"
                                                            aria-labelledby="dropdownMenuLink3"
                                                            data-popper-placement="bottom-end"
                                                            style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-eye-fill me-2 align-middle"></i>View
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-download-2-fill me-2 align-middle"></i>Download
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-delete-bin-5-line me-2 align-middle"></i>Delete
                                                                </b-link>
                                                            </li>
                                                        </ul>
                                                    </div>
                                                </td>
                                            </tr>
                                            <tr>
                                                <td>
                                                    <div class="d-flex align-items-center">
                                                        <div class="avatar-sm">
                                                            <div
                                                                class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                                                <i class="ri-image-2-fill"></i>
                                                            </div>
                                                        </div>
                                                        <div class="ms-3 flex-grow-1">
                                                            <h6 class="fs-15 mb-0">
                                                                <b-link href="javascript:void(0);">Bg-pattern.png
                                                                </b-link>
                                                            </h6>
                                                        </div>
                                                    </div>
                                                </td>
                                                <td>PNG File</td>
                                                <td>879 KB</td>
                                                <td>02 Nov 2021</td>
                                                <td>
                                                    <div class="dropdown">
                                                        <b-link href="javascript:void(0);"
                                                            class="btn btn-light btn-icon" id="dropdownMenuLink4"
                                                            data-bs-toggle="dropdown" aria-expanded="true">
                                                            <i class="ri-equalizer-fill"></i>
                                                        </b-link>
                                                        <ul class="dropdown-menu dropdown-menu-end"
                                                            aria-labelledby="dropdownMenuLink4"
                                                            data-popper-placement="bottom-end"
                                                            style="position: absolute; inset: 0px 0px auto auto; margin: 0px; transform: translate(0px, 23px);">
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-eye-fill me-2 align-middle"></i>View
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-download-2-fill me-2 align-middle"></i>Download
                                                                </b-link>
                                                            </li>
                                                            <li>
                                                                <b-link class="dropdown-item"
                                                                    href="javascript:void(0);"><i
                                                                        class="ri-delete-bin-5-line me-2 align-middle"></i>Delete
                                                                </b-link>
                                                            </li>
                                                        </ul>
                                                    </div>
                                                </td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                            <div class="tab-pane" id="profile-1" role="tabpanel">
                                <h6 class="card-title mb-4 pb-2">Time Entries</h6>
                                <div class="table-responsive table-card">
                                    <table class="table align-middle mb-0">
                                        <thead class="table-light text-muted">
                                            <tr>
                                                <th scope="col">Member</th>
                                                <th scope="col">Date</th>
                                                <th scope="col">Duration</th>
                                                <th scope="col">Timer Idle</th>
                                                <th scope="col">Tasks Title</th>
                                            </tr>
                                        </thead>
                                        <tbody>
                                            <tr>
                                                <th scope="row">
                                                    <div class="d-flex align-items-center">
                                                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                                            class="rounded-circle avatar-xxs">
                                                        <div class="flex-grow-1 ms-2">
                                                            <router-link to="/pages/profile" class="fw-medium">Thomas
                                                                Taylor</router-link>
                                                        </div>
                                                    </div>
                                                </th>
                                                <td>02 Jan, 2022</td>
                                                <td>3 hrs 12 min</td>
                                                <td>05 min</td>
                                                <td>Apps Pages</td>
                                            </tr>
                                            <tr>
                                                <td>
                                                    <div class="d-flex align-items-center">
                                                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                            class="rounded-circle avatar-xxs">
                                                        <div class="flex-grow-1 ms-2">
                                                            <router-link to="/pages/profile" class="fw-medium">Tonya
                                                                Noble</router-link>
                                                        </div>
                                                    </div>
                                                </td>
                                                <td>28 Dec, 2021</td>
                                                <td>1 hrs 35 min</td>
                                                <td>-</td>
                                                <td>Profile Page Design</td>
                                            </tr>
                                            <tr>
                                                <th scope="row">
                                                    <div class="d-flex align-items-center">
                                                        <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                            class="rounded-circle avatar-xxs">
                                                        <div class="flex-grow-1 ms-2">
                                                            <router-link to="/pages/profile" class="fw-medium">Tonya
                                                                Noble</router-link>
                                                        </div>
                                                    </div>
                                                </th>
                                                <td>27 Dec, 2021</td>
                                                <td>4 hrs 26 min</td>
                                                <td>03 min</td>
                                                <td>Ecommerce Dashboard</td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                            </div>

                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>



        <b-modal v-model="modalShow" hide-footer title="Team Members" body-class="p-4" content-class="border-0"
            header-class="p-3 ps-4 bg-soft-success" class="v-modal-custom" centered>
            <div class="search-box mb-3">
                <input type="text" class="form-control bg-light border-light" placeholder="Search here...">
                <i class="ri-search-line search-icon"></i>
            </div>

            <div class="mb-4 d-flex align-items-center">
                <div class="me-2">
                    <h5 class="mb-0 fs-13">Members :</h5>
                </div>
                <div class="avatar-group justify-content-center">
                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover title="Tonya Noble">
                        <div class="avatar-xs">
                            <img src="@/assets/images/users/avatar-10.jpg" alt="" class="rounded-circle img-fluid">
                        </div>
                    </b-link>
                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                        title="Thomas Taylor">
                        <div class="avatar-xs">
                            <img src="@/assets/images/users/avatar-8.jpg" alt="" class="rounded-circle img-fluid">
                        </div>
                    </b-link>
                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                        title="Nancy Martino">
                        <div class="avatar-xs">
                            <img src="@/assets/images/users/avatar-2.jpg" alt="" class="rounded-circle img-fluid">
                        </div>
                    </b-link>
                </div>
            </div>
            <div class="mx-n4 px-4" data-simplebar style="max-height: 225px;">
                <div class="vstack gap-3">
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-2.jpg" alt="" class="img-fluid rounded-circle">
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Nancy Martino
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <div class="avatar-title bg-soft-danger text-danger rounded-circle">
                                HB
                            </div>
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Henry Baird
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-3.jpg" alt="" class="img-fluid rounded-circle">
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Frank Hook
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-4.jpg" alt="" class="img-fluid rounded-circle">
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Jennifer Carter
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <div class="avatar-title bg-soft-success text-success rounded-circle">
                                AC
                            </div>
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Alexis Clarke
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                    <div class="d-flex align-items-center">
                        <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-7.jpg" alt="" class="img-fluid rounded-circle">
                        </div>
                        <div class="flex-grow-1">
                            <h5 class="fs-13 mb-0">
                                <b-link href="javascript:void(0);" class="text-body d-block">Joseph Parker
                                </b-link>
                            </h5>
                        </div>
                        <div class="flex-shrink-0">
                            <b-button type="button" variant="light" size="sm">Add</b-button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="modal-footer v-modal-footer">
                <b-button type="button" variant="light" class="w-xs" @click="modalShow = false">
                    Cancel</b-button>
                <b-button type="button" variant="success" class="w-xs">Assigned</b-button>
            </div>
        </b-modal>
    </Layout>
</template>