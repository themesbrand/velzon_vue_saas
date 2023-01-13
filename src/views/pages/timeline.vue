<script>
import SwiperCore, { Thumbs } from "swiper";

import "swiper/swiper-bundle.css";

SwiperCore.use([Thumbs]);

import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Timeline",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Timeline",
            items: [
                {
                    text: "Pages",
                    href: "/",
                },
                {
                    text: "Timeline",
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
                <div>
                    <h5>Center Timeline</h5>
                    <div class="timeline">
                        <div class="timeline-item left">
                            <i class="icon ri-stack-line"></i>
                            <div class="date fs-13">15 Dec 2021</div>
                            <div class="content">
                                <div class="d-flex">
                                    <div class="flex-shrink-0">
                                        <img src="@/assets/images/users/avatar-5.jpg" alt="" class="avatar-sm rounded">
                                    </div>
                                    <div class="flex-grow-1 ms-3">
                                        <h5 class="fs-14">@Erica245 <small class="text-muted fs-13 fw-normal">- 10 min
                                                Ago</small></h5>
                                        <p class="text-muted mb-2">Wish someone a sincere ‘good luck in your new job’
                                            with these sweet messages. Make sure you pick out a good luck new job card
                                            to go with the words, and pop a beautiful bunch of flowers from our gift
                                            range in your basket, to make them feel super special.</p>
                                        <div class="hstack gap-2">
                                            <b-link class="btn btn-sm btn-light"><span class="me-1">&#128293;</span> 19</b-link>
                                            <b-link class="btn btn-sm btn-light"><span class="me-1">&#129321;</span> 22</b-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="timeline-item right">
                            <i class="icon ri-vip-diamond-line"></i>
                            <div class="date fs-13">22 Oct 2021</div>
                            <div class="content">
                                <h5 class="fs-14">Adding a new event with attachments</h5>
                                <p class="text-muted">Too much or too little spacing, as in the example below, can make
                                    things unpleasant for the reader.</p>
                                <b-row class="g-2">
                                    <b-col sm="6">
                                        <div class="d-flex border border-dashed p-2 rounded position-relative">
                                            <div class="flex-shrink-0 avatar-xs">
                                                <div class="avatar-title bg-soft-danger text-danger fs-15 rounded">
                                                    <i class="ri-image-2-line"></i>
                                                </div>
                                            </div>
                                            <div class="flex-shrink-0">

                                            </div>
                                            <div class="flex-grow-1 overflow-hidden ms-2">
                                                <h6 class="text-truncate mb-0"><b-link href="javascript:void(0);"
                                                        class="stretched-link">Business Template - UI/UX design</b-link></h6>
                                                <small>685 KB</small>
                                            </div>
                                        </div>
                                    </b-col>
                                    <b-col sm="6">
                                        <div class="d-flex border border-dashed p-2 rounded position-relative">
                                            <div class="flex-shrink-0 avatar-xs">
                                                <div class="avatar-title bg-soft-info text-info fs-15 rounded">
                                                    <i class="ri-file-zip-line"></i>
                                                </div>
                                            </div>
                                            <div class="flex-grow-1 ms-2 overflow-hidden">
                                                <h6 class="mb-0 text-truncate"><b-link href="javascript:void(0);"
                                                        class="stretched-link">Bank Management System - PSD</b-link></h6>
                                                <small>8.78 MB</small>
                                            </div>
                                        </div>
                                    </b-col>
                                </b-row>
                            </div>
                        </div>
                        <div class="timeline-item left">
                            <i class="icon ri-gift-line"></i>
                            <div class="date fs-13">10 Jul 2021</div>
                            <div class="content">
                                <h5 class="fs-14">Create new project buildng product</h5>
                                <p class="text-muted">Every team project can have a velzon. Use the velzon to share
                                    information with your team to understand and contribute to your project.</p>
                                <div class="avatar-group mb-2">
                                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover title="Christi">
                                        <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                            class="rounded-circle avatar-xs">
                                    </b-link>
                                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover title="Frank Hook">
                                        <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                            class="rounded-circle avatar-xs">
                                    </b-link>
                                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover title="Ruby">
                                        <div class="avatar-xs">
                                            <div class="avatar-title rounded-circle bg-light text-primary">
                                                R
                                            </div>
                                        </div>
                                    </b-link>
                                    <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover title="more">
                                        <div class="avatar-xs">
                                            <div class="avatar-title rounded-circle">
                                                2+
                                            </div>
                                        </div>
                                    </b-link>
                                </div>
                            </div>
                        </div>
                        <div class="timeline-item right">
                            <i class="icon ri-shield-star-line"></i>
                            <div class="date fs-13">18 May 2021</div>
                            <div class="content">
                                <h5 class="fs-14">Donald Palmer <small class="text-muted fs-13 fw-normal">- Has changed 2
                                        attributes</small></h5>
                                <p class="text-muted fst-italic mb-2">" This is an awesome admin dashboard template. It
                                    is extremely well structured and uses state of the art components (e.g. one of the
                                    only templates using boostrap 5.1.3 so far). I integrated it into a Rails 6 project.
                                    Needs manual integration work of course but the template structure made it easy. "
                                </p>
                                <div class="hstack gap-2">
                                    <b-link class="btn btn-sm bg-light"><span class="me-1">&#128151;</span> 35</b-link>
                                    <b-link class="btn btn-sm btn-light"><span class="me-1">&#128077;</span> 10</b-link>
                                    <b-link class="btn btn-sm btn-light"><span class="me-1">&#128591;</span> 10</b-link>
                                </div>
                            </div>
                        </div>
                        <div class="timeline-item left">
                            <i class="icon ri-user-smile-line"></i>
                            <div class="date fs-13">10 Feb 2021</div>
                            <div class="content">
                                <h5 class="fs-14">Velzon admin dashboard templates layout upload</h5>
                                <p class="text-muted">Powerful, clean & modern responsive bootstrap 5 admin template.
                                    The maximum file size for uploads in this demo :</p>
                                <b-row class="border border-dashed rounded gx-2 p-2">
                                    <b-col cols="3">
                                        <img src="@/assets/images/small/img-2.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                    <b-col cols="3">
                                        <img src="@/assets/images/small/img-3.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                    <b-col cols="3">
                                        <img src="@/assets/images/small/img-4.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                    <b-col cols="3">
                                        <img src="@/assets/images/small/img-6.jpg" alt="" class="img-fluid rounded">
                                    </b-col>
                                </b-row>
                            </div>
                        </div>
                        <div class="timeline-item right">
                            <i class="icon ri-fire-line"></i>
                            <div class="date fs-13">01 Jan 2021</div>
                            <div class="content">
                                <h5 class="fs-14">New ticket received <b-badge variant="soft-success"
                                        class="text-success fs-10 align-middle ms-1">Completed</b-badge>
                                </h5>
                                <p class="text-muted mb-2">
                                    It is important for us that we receive email notifications when a ticket is created
                                    as our IT staff are mobile and will not always be looking at the dashboard for new
                                    tickets.
                                </p>
                                <b-link href="javascript:void(0);" class="link-primary text-decoration-underline">Read More
                                    <i class="ri-arrow-right-line"></i></b-link>
                            </div>
                        </div>
                    </div>
                </div>
            </b-col>
        </b-row>

        <b-row class="mt-4">
            <b-col lg="12">
                <div>
                    <h5 class="mb-4">Left Timeline</h5>
                    <div class="timeline-2">
                        <div class="timeline-year">
                            <p>12 Dec 2021</p>
                        </div>
                        <div class="timeline-continue">
                            <b-row class="timeline-right">
                                <b-col cols="12">
                                    <p class="timeline-date fs-13">
                                        02:35AM to 04:30PM
                                    </p>
                                </b-col>
                                <b-col cols="12">
                                    <div class="timeline-box">
                                        <div class="timeline-text">
                                            <div class="d-flex">
                                                <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                                    class="avatar-sm rounded" />
                                                <div class="flex-grow-1 ms-3">
                                                    <h5 class="fs-15 mb-1">Frank hook joined with our company</h5>
                                                    <p class="text-muted mb-0">It makes a statement, it’s impressive
                                                        graphic design. Increase or decrease the letter spacing
                                                        depending on the situation and try, try again until it looks
                                                        right, and each letter has the perfect spot of its own. </p>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>

                            <b-row class="timeline-right">
                                <b-col cols="12">
                                    <p class="timeline-date fs-13">
                                        02:35AM to 04:30PM
                                    </p>
                                </b-col>
                                <b-col cols="12">
                                    <div class="timeline-box">
                                        <div class="timeline-text">
                                            <h5 class="fs-15">Trip planning</h5>
                                            <p class="text-muted">In the trip planner, keep only one or two activities
                                                in a day if the purpose of the trip is to relax and take it easy during
                                                the vacation :</p>
                                            <b-row class="border border-dashed rounded gx-2 p-2">
                                                <b-col cols="3">
                                                    <b-link href="javascript:void(0);"><img
                                                            src="@/assets/images/small/img-7.jpg" alt=""
                                                            class="img-fluid rounded"></b-link>
                                                </b-col>
                                                <b-col cols="3">
                                                    <b-link href="javascript:void(0);"><img
                                                            src="@/assets/images/small/img-3.jpg" alt=""
                                                            class="img-fluid rounded"></b-link>
                                                </b-col>
                                                <b-col cols="3">
                                                    <b-link href="javascript:void(0);"><img
                                                            src="@/assets/images/small/img-10.jpg" alt=""
                                                            class="img-fluid rounded"></b-link>
                                                </b-col>
                                                <b-col cols="3">
                                                    <b-link href="javascript:void(0);"><img
                                                            src="@/assets/images/small/img-9.jpg" alt=""
                                                            class="img-fluid rounded"></b-link>
                                                </b-col>
                                            </b-row>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>

                            <b-row>
                                <b-col cols="12">
                                    <div class="timeline-year">
                                        <p>08 Dec 2021</p>
                                    </div>
                                </b-col>
                            </b-row>

                            <b-row class="timeline-right">
                                <b-col cols="12">
                                    <p class="timeline-date fs-13">
                                        02:35AM to 04:30PM
                                    </p>
                                </b-col>
                                <b-col cols="12">
                                    <div class="timeline-box">
                                        <div class="timeline-text">
                                            <h5 class="fs-15">Velzon - Project Discussion</h5>
                                            <p class="text-muted mb-0">The purpose of the discussion is to interpret and
                                                describe the significance of your findings in light of what was already
                                                known about the research problem being investigated, and to explain any
                                                new understanding or fresh insights about the problem after you've taken
                                                the findings into consideration.</p>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>

                            <b-row class="timeline-right">
                                <b-col cols="12">
                                    <p class="timeline-date fs-13">
                                        10:24AM to 11:15PM
                                    </p>
                                </b-col>
                                <b-col cols="12">
                                    <div class="timeline-box">
                                        <div class="timeline-text">
                                            <h5 class="fs-15">Client Meeting (Nancy Martino)</h5>
                                            <p class="text-muted mb-0">A client meeting, meaning, direct collaboration
                                                and communication with a customer, is the best way to understand their
                                                needs and how you can help support them.</p>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>

                            <b-row class="timeline-right">
                                <b-col cols="12">
                                    <p class="timeline-date fs-13">
                                        9:20AM to 10:05PM
                                    </p>
                                </b-col>
                                <b-col cols="12">
                                    <div class="timeline-box">
                                        <div class="timeline-text">
                                            <h5 class="fs-15">Designer & Developer Meeting</h5>
                                            <ul class="mb-0 text-muted vstack gap-2">
                                                <li>Last update fs-13s</li>
                                                <li>Weekly Planning</li>
                                                <li>Work Distribution</li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>
                        </div>

                        <div class="timeline-year">
                            <p><span>05 Dec 2021</span></p>
                        </div>
                        <div class="timeline-launch">
                            <div class="timeline-box">
                                <div class="timeline-text">
                                    <h5 class="fs-15">Our Company Activity</h5>
                                    <p class="text-muted text-capitalize mb-0">Wow...!!! What a Journey So Far...!!!</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </b-col>
        </b-row>
    </Layout>
</template>
