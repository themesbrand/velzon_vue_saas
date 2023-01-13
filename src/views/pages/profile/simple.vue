<script>
import SwiperCore, { Thumbs, Navigation, Pagination } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";

SwiperCore.use([Thumbs, Navigation, Pagination]);

import Layout from "../../../layouts/main.vue";
import appConfig from "../../../../app.config";

export default {
  page: {
    title: "Profile",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Profile",
      items: [
        {
          text: "Velzon",
          href: "/",
        },
        {
          text: "Profile",
          active: true,
        },
      ],
      thumbsSwiper: null,
    };
  },
  components: {
    Layout,
    Swiper,
    SwiperSlide,
  },
};
</script>

<template>
  <Layout>
    <div class="profile-foreground position-relative mx-n4 mt-n4">
      <div class="profile-wid-bg">
        <img src="@/assets/images/profile-bg.jpg" alt="" class="profile-wid-img" />
      </div>
    </div>
    <div class="pt-4 mb-4 mb-lg-3 pb-lg-4">
      <b-row class="g-4">
        <b-col cols="auto">
          <div class="avatar-lg">
            <img src="@/assets/images/users/avatar-1.jpg" alt="user-img" class="img-thumbnail rounded-circle" />
          </div>
        </b-col>
        <b-col>
          <div class="p-2">
            <h3 class="text-white mb-1">Anna Adame</h3>
            <p class="text-white-75">Owner & Founder</p>
            <div class="hstack text-white-50 gap-1">
              <div class="me-2">
                <i class="ri-map-pin-user-line me-1 text-white-75 fs-16 align-middle"></i>California, United States
              </div>
              <div>
                <i class="ri-building-line me-1 text-white-75 fs-16 align-middle"></i>Themesbrand
              </div>
            </div>
          </div>
        </b-col>
        <b-col cols="12" lg="auto" order-lg="0" class="order-last">
          <b-row class="text text-white-50 text-center">
            <b-col lg="6" cols="4">
              <div class="p-2">
                <h4 class="text-white mb-1">24.3K</h4>
                <p class="fs-14 mb-0">Followers</p>
              </div>
            </b-col>
            <b-col lg="6" cols="4">
              <div class="p-2">
                <h4 class="text-white mb-1">1.3K</h4>
                <p class="fs-14 mb-0">Following</p>
              </div>
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </div>

    <b-row>
      <b-col lg="12">
        <div>
          <div class="d-flex">
            <ul class="nav nav-pills animation-nav profile-nav gap-2 gap-lg-3 flex-grow-1" role="tablist">
              <li class="nav-item">
                <b-link class="nav-link fs-14 active" data-bs-toggle="tab" href="#overview-tab" role="tab">
                  <i class="ri-airplay-fill d-inline-block d-md-none"></i>
                  <span class="d-none d-md-inline-block">Overview</span>
                </b-link>
              </li>
              <li class="nav-item">
                <b-link class="nav-link fs-14" data-bs-toggle="tab" href="#activities" role="tab">
                  <i class="ri-list-unordered d-inline-block d-md-none"></i>
                  <span class="d-none d-md-inline-block">Activities</span>
                </b-link>
              </li>
              <li class="nav-item">
                <b-link class="nav-link fs-14" data-bs-toggle="tab" href="#projects" role="tab">
                  <i class="ri-price-tag-line d-inline-block d-md-none"></i>
                  <span class="d-none d-md-inline-block">Projects</span>
                </b-link>
              </li>
              <li class="nav-item">
                <b-link class="nav-link fs-14" data-bs-toggle="tab" href="#documents" role="tab">
                  <i class="ri-folder-4-line d-inline-block d-md-none"></i>
                  <span class="d-none d-md-inline-block">Documents</span>
                </b-link>
              </li>
            </ul>
            <div class="flex-shrink-0">
              <router-link to="/pages/profile-setting" class="btn btn-success"><i
                  class="ri-edit-box-line align-bottom"></i> Edit Profile</router-link>
            </div>
          </div>
          <div class="tab-content pt-4 text-muted">
            <div class="tab-pane active" id="overview-tab" role="tabpanel">
              <b-row>
                <b-col xxl="3">
                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-5">Complete Your Profile</h5>
                      <b-progress class="animated-progress custom-progress progress-label">
                        <b-progress-bar :value="30" variant="danger">
                          <div class="label">30%</div>
                        </b-progress-bar>
                      </b-progress>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-3">Info</h5>
                      <div class="table-responsive">
                        <table class="table table-borderless mb-0">
                          <tbody>
                            <tr>
                              <th class="ps-0" scope="row">Full Name :</th>
                              <td class="text-muted">Anna Adame</td>
                            </tr>
                            <tr>
                              <th class="ps-0" scope="row">Mobile :</th>
                              <td class="text-muted">+(1) 987 6543</td>
                            </tr>
                            <tr>
                              <th class="ps-0" scope="row">E-mail :</th>
                              <td class="text-muted">daveadame@velzon.com</td>
                            </tr>
                            <tr>
                              <th class="ps-0" scope="row">Location :</th>
                              <td class="text-muted">
                                California, United States
                              </td>
                            </tr>
                            <tr>
                              <th class="ps-0" scope="row">Joining Date</th>
                              <td class="text-muted">24 Nov 2021</td>
                            </tr>
                          </tbody>
                        </table>
                      </div>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-4">Portfolio</h5>
                      <div class="d-flex flex-wrap gap-2">
                        <div>
                          <b-link href="javascript:void(0);" class="avatar-xs d-block">
                            <span class="avatar-title rounded-circle fs-16 bg-dark text-light">
                              <i class="ri-github-fill"></i>
                            </span>
                          </b-link>
                        </div>
                        <div>
                          <b-link href="javascript:void(0);" class="avatar-xs d-block">
                            <span class="avatar-title rounded-circle fs-16 bg-primary">
                              <i class="ri-global-fill"></i>
                            </span>
                          </b-link>
                        </div>
                        <div>
                          <b-link href="javascript:void(0);" class="avatar-xs d-block">
                            <span class="avatar-title rounded-circle fs-16 bg-success">
                              <i class="ri-dribbble-fill"></i>
                            </span>
                          </b-link>
                        </div>
                        <div>
                          <b-link href="javascript:void(0);" class="avatar-xs d-block">
                            <span class="avatar-title rounded-circle fs-16 bg-danger">
                              <i class="ri-pinterest-fill"></i>
                            </span>
                          </b-link>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-4">Skills</h5>
                      <div class="d-flex flex-wrap gap-2 fs-15">
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">Photoshop</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">illustrator</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">HTML</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">CSS</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">Javascript</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">Php</b-link>
                        <b-link href="javascript:void(0);" class="badge badge-soft-primary">Python</b-link>
                      </div>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <div class="d-flex align-items-center mb-4">
                        <div class="flex-grow-1">
                          <h5 class="card-title mb-0">Suggestions</h5>
                        </div>
                        <div class="flex-shrink-0">
                          <b-dropdown variant="link" right toggle-class="arrow-none p-0" no-caret>
                            <template #button-content><i class="ri-more-2-fill fs-14"></i>
                            </template>
                            <b-dropdown-item href="#">
                              View
                            </b-dropdown-item>
                            <b-dropdown-item href="#">
                              Download
                            </b-dropdown-item>
                            <b-dropdown-item href="#">
                              Delete
                            </b-dropdown-item>
                          </b-dropdown>
                        </div>
                      </div>
                      <div>
                        <div class="d-flex align-items-center py-3">
                          <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-3.jpg" alt="" class="img-fluid rounded-circle" />
                          </div>
                          <div class="flex-grow-1">
                            <div>
                              <h5 class="fs-13 mb-1">Esther James</h5>
                              <p class="fs-13 text-muted mb-0">
                                Frontend Developer
                              </p>
                            </div>
                          </div>
                          <div class="flex-shrink-0 ms-2">
                            <b-button type="button" variant="outline-success" size="sm">
                              <i class="ri-user-add-line align-middle"></i>
                            </b-button>
                          </div>
                        </div>
                        <div class="d-flex align-items-center py-3">
                          <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-4.jpg" alt="" class="img-fluid rounded-circle" />
                          </div>
                          <div class="flex-grow-1">
                            <div>
                              <h5 class="fs-13 mb-1">Jacqueline Steve</h5>
                              <p class="fs-13 text-muted mb-0">
                                UI/UX Designer
                              </p>
                            </div>
                          </div>
                          <div class="flex-shrink-0 ms-2">
                            <b-button type="button" variant="outline-success" size="sm">
                              <i class="ri-user-add-line align-middle"></i>
                            </b-button>
                          </div>
                        </div>
                        <div class="d-flex align-items-center py-3">
                          <div class="avatar-xs flex-shrink-0 me-3">
                            <img src="@/assets/images/users/avatar-5.jpg" alt="" class="img-fluid rounded-circle" />
                          </div>
                          <div class="flex-grow-1">
                            <div>
                              <h5 class="fs-13 mb-1">George Whalen</h5>
                              <p class="fs-13 text-muted mb-0">
                                Backend Developer
                              </p>
                            </div>
                          </div>
                          <div class="flex-shrink-0 ms-2">
                            <b-button type="button" variant="outline-success" size="sm">
                              <i class="ri-user-add-line align-middle"></i>
                            </b-button>
                          </div>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>

                  <b-card no-body>
                    <b-card-body>
                      <div class="d-flex align-items-center mb-4">
                        <div class="flex-grow-1">
                          <h5 class="card-title mb-0">Popular Posts</h5>
                        </div>
                        <div class="flex-shrink-0">
                          <b-dropdown variant="link" right toggle-class="arrow-none p-0" no-caret>
                            <template #button-content><i class="ri-more-2-fill fs-14"></i>
                            </template>
                            <b-dropdown-item href="#">
                              View
                            </b-dropdown-item>
                            <b-dropdown-item href="#">
                              Download
                            </b-dropdown-item>
                            <b-dropdown-item href="#">
                              Delete
                            </b-dropdown-item>
                          </b-dropdown>
                        </div>
                      </div>
                      <div class="d-flex mb-4">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/small/img-4.jpg" alt="" height="50" class="rounded" />
                        </div>
                        <div class="flex-grow-1 ms-3 overflow-hidden">
                          <b-link href="javascript:void(0);">
                            <h6 class="text-truncate fs-13">
                              Design your apps in your own way
                            </h6>
                          </b-link>
                          <p class="text-muted mb-0">15 Dec 2021</p>
                        </div>
                      </div>
                      <div class="d-flex mb-4">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/small/img-5.jpg" alt="" height="50" class="rounded" />
                        </div>
                        <div class="flex-grow-1 ms-3 overflow-hidden">
                          <b-link href="javascript:void(0);">
                            <h6 class="text-truncate fs-13">
                              Smartest Applications for Business
                            </h6>
                          </b-link>
                          <p class="text-muted mb-0">28 Nov 2021</p>
                        </div>
                      </div>
                      <div class="d-flex">
                        <div class="flex-shrink-0">
                          <img src="@/assets/images/small/img-6.jpg" alt="" height="50" class="rounded" />
                        </div>
                        <div class="flex-grow-1 ms-3 overflow-hidden">
                          <b-link href="javascript:void(0);">
                            <h6 class="text-truncate fs-13">
                              How to get creative in your work
                            </h6>
                          </b-link>
                          <p class="text-muted mb-0">21 Nov 2021</p>
                        </div>
                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
                <b-col xxl="9">
                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-3">About</h5>
                      <p>
                        Hi I'm Anna Adame, It will be as simple as Occidental;
                        in fact, it will be Occidental. To an English person, it
                        will seem like simplified English, as a skeptical
                        Cambridge friend of mine told me what Occidental is
                        European languages are members of the same family.
                      </p>
                      <p>
                        You always want to make sure that your fonts work well
                        together and try to limit the number of fonts you use to
                        three or less. Experiment and play around with the fonts
                        that you already have in the software you’re working
                        with reputable font websites. This may be the most
                        commonly encountered tip I received from the designers I
                        spoke with. They highly encourage that you use different
                        fonts in one design, but do not over-exaggerate and go
                        overboard.
                      </p>
                      <b-row>
                        <b-col cols="6" md="4">
                          <div class="d-flex mt-4">
                            <div class="flex-shrink-0 avatar-xs align-self-center me-3">
                              <div class="avatar-title bg-light rounded-circle fs-16 text-primary">
                                <i class="ri-user-2-fill"></i>
                              </div>
                            </div>
                            <div class="flex-grow-1 overflow-hidden">
                              <p class="mb-1">Designation :</p>
                              <h6 class="text-truncate mb-0">
                                Lead Designer / Developer
                              </h6>
                            </div>
                          </div>
                        </b-col>
                        <b-col cols="6" md="4">
                          <div class="d-flex mt-4">
                            <div class="flex-shrink-0 avatar-xs align-self-center me-3">
                              <div class="avatar-title bg-light rounded-circle fs-16 text-primary">
                                <i class="ri-global-line"></i>
                              </div>
                            </div>
                            <div class="flex-grow-1 overflow-hidden">
                              <p class="mb-1">Website :</p>
                              <b-link href="#" class="fw-semibold">www.velzon.com</b-link>
                            </div>
                          </div>
                        </b-col>
                      </b-row>
                    </b-card-body>
                  </b-card>

                  <b-row>
                    <b-col lg="12">
                      <b-card no-body>
                        <b-card-header class="align-items-center d-flex">
                          <b-card-title class="mb-0 me-2">Recent Activity</b-card-title>
                          <div class="flex-shrink-0 ms-auto">
                            <ul class="nav justify-content-end nav-tabs-custom rounded card-header-tabs border-bottom-0"
                              role="tablist">
                              <li class="nav-item">
                                <b-link class="nav-link active" data-bs-toggle="tab" href="#today" role="tab">
                                  Today
                                </b-link>
                              </li>
                              <li class="nav-item">
                                <b-link class="nav-link" data-bs-toggle="tab" href="#weekly" role="tab">
                                  Weekly
                                </b-link>
                              </li>
                              <li class="nav-item">
                                <b-link class="nav-link" data-bs-toggle="tab" href="#monthly" role="tab">
                                  Monthly
                                </b-link>
                              </li>
                            </ul>
                          </div>
                        </b-card-header>
                        <b-card-body>
                          <div class="tab-content text-muted">
                            <div class="tab-pane active" id="today" role="tabpanel">
                              <div class="profile-timeline">
                                <div class="accordion accordion-flush" id="todayExample">
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="headingOne">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapseOne>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Jacqueline Steve
                                            </h6>
                                            <small class="text-muted">We has changed 2 attributes on
                                              05:16PM</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapseOne" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        In an awareness campaign, it is vital
                                        for people to begin put 2 and 2 together
                                        and begin to recognize your cause. Too
                                        much or too little spacing, as in the
                                        example below, can make things
                                        unpleasant for the reader. The goal is
                                        to make your text as comfortable to read
                                        as possible. A wonderful serenity has
                                        taken possession of my entire soul, like
                                        these sweet mornings of spring which I
                                        enjoy with my whole heart.
                                      </div>
                                    </b-collapse>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="headingTwo">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapseTwo>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0 avatar-xs">
                                            <div class="avatar-title bg-light text-success rounded-circle">
                                              M
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Megan Elmore
                                            </h6>
                                            <small class="text-muted">Adding a new event with
                                              attachments - 04:45PM</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                    <b-collapse id="collapseTwo" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        <b-row class="g-2">
                                          <b-col cols="auto">
                                            <div class="d-flex border border-dashed p-2 rounded position-relative">
                                              <div class="flex-shrink-0">
                                                <i class="ri-image-2-line fs-17 text-danger"></i>
                                              </div>
                                              <div class="flex-grow-1 ms-2">
                                                <h6>
                                                  <b-link href="javascript:void(0);" class="stretched-link">Business
                                                    Template
                                                    - UI/UX
                                                    design</b-link>
                                                </h6>
                                                <small>685 KB</small>
                                              </div>
                                            </div>
                                          </b-col>
                                          <b-col cols="auto">
                                            <div class="d-flex border border-dashed p-2 rounded position-relative">
                                              <div class="flex-shrink-0">
                                                <i class="ri-file-zip-line fs-17 text-info"></i>
                                              </div>
                                              <div class="flex-grow-1 ms-2">
                                                <h6>
                                                  <b-link href="javascript:void(0);" class="stretched-link">Bank
                                                    Management
                                                    System -
                                                    PSD</b-link>
                                                </h6>
                                                <small>8.78 MB</small>
                                              </div>
                                            </div>
                                          </b-col>
                                        </b-row>
                                      </div>
                                    </b-collapse>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="headingThree">
                                      <b-link class="accordion-button p-2 shadow-none" data-bs-toggle="collapse"
                                        href="#collapsethree" aria-expanded="false">
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              New ticket received
                                            </h6>
                                            <small class="text-muted mb-2">User
                                              <span class="text-secondary">Erica245</span>
                                              submitted a ticket -
                                              02:33PM</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="headingFour">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapseFour>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0 avatar-xs">
                                            <div class="avatar-title bg-light text-muted rounded-circle">
                                              <i class="ri-user-3-fill"></i>
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Nancy Martino
                                            </h6>
                                            <small class="text-muted">Commented on 12:57PM</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                    <b-collapse id="collapseFour" visible>
                                      <div class="accordion-body ms-2 ps-5 fst-italic">
                                        " A wonderful serenity has taken
                                        possession of my entire soul, like these
                                        sweet mornings of spring which I enjoy
                                        with my whole heart. Each design is a
                                        new, unique piece of art birthed into
                                        this world, and while you have the
                                        opportunity to be creative and make your
                                        own style choices. "
                                      </div>
                                    </b-collapse>

                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="headingFive">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapseFive>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Lewis Arnold
                                            </h6>
                                            <small class="text-muted">Create new project buildng
                                              product - 10:05AM</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapseFive" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        <p class="text-muted mb-2">
                                          Every team project can have a velzon.
                                          Use the velzon to share information
                                          with your team to understand and
                                          contribute to your project.
                                        </p>
                                        <div class="avatar-group">
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="Christi">
                                            <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                              class="rounded-circle avatar-xs" />
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="Frank Hook">
                                            <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                              class="rounded-circle avatar-xs" />
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="Ruby">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle bg-light text-primary">
                                                R
                                              </div>
                                            </div>
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="more">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle">
                                                2+
                                              </div>
                                            </div>
                                          </b-link>
                                        </div>
                                      </div>
                                    </b-collapse>
                                  </div>
                                </div>
                              </div>
                            </div>
                            <div class="tab-pane" id="weekly" role="tabpanel">
                              <div class="profile-timeline">
                                <div class="accordion accordion-flush" id="weeklyExample">
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading6">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse6>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Joseph Parker
                                            </h6>
                                            <small class="text-muted">New people joined with our
                                              company - Yesterday</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                    <b-collapse id="collapse6" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        It makes a statement, it’s impressive
                                        graphic design. Increase or decrease the
                                        letter spacing depending on the
                                        situation and try, try again until it
                                        looks right, and each letter has the
                                        perfect spot of its own.
                                      </div>
                                    </b-collapse>

                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading7">
                                      <b-link class="accordion-button p-2 shadow-none" data-bs-toggle="collapse"
                                        href="#collapse7" aria-expanded="false">
                                        <div class="d-flex">
                                          <div class="avatar-xs">
                                            <div class="avatar-title rounded-circle bg-light text-danger">
                                              <i class="ri-shopping-bag-line"></i>
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Your order is placed
                                              <b-badge variant="soft-success"
                                                class="bg-soft-success text-success align-middle">Completed</b-badge>
                                            </h6>
                                            <small class="text-muted">These customers can rest assured
                                              their order has been placed - 1
                                              week Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading8">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse8>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0 avatar-xs">
                                            <div class="avatar-title bg-light text-success rounded-circle">
                                              <i class="ri-home-3-line"></i>
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Velzon admin dashboard templates
                                              layout upload
                                            </h6>
                                            <small class="text-muted">We talked about a project on
                                              linkedin - 1 week Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapse8" visible>
                                      <div class="accordion-body ms-2 ps-5 fst-italic">
                                        Powerful, clean & modern responsive
                                        bootstrap 5 admin template. The maximum
                                        file size for uploads in this demo :
                                        <b-row class="mt-2">
                                          <b-col xxl="6">
                                            <b-row class="border border-dashed gx-2 p-2">
                                              <b-col cols="3">
                                                <img src="@/assets/images/small/img-3.jpg" alt=""
                                                  class="img-fluid rounded" />
                                              </b-col>
                                              <b-col cols="3">
                                                <img src="@/assets/images/small/img-5.jpg" alt=""
                                                  class="img-fluid rounded" />
                                              </b-col>
                                              <b-col cols="3">
                                                <img src="@/assets/images/small/img-7.jpg" alt=""
                                                  class="img-fluid rounded" />
                                              </b-col>
                                              <b-col cols="3">
                                                <img src="@/assets/images/small/img-9.jpg" alt=""
                                                  class="img-fluid rounded" />
                                              </b-col>
                                            </b-row>
                                          </b-col>
                                        </b-row>
                                      </div>
                                    </b-collapse>

                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading9">
                                      <b-link class="accordion-button p-2 shadow-none">
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              New ticket created
                                              <b-badge class="bg-soft-info text-info align-middle">Inprogress</b-badge>
                                            </h6>
                                            <small class="text-muted mb-2">User
                                              <span class="text-secondary">Jack365</span>
                                              submitted a ticket - 2 week
                                              Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading10">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse10>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Jennifer Carter
                                            </h6>
                                            <small class="text-muted">Commented - 4 week Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                    <b-collapse id="collapse10" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        <p class="text-muted fst-italic mb-2">
                                          " This is an awesome admin dashboard
                                          template. It is extremely well
                                          structured and uses state of the art
                                          components (e.g. one of the only
                                          templates using boostrap 5.1.3 so
                                          far). I integrated it into a Rails 6
                                          project. Needs manual integration work
                                          of course but the template structure
                                          made it easy. "
                                        </p>
                                      </div>
                                    </b-collapse>
                                  </div>
                                </div>
                              </div>
                            </div>
                            <div class="tab-pane" id="monthly" role="tabpanel">
                              <div class="profile-timeline">
                                <div class="accordion accordion-flush" id="monthlyExample">
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading11">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse11>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0 avatar-xs">
                                            <div class="avatar-title bg-light text-success rounded-circle">
                                              M
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Megan Elmore
                                            </h6>
                                            <small class="text-muted">Adding a new event with
                                              attachments - 1 month Ago.</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapse11" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        <b-row class="g-2">
                                          <b-col cols="auto">
                                            <div class="d-flex border border-dashed p-2 rounded position-relative">
                                              <div class="flex-shrink-0">
                                                <i class="ri-image-2-line fs-17 text-danger"></i>
                                              </div>
                                              <div class="flex-grow-1 ms-2">
                                                <h6>
                                                  <b-link href="javascript:void(0);" class="stretched-link">Business
                                                    Template
                                                    - UI/UX
                                                    design</b-link>
                                                </h6>
                                                <small>685 KB</small>
                                              </div>
                                            </div>
                                          </b-col>
                                          <b-col cols="auto">
                                            <div class="d-flex border border-dashed p-2 rounded position-relative">
                                              <div class="flex-shrink-0">
                                                <i class="ri-file-zip-line fs-17 text-info"></i>
                                              </div>
                                              <div class="flex-grow-1 ms-2">
                                                <h6>
                                                  <b-link href="javascript:void(0);" class="stretched-link">Bank
                                                    Management
                                                    System -
                                                    PSD</b-link>
                                                </h6>
                                                <small>8.78 MB</small>
                                              </div>
                                            </div>
                                          </b-col>
                                          <b-col cols="auto">
                                            <div class="d-flex border border-dashed p-2 rounded position-relative">
                                              <div class="flex-shrink-0">
                                                <i class="ri-file-zip-line fs-17 text-info"></i>
                                              </div>
                                              <div class="flex-grow-1 ms-2">
                                                <h6>
                                                  <b-link href="javascript:void(0);" class="stretched-link">Bank
                                                    Management
                                                    System -
                                                    PSD</b-link>
                                                </h6>
                                                <small>8.78 MB</small>
                                              </div>
                                            </div>
                                          </b-col>
                                        </b-row>
                                      </div>
                                    </b-collapse>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading12">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse12>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Jacqueline Steve
                                            </h6>
                                            <small class="text-muted">We has changed 2 attributes on 3
                                              month Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapse12" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        In an awareness campaign, it is vital
                                        for people to begin put 2 and 2 together
                                        and begin to recognize your cause. Too
                                        much or too little spacing, as in the
                                        example below, can make things
                                        unpleasant for the reader. The goal is
                                        to make your text as comfortable to read
                                        as possible. A wonderful serenity has
                                        taken possession of my entire soul, like
                                        these sweet mornings of spring which I
                                        enjoy with my whole heart.
                                      </div>
                                    </b-collapse>

                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading13">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse14>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              New ticket received
                                            </h6>
                                            <small class="text-muted mb-2">User
                                              <span class="text-secondary">Erica245</span>
                                              submitted a ticket - 5 month
                                              Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading14">
                                      <b-link class="accordion-button p-2 shadow-none" data-bs-toggle="collapse"
                                        href="#collapse14" aria-expanded="true">
                                        <div class="d-flex">
                                          <div class="flex-shrink-0 avatar-xs">
                                            <div class="avatar-title bg-light text-muted rounded-circle">
                                              <i class="ri-user-3-fill"></i>
                                            </div>
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Nancy Martino
                                            </h6>
                                            <small class="text-muted">Commented on 24 Nov, 2021.</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapse14" visible>
                                      <div class="accordion-body ms-2 ps-5 fst-italic">
                                        " A wonderful serenity has taken
                                        possession of my entire soul, like these
                                        sweet mornings of spring which I enjoy
                                        with my whole heart. Each design is a
                                        new, unique piece of art birthed into
                                        this world, and while you have the
                                        opportunity to be creative and make your
                                        own style choices. "
                                      </div>
                                    </b-collapse>
                                  </div>
                                  <div class="accordion-item border-0">
                                    <div class="accordion-header" id="heading15">
                                      <b-link class="accordion-button p-2 shadow-none" v-b-toggle.collapse15>
                                        <div class="d-flex">
                                          <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                              class="avatar-xs rounded-circle" />
                                          </div>
                                          <div class="flex-grow-1 ms-3">
                                            <h6 class="fs-14 mb-1">
                                              Lewis Arnold
                                            </h6>
                                            <small class="text-muted">Create new project buildng
                                              product - 8 month Ago</small>
                                          </div>
                                        </div>
                                      </b-link>
                                    </div>

                                    <b-collapse id="collapse15" visible>
                                      <div class="accordion-body ms-2 ps-5">
                                        <p class="text-muted mb-2">
                                          Every team project can have a velzon.
                                          Use the velzon to share information
                                          with your team to understand and
                                          contribute to your project.
                                        </p>
                                        <div class="avatar-group">
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="Christi">
                                            <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                              class="rounded-circle avatar-xs" />
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="Frank Hook">
                                            <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                              class="rounded-circle avatar-xs" />
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title=" Ruby">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle bg-light text-primary">
                                                R
                                              </div>
                                            </div>
                                          </b-link>
                                          <b-link href="javascript: void(0);" class="avatar-group-item"
                                            v-b-tooltip.hover title="more">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle">
                                                2+
                                              </div>
                                            </div>
                                          </b-link>
                                        </div>
                                      </div>
                                    </b-collapse>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                  </b-row>

                  <b-card no-body>
                    <b-card-body>
                      <h5 class="card-title mb-3">Projects</h5>

                      <div class="swiper project-swiper">

                        <swiper :slides-per-view="3" :space-between="50" :thumbs="{ swiper: thumbsSwiper }">
                          <swiper-slide>
                            <div class="swiper-slide">
                              <b-card no-body class="profile-project-card shadow-none profile-project-success mb-0">
                                <b-card-body class="p-4">
                                  <div class="d-flex">
                                    <div class="flex-grow-1 text-muted overflow-hidden">
                                      <h5 class="fs-14 text-truncate mb-1">
                                        <b-link href="#" class="text-dark">ABC Project Customization</b-link>
                                      </h5>
                                      <p class="text-muted text-truncate mb-0">
                                        Last Update :
                                        <span class="fw-semibold text-dark">4 hr Ago</span>
                                      </p>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                      <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                        Inprogress
                                      </b-badge>
                                    </div>
                                  </div>
                                  <div class="d-flex mt-4">
                                    <div class="flex-grow-1">
                                      <div class="d-flex align-items-center gap-2">
                                        <div>
                                          <h5 class="fs-12 text-muted mb-0">
                                            Members :
                                          </h5>
                                        </div>
                                        <div class="avatar-group">
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle bg-light text-primary">
                                                A
                                              </div>
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </b-card-body>
                              </b-card>
                            </div>
                          </swiper-slide>
                          <swiper-slide>
                            <div class="swiper-slide">
                              <b-card no-body class="profile-project-card shadow-none profile-project-danger mb-0">
                                <b-card-body class="p-4">
                                  <div class="d-flex">
                                    <div class="flex-grow-1 text-muted overflow-hidden">
                                      <h5 class="fs-14 text-truncate mb-1">
                                        <b-link href="#" class="text-dark">Client - John</b-link>
                                      </h5>
                                      <p class="text-muted text-truncate mb-0">
                                        Last Update :
                                        <span class="fw-semibold text-dark">1 hr Ago</span>
                                      </p>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                      <b-badge variant="soft-success" class="badge-soft-success fs-10">
                                        Completed
                                      </b-badge>
                                    </div>
                                  </div>
                                  <div class="d-flex mt-4">
                                    <div class="flex-grow-1">
                                      <div class="d-flex align-items-center gap-2">
                                        <div>
                                          <h5 class="fs-12 text-muted mb-0">
                                            Members :
                                          </h5>
                                        </div>
                                        <div class="avatar-group">
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle bg-light text-primary">
                                                C
                                              </div>
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </b-card-body>
                              </b-card>
                            </div>
                          </swiper-slide>
                          <swiper-slide>
                            <div class="swiper-slide">
                              <b-card no-body class="profile-project-card shadow-none profile-project-info mb-0">
                                <b-card-body class="p-4">
                                  <div class="d-flex">
                                    <div class="flex-grow-1 text-muted overflow-hidden">
                                      <h5 class="fs-14 text-truncate mb-1">
                                        <b-link href="#" class="text-dark">Brand logo Design</b-link>
                                      </h5>
                                      <p class="text-muted text-truncate mb-0">
                                        Last Update :
                                        <span class="fw-semibold text-dark">2 hr Ago</span>
                                      </p>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                      <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                        Inprogress
                                      </b-badge>
                                    </div>
                                  </div>
                                  <div class="d-flex mt-4">
                                    <div class="flex-grow-1">
                                      <div class="d-flex align-items-center gap-2">
                                        <div>
                                          <h5 class="fs-12 text-muted mb-0">
                                            Members :
                                          </h5>
                                        </div>
                                        <div class="avatar-group">
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </b-card-body>
                              </b-card>
                            </div>
                          </swiper-slide>

                          <swiper-slide>
                            <div class="swiper-slide">
                              <b-card no-body class="profile-project-card shadow-none profile-project-danger mb-0">
                                <b-card-body class="p-4">
                                  <div class="d-flex">
                                    <div class="flex-grow-1 text-muted overflow-hidden">
                                      <h5 class="fs-14 text-truncate mb-1">
                                        <b-link href="#" class="text-dark">Project update</b-link>
                                      </h5>
                                      <p class="text-muted text-truncate mb-0">
                                        Last Update :
                                        <span class="fw-semibold text-dark">4 hr Ago</span>
                                      </p>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                      <b-badge variant="soft-success" class="badge-soft-success fs-10">
                                        Completed
                                      </b-badge>
                                    </div>
                                  </div>

                                  <div class="d-flex mt-4">
                                    <div class="flex-grow-1">
                                      <div class="d-flex align-items-center gap-2">
                                        <div>
                                          <h5 class="fs-12 text-muted mb-0">
                                            Members :
                                          </h5>
                                        </div>
                                        <div class="avatar-group">
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </b-card-body>
                              </b-card>
                            </div>
                          </swiper-slide>
                          <swiper-slide>
                            <div class="swiper-slide">
                              <b-card no-body class="profile-project-card shadow-none profile-project-warning mb-0">
                                <b-card-body class="p-4">
                                  <div class="d-flex">
                                    <div class="flex-grow-1 text-muted overflow-hidden">
                                      <h5 class="fs-14 text-truncate mb-1">
                                        <b-link href="#" class="text-dark">Chat App</b-link>
                                      </h5>
                                      <p class="text-muted text-truncate mb-0">
                                        Last Update :
                                        <span class="fw-semibold text-dark">1 hr Ago</span>
                                      </p>
                                    </div>
                                    <div class="flex-shrink-0 ms-2">
                                      <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                        Inprogress
                                      </b-badge>
                                    </div>
                                  </div>

                                  <div class="d-flex mt-4">
                                    <div class="flex-grow-1">
                                      <div class="d-flex align-items-center gap-2">
                                        <div>
                                          <h5 class="fs-12 text-muted mb-0">
                                            Members :
                                          </h5>
                                        </div>
                                        <div class="avatar-group">
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                                class="rounded-circle img-fluid" />
                                            </div>
                                          </div>
                                          <div class="avatar-group-item">
                                            <div class="avatar-xs">
                                              <div class="avatar-title rounded-circle bg-light text-primary">
                                                A
                                              </div>
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </b-card-body>
                              </b-card>
                            </div>
                          </swiper-slide>
                        </swiper>

                      </div>
                    </b-card-body>
                  </b-card>
                </b-col>
              </b-row>
            </div>
            <div class="tab-pane fade" id="activities" role="tabpanel">
              <b-card no-body>
                <b-card-body>
                  <h5 class="card-title mb-3">Activities</h5>
                  <div class="acitivity-timeline">
                    <div class="acitivity-item d-flex">
                      <div class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-1.jpg" alt=""
                          class="avatar-xs rounded-circle acitivity-avatar" />
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">
                          Oliver Phillips
                          <b-badge variant="soft-primary" class="text-primary align-middle">New</b-badge>
                        </h6>
                        <p class="text-muted mb-2">
                          We talked about a project on linkedin.
                        </p>
                        <small class="mb-0 text-muted">Today</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0 avatar-xs acitivity-avatar">
                        <div class="avatar-title bg-soft-success text-success rounded-circle">
                          N
                        </div>
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">
                          Nancy Martino
                          <b-badge variant="soft-secondary" class="text-secondary align-middle">In Progress</b-badge>
                        </h6>
                        <p class="text-muted mb-2">
                          <i class="ri-file-text-line align-middle ms-2"></i>
                          Create new project Buildng product
                        </p>
                        <div class="avatar-group mb-2">
                          <b-link href="javascript: void(0);" class="avatar-group-item" data-bs-toggle="tooltip"
                            data-bs-placement="top" title="" data-bs-original-title="Christi">
                            <img src="@/assets/images/users/avatar-4.jpg" alt="" class="rounded-circle avatar-xs" />
                          </b-link>
                          <b-link href="javascript: void(0);" class="avatar-group-item" data-bs-toggle="tooltip"
                            data-bs-placement="top" title="" data-bs-original-title="Frank Hook">
                            <img src="@/assets/images/users/avatar-3.jpg" alt="" class="rounded-circle avatar-xs" />
                          </b-link>
                          <b-link href="javascript: void(0);" class="avatar-group-item" data-bs-toggle="tooltip"
                            data-bs-placement="top" title="" data-bs-original-title=" Ruby">
                            <div class="avatar-xs">
                              <div class="avatar-title rounded-circle bg-light text-primary">
                                R
                              </div>
                            </div>
                          </b-link>
                          <b-link href="javascript: void(0);" class="avatar-group-item" data-bs-toggle="tooltip"
                            data-bs-placement="top" title="" data-bs-original-title="more">
                            <div class="avatar-xs">
                              <div class="avatar-title rounded-circle">2+</div>
                            </div>
                          </b-link>
                        </div>
                        <small class="mb-0 text-muted">Yesterday</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-2.jpg" alt=""
                          class="avatar-xs rounded-circle acitivity-avatar" />
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">
                          Natasha Carey
                          <b-badge variant="soft-success" class="text-success align-middle">Completed</b-badge>
                        </h6>
                        <p class="text-muted mb-2">
                          Adding a new event with attachments
                        </p>
                        <b-row>
                          <b-col xxl="4">
                            <b-row class="border border-dashed gx-2 p-2 mb-2">
                              <b-col cols="4">
                                <img src="@/assets/images/small/img-2.jpg" alt="" class="img-fluid rounded" />
                              </b-col>
                              <b-col cols="4">
                                <img src="@/assets/images/small/img-3.jpg" alt="" class="img-fluid rounded" />
                              </b-col>
                              <b-col cols="4">
                                <img src="@/assets/images/small/img-4.jpg" alt="" class="img-fluid rounded" />
                              </b-col>
                            </b-row>
                          </b-col>
                        </b-row>
                        <small class="mb-0 text-muted">25 Nov</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-6.jpg" alt=""
                          class="avatar-xs rounded-circle acitivity-avatar" />
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">Bethany Johnson</h6>
                        <p class="text-muted mb-2">
                          added a new member to velzon dashboard
                        </p>
                        <small class="mb-0 text-muted">19 Nov</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0">
                        <div class="avatar-xs acitivity-avatar">
                          <div class="avatar-title rounded-circle bg-soft-danger text-danger">
                            <i class="ri-shopping-bag-line"></i>
                          </div>
                        </div>
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">
                          Your order is placed
                          <b-badge variant="soft-danger" class="text-danger align-middle ms-1">Out of Delivery</b-badge>
                        </h6>
                        <p class="text-muted mb-2">
                          These customers can rest assured their order has been
                          placed.
                        </p>
                        <small class="mb-0 text-muted">16 Nov</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-7.jpg" alt=""
                          class="avatar-xs rounded-circle acitivity-avatar" />
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">Lewis Pratt</h6>
                        <p class="text-muted mb-2">
                          They all have something to say beyond the words on the
                          page. They can come across as casual or neutral,
                          exotic or graphic.
                        </p>
                        <small class="mb-0 text-muted">22 Oct</small>
                      </div>
                    </div>
                    <div class="acitivity-item py-3 d-flex">
                      <div class="flex-shrink-0">
                        <div class="avatar-xs acitivity-avatar">
                          <div class="avatar-title rounded-circle bg-soft-info text-info">
                            <i class="ri-line-chart-line"></i>
                          </div>
                        </div>
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">Monthly sales report</h6>
                        <p class="text-muted mb-2">
                          <span class="text-danger">2 days left</span>
                          notification to submit the monthly sales report.
                          <b-link href="javascript:void(0);" class="link-warning text-decoration-underline">Reports
                            Builder</b-link>
                        </p>
                        <small class="mb-0 text-muted">15 Oct</small>
                      </div>
                    </div>
                    <div class="acitivity-item d-flex">
                      <div class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-8.jpg" alt=""
                          class="avatar-xs rounded-circle acitivity-avatar" />
                      </div>
                      <div class="flex-grow-1 ms-3">
                        <h6 class="mb-1">
                          New ticket received
                          <b-badge variant="soft-success" class="text-success align-middle">Completed</b-badge>
                        </h6>
                        <p class="text-muted mb-2">
                          User
                          <span class="text-secondary">Erica245</span> submitted
                          a ticket.
                        </p>
                        <small class="mb-0 text-muted">26 Aug</small>
                      </div>
                    </div>
                  </div>
                </b-card-body>
              </b-card>
            </div>
            <div class="tab-pane fade" id="projects" role="tabpanel">
              <b-card no-body>
                <b-card-body>
                  <b-row>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-warning">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Chat App Update</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">2 year Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                Inprogress
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-1.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-light text-primary">
                                        J
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-success">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">ABC Project Customization</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">2 month Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-primary" class="badge-soft-primary fs-10">
                                Progress
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-primary">
                                        2+
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-info">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Client - Frank Hook</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">1 hr Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-info" class="badge-soft-info fs-10">New</b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-light text-primary">
                                        M
                                      </div>
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-primary">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Velzon Project</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">11 hr Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-success" class="badge-soft-success fs-10">
                                Completed
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-danger">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Brand Logo Design</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">10 min Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-info" class="badge-soft-info fs-10">New</b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-light text-primary">
                                        E
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-primary">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Chat App</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">8 hr Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                Inprogress
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-light text-primary">
                                        R
                                      </div>
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-warning">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Project Update</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">48 min Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-warning" class="badge-soft-warning fs-10">
                                Inprogress
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none profile-project-success">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Client - Jennifer</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">30 min Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-primary" class="badge-soft-primary fs-10">
                                Process
                              </b-badge>
                            </div>
                          </div>

                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-1.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none mb-xxl-0 profile-project-info">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Bsuiness Template - UI/UX design</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">7 month Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-success" class="badge-soft-success fs-10">
                                Completed
                              </b-badge>
                            </div>
                          </div>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-primary">
                                        2+
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none mb-xxl-0 profile-project-success">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Update Project</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">1 month Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-info" class="badge-soft-info fs-10">New</b-badge>
                            </div>
                          </div>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-light text-primary">
                                        A
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none mb-sm-0 profile-project-danger">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">Bank Management System</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">10 month Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-success" class="badge-soft-success fs-10">
                                Completed
                              </b-badge>
                            </div>
                          </div>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <div class="avatar-title rounded-circle bg-primary">
                                        2+
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col xxl="3" sm="6">
                      <b-card no-body class="profile-project-card shadow-none mb-0 profile-project-primary">
                        <b-card-body class="p-4">
                          <div class="d-flex">
                            <div class="flex-grow-1 text-muted overflow-hidden">
                              <h5 class="fs-14 text-truncate">
                                <b-link href="#" class="text-dark">PSD to HTML Convert</b-link>
                              </h5>
                              <p class="text-muted text-truncate mb-0">
                                Last Update :
                                <span class="fw-semibold text-dark">29 min Ago</span>
                              </p>
                            </div>
                            <div class="flex-shrink-0 ms-2">
                              <b-badge variant="soft-info" class="badge-soft-info fs-10">New</b-badge>
                            </div>
                          </div>
                          <div class="d-flex mt-4">
                            <div class="flex-grow-1">
                              <div class="d-flex align-items-center gap-2">
                                <div>
                                  <h5 class="fs-12 text-muted mb-0">
                                    Members :
                                  </h5>
                                </div>
                                <div class="avatar-group">
                                  <div class="avatar-group-item">
                                    <div class="avatar-xs">
                                      <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                        class="rounded-circle img-fluid" />
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </b-card-body>
                      </b-card>
                    </b-col>
                    <b-col lg="12">
                      <div class="mt-4">
                        <ul class="pagination pagination-separated justify-content-center mb-0">
                          <li class="page-item disabled">
                            <b-link href="javascript:void(0);" class="page-link"><i class="mdi mdi-chevron-left"></i>
                            </b-link>
                          </li>
                          <li class="page-item active">
                            <b-link href="javascript:void(0);" class="page-link">1</b-link>
                          </li>
                          <li class="page-item">
                            <b-link href="javascript:void(0);" class="page-link">2</b-link>
                          </li>
                          <li class="page-item">
                            <b-link href="javascript:void(0);" class="page-link">3</b-link>
                          </li>
                          <li class="page-item">
                            <b-link href="javascript:void(0);" class="page-link">4</b-link>
                          </li>
                          <li class="page-item">
                            <b-link href="javascript:void(0);" class="page-link">5</b-link>
                          </li>
                          <li class="page-item">
                            <b-link href="javascript:void(0);" class="page-link"><i class="mdi mdi-chevron-right"></i>
                            </b-link>
                          </li>
                        </ul>
                      </div>
                    </b-col>
                  </b-row>
                </b-card-body>
              </b-card>
            </div>
            <div class="tab-pane fade" id="documents" role="tabpanel">
              <b-card no-body>
                <b-card-body>
                  <div class="d-flex align-items-center mb-4">
                    <h5 class="card-title flex-grow-1 mb-0">Documents</h5>
                    <div class="flex-shrink-0">
                      <input class="form-control d-none" type="file" id="formFile" />
                      <label for="formFile" class="btn btn-danger"><i class="ri-upload-2-fill me-1 align-bottom"></i>
                        Upload File</label>
                    </div>
                  </div>
                  <b-row>
                    <b-col lg="12">
                      <div class="table-responsive">
                        <table class="table table-borderless align-middle mb-0">
                          <thead class="table-light">
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
                                    <div class="avatar-title bg-soft-primary text-primary rounded fs-20">
                                      <i class="ri-file-zip-fill"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0)">Artboard-documents.zip</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>Zip File</td>
                              <td>4.57 MB</td>
                              <td>12 Dec 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                            <tr>
                              <td>
                                <div class="d-flex align-items-center">
                                  <div class="avatar-sm">
                                    <div class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                      <i class="ri-file-pdf-fill"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0);">Bank Management System</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>PDF File</td>
                              <td>8.89 MB</td>
                              <td>24 Nov 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                            <tr>
                              <td>
                                <div class="d-flex align-items-center">
                                  <div class="avatar-sm">
                                    <div class="avatar-title bg-soft-secondary text-secondary rounded fs-20">
                                      <i class="ri-video-line"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0);">Tour-video.mp4</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>MP4 File</td>
                              <td>14.62 MB</td>
                              <td>19 Nov 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                            <tr>
                              <td>
                                <div class="d-flex align-items-center">
                                  <div class="avatar-sm">
                                    <div class="avatar-title bg-soft-success text-success rounded fs-20">
                                      <i class="ri-file-excel-fill"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0);">Account-statement.xsl</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>XSL File</td>
                              <td>2.38 KB</td>
                              <td>14 Nov 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                            <tr>
                              <td>
                                <div class="d-flex align-items-center">
                                  <div class="avatar-sm">
                                    <div class="avatar-title bg-soft-info text-info rounded fs-20">
                                      <i class="ri-folder-line"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0);">Project Screenshots Collection</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>Floder File</td>
                              <td>87.24 MB</td>
                              <td>08 Nov 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                            <tr>
                              <td>
                                <div class="d-flex align-items-center">
                                  <div class="avatar-sm">
                                    <div class="avatar-title bg-soft-danger text-danger rounded fs-20">
                                      <i class="ri-image-2-fill"></i>
                                    </div>
                                  </div>
                                  <div class="ms-3 flex-grow-1">
                                    <h6 class="fs-14 mb-0">
                                      <b-link class="text-body" href="javascript:void(0);">Velzon-logo.png</b-link>
                                    </h6>
                                  </div>
                                </div>
                              </td>
                              <td>PNG File</td>
                              <td>879 KB</td>
                              <td>02 Nov 2021</td>
                              <td>
                                <b-dropdown variant="light" toggle-class="arrow-none px-1" class="btn-icon" no-caret>
                                  <template #button-content><i class="ri-equalizer-fill"></i>
                                  </template>
                                  <b-dropdown-item href="#">
                                    <i class="ri-eye-fill me-2 align-middle text-muted"></i>View
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-download-2-fill me-2 align-middle text-muted"></i>Download
                                  </b-dropdown-item>
                                  <b-dropdown-item href="#">
                                    <i class="ri-delete-bin-5-line me-2 align-middle text-muted"></i>Delete
                                  </b-dropdown-item>
                                </b-dropdown>
                              </td>
                            </tr>
                          </tbody>
                        </table>
                      </div>
                      <div class="text-center mt-3">
                        <b-link href="javascript:void(0);" class="text-success"><i
                            class="mdi mdi-loading mdi-spin fs-20 align-middle me-2"></i>
                          Load more
                        </b-link>
                      </div>
                    </b-col>
                  </b-row>
                </b-card-body>
              </b-card>
            </div>
          </div>
        </div>
      </b-col>
    </b-row>
  </Layout>
</template>
