<script>
import { VueDraggableNext } from 'vue-draggable-next';
import flatPickr from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";

import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

import Lottie from "@/components/widgets/lottie.vue";
import animationData from "@/components/widgets/gsqxdxog.json";

export default {
    page: {
        title: "Kanban Board",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Kanban Board",
            items: [
                {
                    text: "Tasks",
                    href: "/",
                },
                {
                    text: "Kanban Board",
                    active: true,
                },
            ],
            modalShow: false,
            modalShow1: false,
            modalShow2: false,
            modalShow3: false,
            config: {
                wrap: true, // set wrap to true only when using 'input-group'
                altFormat: "M j, Y",
                altInput: true,
                dateFormat: "d M, Y",
            },
            date: null,
            date1: null,
            defaultOptions: { animationData: animationData },
            unassigned: [
                {
                    title: "Profile Page Structure",
                    description: "Profile Page means a web page accessible to the public or to guests.",
                    features: ["Admin"],
                    users: [require("@/assets/images/users/avatar-6.jpg"), require("@/assets/images/users/avatar-5.jpg")],
                    id: "#VL2436",
                    watch: "04",
                    message: "19",
                    file: "2"
                },
                {
                    title: "Velzon - Admin Layout Design",
                    description: "The dashboard is the front page of the Administration UI.",
                    features: ["Layout", "Admin", "Dashboard"],
                    users: [require("@/assets/images/users/avatar-7.jpg"), require("@/assets/images/users/avatar-6.jpg"), require("@/assets/images/users/avatar-1.jpg")],
                    id: "#VL2436",
                    watch: "04",
                    message: "19",
                    file: "2",
                    date: " 07 Jan, 2022"
                }
            ],
            todo: [
                {
                    title: "Admin Layout Design",
                    description: "Landing page template with clean, minimal and modern design.",
                    features: ["Design", "Wensite"],
                    users: [require("@/assets/images/users/avatar-10.jpg"), require("@/assets/images/users/avatar-3.jpg")],
                    id: "#VL2436",
                    watch: "13",
                    message: "52",
                    file: "17",
                    date: " 07 Jan, 2022"
                },
                {
                    title: "Marketing & Sales",
                    description: "Sales and marketing are two business functions within an organization.",
                    features: ["Marketing", "Business"],
                    users: [require("@/assets/images/users/avatar-9.jpg"), require("@/assets/images/users/avatar-8.jpg")],
                    id: "#VL2436",
                    watch: "24",
                    message: "10",
                    file: "10",
                    date: " 27 Dec, 2021"
                },
            ],
            inprogress: [
                {
                    title: "Brand Logo Design ",
                    description: "BrandCrowd's brand logo maker allows you to generate and customize stand-out brand logos in minutes.",
                    features: ["Logo", "Design", "UI/UX"],
                    users: [require("@/assets/images/users/avatar-10.jpg"), require("@/assets/images/users/avatar-3.jpg")],
                    id: "#VL2436",
                    watch: "24",
                    message: "10",
                    file: "10",
                    date: " 22 Dec, 2022"
                },
                {
                    title: "Change Old App Icon",
                    description: "Change app icons on Android: How do you change the look of your apps.",
                    features: ["Marketing", "Business"],
                    users: [require("@/assets/images/users/avatar-9.jpg"), require("@/assets/images/users/avatar-8.jpg")],
                    id: "#VL2436",
                    watch: "64",
                    message: "35",
                    file: "23",
                    date: " 24 Oct, 2021"
                },
            ],
            reviews: [
                {
                    title: "Product Features Analysis",
                    description: "An essential part of strategic planning is running a product feature analysis.",
                    features: ["Project", "Analysis"],
                    users: [require("@/assets/images/users/avatar-5.jpg"), require("@/assets/images/users/avatar-6.jpg")],
                    id: "#VL2436",
                    watch: "14",
                    message: "31",
                    file: "07",
                    date: " 05 Jan, 2022"
                },
                {
                    title: "Create a Graph of Sketch",
                    description: "To make a pie chart with equal slices create a perfect circle by selecting an Oval Tool.",
                    features: ["Sketch", "Marketing", "Design"],
                    users: [require("@/assets/images/users/avatar-4.jpg"), require("@/assets/images/users/avatar-8.jpg"), require("@/assets/images/users/avatar-2.jpg"), require("@/assets/images/users/avatar-1.jpg")],
                    id: "#VL2436",
                    watch: "64",
                    message: "35",
                    file: "23",
                    date: " 24 Oct, 2021"
                },
            ],
            completed: [
                {
                    title: "Create a Blog Template UI",
                    description: "Landing page template with clean, minimal and modern design.",
                    features: ["Design", "Website"],
                    users: [require("@/assets/images/users/avatar-8.jpg"), require("@/assets/images/users/avatar-7.jpg"), require("@/assets/images/users/avatar-6.jpg")],
                    id: "#VL2451",
                    watch: "24",
                    message: "10",
                    file: "10",
                    date: " 05 Jan, 2022"
                },
            ],
            newData: [
                {
                    title: "Banner Design for FB & Twitter",
                    image: require("@/assets/images/small/img-4.jpg"),
                    features: ["UI/UX", "Graphic"],
                    users: [require("@/assets/images/users/avatar-8.jpg"), require("@/assets/images/users/avatar-7.jpg"), require("@/assets/images/users/avatar-6.jpg")],
                    id: "#VL2451",
                    watch: "24",
                    message: "10",
                    file: "10",
                    date: " 05 Jan, 2022"
                },
            ],
            enabled: true,

            dragging: false
        };
    },
    methods: {
        log(event) {
            console.log(event);
        },

        deleteTask() {
            this.modalShow3 = true;
            document.getElementById("deleteTask")
            addEventListener("click", (e) => {
                document
                    .getElementById("delete-record")
                    .addEventListener("click", () => {
                        if (e.target.closest('.tasks-list')) {
                            e.target.closest('.tasks-list').remove();
                        }
                        this.modalShow3 = false;
                    });
            });
        },

        addNewTask() {
            // var projectName = document.getElementById("projectName").value;
            // var sub_tasks = document.getElementById("sub-tasks").value;
            // var task_description = document.getElementById("task-description").value;
            // var formFile = document.getElementById("formFile").value;
            // var due_date = document.getElementById("due-date").value;
            // var categories = document.getElementById("categories").value;
            // var tasks_progress = document.getElementById("tasks-progress").value;

            // var list = document.querySelectorAll('.tasks-list');
            // list.forEach(element => {
            //     // var listName = element.childNodes[0].childNodes[0].children[0].childNodes[0].data;
            //     // console.log(listName)
            // })

            // for (var k in list) {
            //     if (list) {
            //         var n = k;
            //         var listName = list[k].childNodes[0].childNodes[0].children[k].childNodes[0];
            //         console.log(listName)
            //         console.log('n',n)
            //     }
            // }
        }
    },
    components: {
        Layout,
        PageHeader,
        draggable: VueDraggableNext,
        lottie: Lottie,
        flatPickr
    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />

        <b-card no-body>
            <b-card-body>
                <b-row class="g-2">
                    <b-col lg="auto">
                        <div class="hstack gap-2">
                            <b-button variant="primary" @click="modalShow1 = !modalShow1"><i class="ri-add-line align-bottom me-1"></i> Create Board</b-button>
                        </div>
                    </b-col>
                    <b-col lg="3" class="col-auto">
                        <div class="search-box">
                            <input type="text" class="form-control search" placeholder="Search for project, tasks...">
                            <i class="ri-search-line search-icon"></i>
                        </div>
                    </b-col>
                    <div class="col-auto ms-sm-auto">
                        <div class="avatar-group" id="newMembar">
                            <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                                title="Nancy">
                                <img src="@/assets/images/users/avatar-5.jpg" alt="" class="rounded-circle avatar-xs">
                            </b-link>
                            <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                                title="Frank">
                                <img src="@/assets/images/users/avatar-3.jpg" alt="" class="rounded-circle avatar-xs">
                            </b-link>
                            <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                                title="Tonya">
                                <img src="@/assets/images/users/avatar-10.jpg" alt="" class="rounded-circle avatar-xs">
                            </b-link>
                            <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                                title="Thomas">
                                <img src="@/assets/images/users/avatar-8.jpg" alt="" class="rounded-circle avatar-xs">
                            </b-link>
                            <b-link href="javascript: void(0);" class="avatar-group-item" v-b-tooltip.hover
                                title="Herbert">
                                <img src="@/assets/images/users/avatar-2.jpg" alt="" class="rounded-circle avatar-xs">
                            </b-link>
                            <b-link class="avatar-group-item"
                                @click="modalShow = !modalShow">
                                <div class="avatar-xs">
                                    <div class="avatar-title rounded-circle">
                                        +
                                    </div>
                                </div>
                            </b-link>
                        </div>
                    </div>
                </b-row>
            </b-card-body>
        </b-card>

        <div class="tasks-board mb-3" id="kanbanboard">
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">Unassigned <b-badge tag="small" variant="success" class="align-bottom ms-1">2</b-badge></h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="unassigned-task" class="tasks">
                        <draggable :list="unassigned" class="dragArea" :group="{ name: 'todo' }">
                            <b-card no-body class="tasks-box" v-for="(data, index) of unassigned" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">To Do <b-badge tag="small" variant="secondary"
                                class="align-bottom ms-1">2</b-badge></h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="todo-task" class="tasks">
                        <draggable :list="todo" class="dragArea" group="todo">
                            <b-card no-body class="tasks-box" v-for="(data, index) of todo" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">Inprogress 
                            <b-badge tag="small" class="bg-warning align-bottom ms-1">2</b-badge>
                        </h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="inprogress-task" class="tasks">
                        <draggable :list="inprogress" class="dragArea" group="reviews">
                            <b-card no-body class="tasks-box" v-for="(data, index) of inprogress" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">In Reviews 
                            <b-badge tag="small" class="bg-info align-bottom ms-1">3</b-badge>
                        </h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="reviews-task" class="tasks">
                        <draggable :list="reviews" class="dragArea" group="reviews">
                            <b-card no-body class="tasks-box" v-for="(data, index) of reviews" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">Completed 
                            <b-badge tag="small" variant="success" class="align-bottom ms-1">1</b-badge></h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="completed-task" class="tasks">
                        <draggable :list="completed" class="dragArea" group="newData">
                            <b-card no-body class="tasks-box" v-for="(data, index) of completed" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
            <div class="tasks-list">
                <div class="d-flex mb-3">
                    <div class="flex-grow-1">
                        <h6 class="fs-13 text-uppercase mb-0">new <b-badge tag="small" variant="success" class="align-bottom ms-1">1</b-badge></h6>
                    </div>
                    <div class="flex-shrink-0">
                        <div class="dropdown card-header-dropdown">
                            <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <span class="fw-medium text-muted fs-13">Priority<i
                                        class="mdi mdi-chevron-down ms-1"></i></span>
                            </b-link>
                            <div class="dropdown-menu dropdown-menu-end">
                                <b-link class="dropdown-item" href="#">Priority</b-link>
                                <b-link class="dropdown-item" href="#">Date Added</b-link>
                            </div>
                        </div>
                    </div>
                </div>
                <div data-simplebar class="tasks-wrapper px-3 mx-n3">
                    <div id="new-task" class="tasks">
                        <draggable :list="newData" class="dragArea" group="newData">
                            <b-card no-body class="tasks-box" v-for="(data, index) of newData" :key="index">
                                <b-card-body>
                                    <div class="d-flex mb-2">
                                        <h6 class="fs-14 mb-0 flex-grow-1 text-truncate task-title">
                                            <router-link class="text-body d-block" to="/apps/tasks-details">{{ data.title }}</router-link>
                                        </h6>
                                        <div class="dropdown">
                                            <b-link href="javascript:void(0);" class="text-muted" id="dropdownMenuLink1"
                                                data-bs-toggle="dropdown" aria-expanded="false"><i
                                                    class="ri-more-fill"></i></b-link>
                                            <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                                                <li>
                                                    <router-link class="dropdown-item" to="/apps/tasks-details"><i
                                                            class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                                    </router-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" href="#"><i
                                                            class="ri-edit-2-line align-bottom me-2 text-muted"></i>
                                                        Edit</b-link>
                                                </li>
                                                <li>
                                                    <b-link class="dropdown-item" @click="deleteTask"><i
                                                            class="ri-delete-bin-5-line align-bottom me-2 text-muted"></i>
                                                        Delete</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                    <p class="text-muted">{{ data.description }}</p>
                                    <div class="mb-3">
                                        <div class="d-flex mb-1">
                                            <div class="flex-grow-1">
                                                <h6 class="text-muted mb-0"><span class="text-secondary">15%</span> of
                                                    100%</h6>
                                            </div>
                                            <div class="flex-shrink-0">
                                                <span class="text-muted">{{ data.date }}</span>
                                            </div>
                                        </div>
                                        <div class="progress rounded-3 progress-sm">
                                            <div class="progress-bar bg-danger" role="progressbar" style="width: 15%"
                                                aria-valuenow="15" aria-valuemin="0" aria-valuemax="100"></div>
                                        </div>
                                    </div>
                                    <div class="d-flex align-items-center">
                                        <div class="flex-grow-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary me-1"
                                                v-for="(item, index) of data.features" :key="index">{{item}}</b-badge>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <div class="avatar-group">
                                                <b-link href="javascript: void(0);" v-for="(item, index) of data.users"
                                                    :key="index" class="avatar-group-item" v-b-tooltip.hover
                                                    title="Alexis">
                                                    <img :src="item" alt="" class="rounded-circle avatar-xxs">
                                                </b-link>
                                            </div>
                                        </div>
                                    </div>
                                </b-card-body>
                                <b-card-footer class="border-top-dashed">
                                    <div class="d-flex">
                                        <div class="flex-grow-1">
                                            <h6 class="text-muted mb-0">#VL2436</h6>
                                        </div>
                                        <div class="flex-shrink-0">
                                            <ul class="link-inline mb-0">
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-eye-line align-bottom"></i> 04</b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-question-answer-line align-bottom"></i> 19
                                                    </b-link>
                                                </li>
                                                <li class="list-inline-item">
                                                    <b-link href="javascript:void(0)" class="text-muted"><i
                                                            class="ri-attachment-2 align-bottom"></i> 02</b-link>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </b-card-footer>
                            </b-card>
                        </draggable>
                    </div>
                </div>
                <div class="my-3">
                    <b-button variant="soft-info" class="w-100" @click="modalShow2 = !modalShow2">Add More</b-button>
                </div>
            </div>
        </div>


        <b-modal v-model="modalShow" header-class="p-3 bg-soft-warning" content-class="border-0" hide-footer
            title="Add Member" class="v-modal-custom">
            <b-form>
                <b-row class="g-3">
                    <b-col lg="12">
                        <label for="submissionidInput" class="form-label">Submission ID</label>
                        <input type="number" class="form-control" id="submissionidInput" placeholder="Submission ID">
                    </b-col>
                    <b-col lg="12">
                        <label for="profileimgInput" class="form-label">Profile Images</label>
                        <input class="form-control" type="file" id="profileimgInput">
                    </b-col>
                    <b-col lg="6">
                        <label for="firstnameInput" class="form-label">First Name</label>
                        <input type="text" class="form-control" id="firstnameInput" placeholder="Enter firstname">
                    </b-col>
                    <b-col lg="6">
                        <label for="lastnameInput" class="form-label">Last Name</label>
                        <input type="text" class="form-control" id="lastnameInput" placeholder="Enter lastname">
                    </b-col>
                    <b-col lg="12">
                        <label for="designationInput" class="form-label">Designation</label>
                        <input type="text" class="form-control" id="designationInput" placeholder="Designation">
                    </b-col>
                    <b-col lg="12">
                        <label for="titleInput" class="form-label">Title</label>
                        <input type="text" class="form-control" id="titleInput" placeholder="Title">
                    </b-col>
                    <b-col lg="6">
                        <label for="numberInput" class="form-label">Phone Number</label>
                        <input type="text" class="form-control" id="numberInput" placeholder="Phone number">
                    </b-col>
                    <b-col lg="6">
                        <label for="joiningdateInput" class="form-label">Joining Date</label>

                        <flat-pickr v-model="date" :config="config" placeholder="Select date" class="form-control">
                        </flat-pickr>
                    </b-col>
                    <b-col lg="12">
                        <label for="emailInput" class="form-label">Email ID</label>
                        <input type="email" class="form-control" id="emailInput" placeholder="Email">
                    </b-col>
                </b-row>
            </b-form>
            <div class="modal-footer v-modal-footer">
                <b-button type="button" variant="light" @click="modalShow = false"><i
                        class="ri-close-line align-bottom me-1"></i> Close</b-button>
                <b-button type="button" variant="success" id="addMember">Add Member</b-button>
            </div>
        </b-modal>

        <b-modal v-model="modalShow1" header-class="p-3 bg-soft-info" content-class="border-0" hide-footer
            title="Add Board" class="v-modal-custom" centered>
            <b-form action="#">
                <b-row>
                    <b-col lg="12">
                        <label for="boardName" class="form-label">Board Name</label>
                        <input type="text" class="form-control" id="boardName" placeholder="Enter board name">
                    </b-col>
                    <div class="mt-4">
                        <div class="hstack gap-2 justify-content-end">
                            <b-button type="button" variant="light" @click="modalShow1 = false">Close</b-button>
                            <b-button type="button" variant="success" id="addNewBoard">Add Board</b-button>
                        </div>
                    </div>
                </b-row>
            </b-form>
        </b-modal>

        <b-modal v-model="modalShow2" header-class="p-3 bg-soft-info" content-class="border-0" hide-footer
            title="Create New Task" class="v-modal-custom" size="lg" centered>
            <b-form action="#">
                <b-row class="g-3">
                    <b-col lg="12">
                        <label for="projectName" class="form-label">Project Name</label>
                        <input type="text" class="form-control" id="projectName" placeholder="Enter project name">
                    </b-col>
                    <b-col lg="12">
                        <label for="sub-tasks" class="form-label">Task Title</label>
                        <input type="text" class="form-control" id="sub-tasks" placeholder="Task title">
                    </b-col>
                    <b-col lg="12">
                        <label for="task-description" class="form-label">Task Description</label>
                        <textarea class="form-control" id="task-description" rows="3"></textarea>
                    </b-col>
                    <b-col lg="12">
                        <label for="formFile" class="form-label">Tasks Images</label>
                        <input class="form-control" type="file" id="formFile">
                    </b-col>
                    <b-col lg="12">
                        <label for="tasks-progress" class="form-label">Add Team Member</label>
                        <div data-simplebar style="height: 95px;">
                            <ul class="list-unstyled vstack gap-2 mb-0">
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value="" id="anna-adame">
                                        <label class="form-check-label d-flex align-items-center" for="anna-adame">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-1.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Anna Adame
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value="" id="frank-hook">
                                        <label class="form-check-label d-flex align-items-center" for="frank-hook">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Frank Hook
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value=""
                                            id="alexis-clarke">
                                        <label class="form-check-label d-flex align-items-center" for="alexis-clarke">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Alexis Clarke
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value=""
                                            id="herbert-stokes">
                                        <label class="form-check-label d-flex align-items-center" for="herbert-stokes">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-2.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Herbert Stokes
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value=""
                                            id="michael-morris">
                                        <label class="form-check-label d-flex align-items-center" for="michael-morris">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-7.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Michael Morris
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value=""
                                            id="nancy-martino">
                                        <label class="form-check-label d-flex align-items-center" for="nancy-martino">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-5.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Nancy Martino
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value=""
                                            id="thomas-taylor">
                                        <label class="form-check-label d-flex align-items-center" for="thomas-taylor">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Thomas Taylor
                                            </span>
                                        </label>
                                    </div>
                                </li>
                                <li>
                                    <div class="form-check d-flex align-items-center">
                                        <input class="form-check-input me-3" type="checkbox" value="" id="tonya-noble">
                                        <label class="form-check-label d-flex align-items-center" for="tonya-noble">
                                            <span class="flex-shrink-0">
                                                <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                    class="avatar-xxs rounded-circle" />
                                            </span>
                                            <span class="flex-grow-1 ms-2">
                                                Tonya Noble
                                            </span>
                                        </label>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </b-col>
                    <b-col lg="4">
                        <label for="due-date" class="form-label">Due Date</label>

                        <flat-pickr v-model="date1" placeholder="Select date" class="form-control">
                        </flat-pickr>
                    </b-col>
                    <b-col lg="4">
                        <label for="categories" class="form-label">Tags</label>
                        <input type="text" class="form-control" id="categories" placeholder="Enter tag">
                    </b-col>
                    <b-col lg="4">
                        <label for="tasks-progress" class="form-label">Tasks Progress</label>
                        <input type="text" class="form-control" maxlength="3" id="tasks-progress"
                            placeholder="Enter progress">
                    </b-col>
                    <div class="mt-4">
                        <div class="hstack gap-2 justify-content-end">
                            <b-button type="button" variant="light" @click="modalShow2 = false">Close</b-button>
                            <b-button type="button" variant="success" @click="addNewTask">Add Task</b-button>
                        </div>
                    </div>
                </b-row>
            </b-form>
        </b-modal>

        <b-modal v-model="modalShow3" id="deleteTask" modal-class="zoomIn" hide-footer class="v-modal-custom" centered>
            <div class="mt-2 text-center">
                <lottie class="avatar-xl" colors="primary:#f7b84b,secondary:#f06548" :options="defaultOptions"
                    :height="100" :width="100" />
                <div class="mt-4 pt-2 fs-15 mx-4 mx-sm-5">
                    <h4>Are you sure ?</h4>
                    <p class="text-muted mx-4 mb-0">Are you sure you want to remove this tasks ?</p>
                </div>
            </div>
            <div class="d-flex gap-2 justify-content-center mt-4 mb-2">
                <b-button type="button" variant="light" class="w-sm" data-bs-dismiss="modal">Close</b-button>
                <b-button type="button" variant="danger" class="w-sm" id="delete-record">Yes, Delete It!</b-button>
            </div>
        </b-modal>

    </Layout>
</template>