<script>
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";
import flatPickr from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

export default {
    page: {
        title: "Deals",
        meta: [{
            name: "description",
            content: appConfig.description
        }],
    },
    components: {
        Layout,
        PageHeader,
        Multiselect,
        flatPickr
    },
    data() {
        return {
            title: "Deals",
            items: [{
                text: "CRM",
                href: "/",
            },
            {
                text: "Deals",
                active: true,
            },
            ],
            modalShow: false,
            value: null,
            date: null,
            timeConfig: {
                enableTime: false,
                dateFormat: "d M, Y",
            },
        };
    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-card no-body>
            <b-card-body>
                <b-row class="g-3">
                    <b-col md="3">
                        <div class="search-box">
                            <input type="text" class="form-control search" placeholder="Search for deals...">
                            <i class="ri-search-line search-icon"></i>
                        </div>
                    </b-col>
                    <b-col md="auto" class="ms-auto">
                        <div class="d-flex hastck gap-2 flex-wrap">
                            <div class="d-flex align-items-center gap-2">
                                <span class="text-muted flex-shrink-0">Sort by: </span>

                                <Multiselect class="form-control" style="width:130px;" v-model="value"
                                    :close-on-select="true" :searchable="true" :create-option="true" :options="[
                                        { value: 'Owner', label: 'Owner' },
                                        { value: 'Company', label: 'Company' },
                                        { value: 'Date', label: 'Date' },
                                    
                                    ]" />

                            </div>
                            <b-button variant="success" @click="modalShow = !modalShow">
                                <i class="ri-add-fill align-bottom me-1"></i> Add Deals
                            </b-button>
                            <div class="dropdown">
                                <button class="btn btn-soft-info btn-icon fs-14" type="button" id="dropdownMenuButton1"
                                    data-bs-toggle="dropdown" aria-expanded="false">
                                    <i class="ri-settings-4-line"></i>
                                </button>
                                <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                                    <li>
                                        <b-link class="dropdown-item" href="#">Copy</b-link>
                                    </li>
                                    <li>
                                        <b-link class="dropdown-item" href="#">Move to pipline</b-link>
                                    </li>
                                    <li>
                                        <b-link class="dropdown-item" href="#">Add to exceptions</b-link>
                                    </li>
                                    <li>
                                        <b-link class="dropdown-item" href="#">Switch to common form view</b-link>
                                    </li>
                                    <li>
                                        <b-link class="dropdown-item" href="#">Reset form view to default</b-link>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </b-col>
                </b-row>
            </b-card-body>
        </b-card>

        <b-row class="row-cols-xxl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
            <b-col>
                <b-card no-body>
                    <b-link class="card-header bg-soft-danger" role="button" v-b-toggle.leadDiscovered>
                        <h5 class="card-title text-uppercase mb-1 fs-14">Lead Discovered</h5>
                        <p class="text-muted mb-0">$265,200 <span class="fw-medium">4 Deals</span></p>
                    </b-link>
                </b-card>
                <b-collapse id="leadDiscovered" visible>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.leadDiscovered1>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-1.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Managing sales team meeting</h6>
                                    <p class="text-muted mb-0">$87k - 01 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="leadDiscovered1">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.leadDiscovered2>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Airbnb React Development</h6>
                                    <p class="text-muted mb-0">$20.3k - 24 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="leadDiscovered2">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.leadDiscovered3>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Discovery Capital</h6>
                                    <p class="text-muted mb-0">$124.3k - 29 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed show" id="leadDiscovered3" visible>
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.leadDiscovered4>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Airbnb React Development</h6>
                                    <p class="text-muted mb-0">$33.6k - 24 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="leadDiscovered4">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                </b-collapse>
            </b-col>

            <b-col>
                <b-card no-body>
                    <b-link class="card-header bg-soft-success" role="button" v-b-toggle.contactInitiated>
                        <h5 class="card-title text-uppercase mb-1 fs-14">Contact Initiated</h5>
                        <p class="text-muted mb-0">$108,700 <span class="fw-medium">5 Deals</span></p>
                    </b-link>
                </b-card>
                <b-collapse id="contactInitiated" visible>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.contactInitiated1>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Custom Mobile Apps</h6>
                                    <p class="text-muted mb-0">$28.7k - 13 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="contactInitiated1">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.contactInitiated2>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/brands/github.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Investment Deal for Zoetic Fashion</h6>
                                    <p class="text-muted mb-0">$32.8k - 10 Oct, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="contactInitiated2">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Zoetic Fashion <b-badge tag="small" variant="soft-warning" class="badge-soft-warning">25
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Today at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.contactInitiated3>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Modern Design</h6>
                                    <p class="text-muted mb-0">$23k - 03 Oct, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="contactInitiated3">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Micro Design <b-badge tag="small" variant="soft-success" class="badge-soft-success">2
                                        Month</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Today at 11:58AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.contactInitiated4>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Hotel Logo Design</h6>
                                    <p class="text-muted mb-0">$10.9k - 05 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="contactInitiated4">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.contactInitiated5>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/brands/mail_chimp.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Managing Sales</h6>
                                    <p class="text-muted mb-0">$13.3k - 04 Sep, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="contactInitiated5">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                </b-collapse>
            </b-col>

            <b-col>
                <b-card no-body>
                    <b-link class="card-header bg-soft-warning" role="button" v-b-toggle.needsIdentified>
                        <h5 class="card-title text-uppercase mb-1 fs-14">Needs Identified</h5>
                        <p class="text-muted mb-0">$708,200 <span class="fw-medium">7 Deals</span></p>
                    </b-link>
                </b-card>
                <b-collapse id="needsIdentified" visible>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified1>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-9.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Art Studio Design</h6>
                                    <p class="text-muted mb-0">$147.5k - 24 Sep, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified1">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Alexis Clarke <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">7
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Alexis</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified2>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Billing Page Bug</h6>
                                    <p class="text-muted mb-0">$15.8k - 17 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified2">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Meta4Systems <b-badge variant="soft-warning" class="badge-soft-warning">35
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Mary</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified3>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/brands/dribbble.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Food Selection Platform</h6>
                                    <p class="text-muted mb-0">$72.5k - 04 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified3">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Syntyce Solutions <b-badge variant="soft-danger" class="badge-soft-danger">15
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified4>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-1.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Skote React Development</h6>
                                    <p class="text-muted mb-0">$89.8 - 21 Nov, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified4">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Themesbrand <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">3
                                        Month</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified5>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Velzon - Admin Dashboard</h6>
                                    <p class="text-muted mb-0">$126.7k - 30 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified5">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Themesbrand <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">3 Days</b-badge>
                                </h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Nancy</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified6>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/companies/img-6.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Wood Elements Design</h6>
                                    <p class="text-muted mb-0">$120.2k - 24 Nov, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified6">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">iTest Factory <b-badge variant="soft-warning" tag="small" class="badge-soft-warning">42
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" v-b-toggle.needsIdentified7>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">PayPal SEO audit</h6>
                                    <p class="text-muted mb-0">$135.7k - 23 Nov, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="needsIdentified7">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Meta4Systems <b-badge tag="small" variant="soft-success" class="badge-soft-success">6
                                        Month</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                </b-collapse>
            </b-col>

            <b-col>
                <b-card no-body>
                    <b-link class="card-header bg-soft-info" role="button" v-b-toggle.meetingArranged>
                        <h5 class="card-title text-uppercase mb-1 fs-14">Meeting Arranged</h5>
                        <p class="text-muted mb-0">$44,900 <span class="fw-medium">3 Deals</span></p>
                    </b-link>
                </b-card>
                <b-collapse id="meetingArranged" visible>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.meetingArranged1>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/companies/img-5.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">SASS app workflow diagram</h6>
                                    <p class="text-muted mb-0">$17.8k - 01 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="meetingArranged1">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">10
                                        Days</b-badge ></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.meetingArranged2>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Uber new brand system</h6>
                                    <p class="text-muted mb-0">$24.5k - 22 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="meetingArranged2">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.meetingArranged3>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/companies/img-8.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">TripAdvisor</h6>
                                    <p class="text-muted mb-0">$2.6k - 12 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="meetingArranged3">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                </b-collapse>
            </b-col>

            <b-col>
                <b-card no-body>
                    <b-link class="card-header bg-soft-secondary" role="button" v-b-toggle.offerAccepted>
                        <h5 class="card-title text-uppercase mb-1 fs-14">Offer Accepted</h5>
                        <p class="text-muted mb-0">$819,300 <span class="fw-medium">8 Deals</span></p>
                    </b-link>
                </b-card>
                <b-collapse id="offerAccepted" visible>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted1>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Coupon Website</h6>
                                    <p class="text-muted mb-0">$27.4k - 07 Jan, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted1">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted2>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/brands/slack.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Marketing Automation Demo</h6>
                                    <p class="text-muted mb-0">$94.8 - 19 Nov, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted2">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-warning" class="badge-soft-warning">47
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted3>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">New Email Design Templates</h6>
                                    <p class="text-muted mb-0">$136.9k - 05 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted3">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted4>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Create New Components</h6>
                                    <p class="text-muted mb-0">$45.9k - 26 Dec, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted4">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-success" class="badge-soft-success">4
                                        Month</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted5>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/companies/img-3.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">New Test Tickets</h6>
                                    <p class="text-muted mb-0">$118k - 01 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted5">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1 ribbon-box ribbon-fill ribbon-sm">
                        <div class="ribbon ribbon-info"><i class="ri-flashlight-fill"></i></div>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted6>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Recover Deleted Folder</h6>
                                    <p class="text-muted mb-0">$87.3k - 03 Jan, 2022</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted6">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">14
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body class="mb-1">
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted7>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/brands/github.png" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Github SEO audit</h6>
                                    <p class="text-muted mb-0">$241.2k - 21 Sep, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted7">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                    <b-card no-body>
                        <b-card-body>
                            <b-link class="d-flex align-items-center" role="button" v-b-toggle.offerAccepted8>
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h6 class="fs-13 mb-1">Urban Modern Design</h6>
                                    <p class="text-muted mb-0">$67.8k - 09 Oct, 2021</p>
                                </div>
                            </b-link>
                        </b-card-body>
                        <b-collapse class="border-top border-top-dashed" id="offerAccepted8">
                            <b-card-body>
                                <h6 class="fs-13 mb-1">Nesta Technologies <b-badge tag="small" variant="soft-danger" class="badge-soft-danger">4
                                        Days</b-badge></h6>
                                <p class="text-muted">As a company grows however, you find it's not as easy to shout
                                    across</p>
                                <ul class="list-unstyled vstack gap-2 mb-0">
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-question-answer-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Meeting with Thomas</h6>
                                                <small class="text-muted">Yesterday at 9:12AM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-mac-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Product Demo</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                    <li>
                                        <div class="d-flex">
                                            <div class="flex-shrink-0 avatar-xxs text-muted">
                                                <i class="ri-earth-line"></i>
                                            </div>
                                            <div class="flex-grow-1">
                                                <h6 class="mb-0">Marketing Team Meeting</h6>
                                                <small class="text-muted">Monday at 04:41PM</small>
                                            </div>
                                        </div>
                                    </li>
                                </ul>
                            </b-card-body>
                            <b-card-footer class="hstack gap-2">
                                <b-button variant="warning" size="sm" class="w-100"><i
                                        class="ri-phone-line align-bottom me-1"></i> Call</b-button>
                                <b-button variant="info" size="sm" class="w-100"><i
                                        class="ri-question-answer-line align-bottom me-1"></i> Message</b-button>
                            </b-card-footer>
                        </b-collapse>
                    </b-card>
                </b-collapse>
            </b-col>
        </b-row>

            <!-- <b-modal v-model="modalShow" body-class="p-0" header-class="bg-light p-3" hide-footer title="Create Deals"
                class="v-modal-custom" centered>
                <form>
                    <div class="modal-body">
                        <div class="mb-3">
                            <label for="dealTitle" class="form-label">Deal Title</label>
                            <input type="email" class="form-control" id="dealTitle" placeholder="Enter title">
                        </div>
                        <div class="mb-3">
                            <label for="dealValue" class="form-label">Value (USD)</label>
                            <input type="text" class="form-control" id="dealValue" placeholder="Enter value">
                        </div>
                        <div class="mb-3">
                            <label for="dealOwner" class="form-label">Deals Owner</label>
                            <input type="text" class="form-control" id="dealOwner" placeholder="Enter owner name">
                        </div>
                        <div class="mb-3">
                            <label for="dueDate" class="form-label">Due Date</label>
                            <flat-pickr placeholder="Select date" v-model="date" :config="timeConfig"
                                class="form-control flatpickr-input" id="adddate"></flat-pickr>
                        </div>
                        <div class="mb-3">
                            <label for="contactNumber" class="form-label">Contact</label>
                            <input type="text" class="form-control" id="contactNumber" placeholder="Enter contact number">
                        </div>
                        <div class="mb-3">
                            <label for="contactNumber" class="form-label">Description</label>
                            <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"
                                placeholder="Enter description"></textarea>
                        </div>
                    </div>
                    <div class="modal-footer">
                        <b-button type="button" variant="light" @click="modalShow = false">Close
                        </b-button>
                        <b-button type="button" variant="success"><i class="ri-save-line align-bottom me-1"></i> Save
                        </b-button>
                    </div>
                </b-form>
            </b-modal> -->

        <b-modal v-model="modalShow" body-class="" header-class="bg-light p-3" hide-footer title="Create Deals"
            class="v-modal-custom" centered>
            <b-form class="needs-validation" novalidate id="deals-form" onsubmit="return false">
                <div class="mb-3">
                    <label for="deatType" class="form-label">Deals Type</label>
                    <select class="form-select" id="deatType" data-choices aria-label="Default select example" required>
                        <option value="" data-custom-properties="[object Object]">Select deals type</option>
                        <option value="Lead Disovered">Lead Disovered</option>
                        <option value="Contact Initiated">Contact Initiated</option>
                        <option value="Need Identified">Need Identified</option>
                        <option value="Meeting Arranged">Meeting Arranged</option>
                        <option value="Offer Accepted">Offer Accepted</option>
                    </select>
                    <div class="invalid-feedback">
                        Please write an deals owner name.
                    </div>
                </div>
                <div class="mb-3">
                    <label for="dealTitle" class="form-label">Deal Title</label>
                    <input type="text" class="form-control" id="dealTitle" placeholder="Enter title" required>
                    <div class="invalid-feedback">
                        Please write a title.
                    </div>
                </div>
                <div class="mb-3">
                    <label for="dealValue" class="form-label">Value (USD)</label>
                    <input type="number" class="form-control" id="dealValue" step="0.01" placeholder="Enter value"
                        required>
                    <div class="invalid-feedback">
                        Please write a value.
                    </div>
                </div>

                <div class="mb-3">
                    <label for="dealOwner" class="form-label">Deals Owner</label>
                    <input type="text" class="form-control" id="dealOwner" required placeholder="Enter owner name">
                    <div class="invalid-feedback">
                        Please write an deals owner name.
                    </div>
                </div>
                <div class="mb-3">
                    <label for="dueDate" class="form-label">Due Date</label>
                    <flat-pickr placeholder="Select date" v-model="date" :config="timeConfig"
                            class="form-control flatpickr-input" id="adddate"></flat-pickr>
                    <div class="invalid-feedback">
                        Please select a due date.
                    </div>
                </div>

                <div class="mb-3">
                    <label for="dealEmail" class="form-label">Email</label>
                    <input type="email" class="form-control" id="dealEmail" placeholder="Enter email" required>
                    <div class="invalid-feedback">
                        Please write a email.
                    </div>
                </div>

                <div class="mb-3">
                    <label for="contactNumber" class="form-label">Contact</label>
                    <input type="text" class="form-control" id="contactNumber" placeholder="Enter contact number"
                        required>
                    <div class="invalid-feedback">
                        Please add a contact.
                    </div>
                </div>
                <div class="mb-3">
                    <label for="contactDescription" class="form-label">Description</label>
                    <textarea class="form-control" id="contactDescription" rows="3" placeholder="Enter description"
                        required></textarea>
                    <div class="invalid-feedback">
                        Please add a description.
                    </div>
                </div>
                <div class="modal-footer v-modal-footer">
                    <b-button type="button" variant="light" id="close-modal" @click="modalShow = false"> Close </b-button>
                    <b-button type="submit" variant="success"><i class="ri-save-line align-bottom me-1"></i> Save </b-button>
                </div>
            </b-form>
        </b-modal>
    </Layout>
</template>