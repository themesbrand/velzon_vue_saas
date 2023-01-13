<script>
import Layout from "../../layouts/main.vue";
import appConfig from "../../../app.config";
import flatPickr from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";
import Swal from "sweetalert2";

export default {
    page: {
        title: "Starter",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            projectModal: false,
            taskModal: false,
            editFlag: null,
            searchQuery: null,
            status: null,
            todoList: [{
                'id': '1',
                "checkedElem": false,
                'todo': 'Added Email Templates',
                "assignedto": [{
                    "assigneeName": "Test 01",
                    "assigneeImg": require("@/assets/images/users/avatar-1.jpg"),
                }, {
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }
                ],
                'dueDate': '03 Apr, 2022',
                'status': 'Inprogress',
                "priority": "High"
            }, {
                'id': '2',
                "checkedElem": false,
                'todo': 'Additional Mailbox',
                "assignedto": [{
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }, {
                    "assigneeName": "Diego Norris",
                    "assigneeImg": require("@/assets/images/users/avatar-9.jpg"),
                }, {
                    "assigneeName": "Anthony Mills",
                    "assigneeImg": require("@/assets/images/users/avatar-10.jpg"),
                }
                ],
                'dueDate': '02 Apr, 2022',
                'status': 'Pending',
                "priority": "Medium"
            }, {
                'id': '3',
                "checkedElem": true,
                'todo': 'Make a creating an account profile',
                "assignedto": [{
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }, {
                    "assigneeName": "Marian Angel",
                    "assigneeImg": require("@/assets/images/users/avatar-6.jpg"),
                }, {
                    "assigneeName": "Johnnie Walton",
                    "assigneeImg": require("@/assets/images/users/avatar-7.jpg"),
                }, {
                    "assigneeName": "Donna Weston",
                    "assigneeImg": require("@/assets/images/users/avatar-8.jpg"),
                }
                ],
                'dueDate': '02 May, 2022',
                'status': 'Completed',
                "priority": "Low"
            }, {
                'id': '4',
                "checkedElem": false,
                'todo': 'Added new tabs styles',
                "assignedto": [{
                    "assigneeName": "James Forbes",
                    "assigneeImg": require("@/assets/images/users/avatar-2.jpg"),
                }
                ],
                'dueDate': '01 May, 2022',
                'status': 'New',
                "priority": "Low"
            }, {
                'id': '5',
                "checkedElem": false,
                'todo': 'Added bdge new style - gradient',
                "assignedto": [{
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }, {
                    "assigneeName": "Anthony Mills",
                    "assigneeImg": require("@/assets/images/users/avatar-10.jpg"),
                }, {
                    "assigneeName": "Diego Norris",
                    "assigneeImg": require("@/assets/images/users/avatar-9.jpg"),
                }
                ],
                'dueDate': '01 May, 2022',
                'status': 'Inprogress',
                "priority": "Medium"
            }, {
                'id': '6',
                "checkedElem": false,
                'todo': 'Added Back to Top button',
                "assignedto": [{
                    "assigneeName": "Marian Angel",
                    "assigneeImg": require("@/assets/images/users/avatar-6.jpg"),
                }, {
                    "assigneeName": "Johnnie Walton",
                    "assigneeImg": require("@/assets/images/users/avatar-7.jpg"),
                }
                ],
                'dueDate': '30 Apr, 2022',
                'status': 'Inprogress',
                "priority": "High"
            }, {
                'id': '7',
                "checkedElem": true,
                'todo': 'Added File Manager Apps',
                "assignedto": [{
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }, {
                    "assigneeName": "Mary Gant",
                    "assigneeImg": require("@/assets/images/users/avatar-4.jpg"),
                }, {
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }
                ],
                'dueDate': '29 Apr, 2022',
                'status': 'Completed',
                "priority": "Medium"
            }, {
                'id': '8',
                "checkedElem": false,
                'todo': 'Datatable with jQuery cdn',
                "assignedto": [{
                    "assigneeName": "Marian Angel",
                    "assigneeImg": require("@/assets/images/users/avatar-6.jpg"),
                }, {
                    "assigneeName": "Johnnie Walton",
                    "assigneeImg": require("@/assets/images/users/avatar-7.jpg"),
                }, {
                    "assigneeName": "Donna Weston",
                    "assigneeImg": require("@/assets/images/users/avatar-8.jpg"),
                }
                ],
                'dueDate': '28 Apr, 2022',
                'status': 'Pending',
                "priority": "High"
            }, {
                'id': '9',
                "checkedElem": false,
                'todo': 'Profile Page Structure',
                "assignedto": [{
                    "assigneeName": "Mary Gant",
                    "assigneeImg": require("@/assets/images/users/avatar-4.jpg"),
                }, {
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }
                ],
                'dueDate': '27 Apr, 2022',
                'status': 'New',
                "priority": "Low"
            }, {
                'id': '10',
                "checkedElem": true,
                'todo': 'Make a creating an account profile',
                "assignedto": [{
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }
                ],
                'dueDate': '26 Apr, 2022',
                'status': 'Completed',
                "priority": "Medium"
            }, {
                'id': '11',
                "checkedElem": true,
                'todo': 'Change email option process',
                "assignedto": [{
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }, {
                    "assigneeName": "Anthony Mills",
                    "assigneeImg": require("@/assets/images/users/avatar-10.jpg"),
                }, {
                    "assigneeName": "Diego Norris",
                    "assigneeImg": require("@/assets/images/users/avatar-9.jpg"),
                }
                ],
                'dueDate': '25 Apr, 2022',
                'status': 'Completed',
                "priority": "High"
            }, {
                'id': '12',
                "checkedElem": false,
                'todo': 'Brand Logo design',
                "assignedto": [{
                    "assigneeName": "James Forbes",
                    "assigneeImg": require("@/assets/images/users/avatar-2.jpg"),
                }, {
                    "assigneeName": "Anthony Mills",
                    "assigneeImg": require("@/assets/images/users/avatar-10.jpg"),
                }, {
                    "assigneeName": "Diego Norris",
                    "assigneeImg": require("@/assets/images/users/avatar-9.jpg"),
                }
                ],
                'dueDate': '25 Apr, 2022',
                'status': 'New',
                "priority": "Medium",
            }, {
                'id': '13',
                "checkedElem": false,
                'todo': 'Add Dynamic Contact List',
                "assignedto": [{
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }, {
                    "assigneeName": "Marian Angel",
                    "assigneeImg": require("@/assets/images/users/avatar-6.jpg"),
                }, {
                    "assigneeName": "Johnnie Walton",
                    "assigneeImg": require("@/assets/images/users/avatar-7.jpg"),
                }, {
                    "assigneeName": "Donna Weston",
                    "assigneeImg": require("@/assets/images/users/avatar-8.jpg"),
                }
                ],
                'dueDate': '24 Apr, 2022',
                'status': 'Inprogress',
                "priority": "Low"
            }, {
                'id': '14',
                "checkedElem": true,
                'todo': 'Additional Calendar',
                "assignedto": [{
                    "assigneeName": "Virgie Price",
                    "assigneeImg": require("@/assets/images/users/avatar-5.jpg"),
                }, {
                    "assigneeName": "Diego Norris",
                    "assigneeImg": require("@/assets/images/users/avatar-9.jpg"),
                }, {
                    "assigneeName": "Anthony Mills",
                    "assigneeImg": require("@/assets/images/users/avatar-10.jpg"),
                }
                ],
                'dueDate': '23 Apr, 2022',
                'status': 'Completed',
                "priority": "Medium",
            }, {
                'id': '15',
                "checkedElem": false,
                'todo': 'Added Select2',
                "assignedto": [{
                    "assigneeName": "Curtis Saenz",
                    "assigneeImg": require("@/assets/images/users/avatar-1.jpg"),
                }, {
                    "assigneeName": "John Robles",
                    "assigneeImg": require("@/assets/images/users/avatar-3.jpg"),
                }
                ],
                'dueDate': '23 Apr, 2022',
                'status': 'Pending',
                "priority": "High"
            }],
            value: null,
            statusvalue: null,
            priorityvalue: null,
            selectedimage: [],
            options: [
                { name: 'James Forbes', value: require('@/assets/images/users/avatar-2.jpg') },
                { name: 'John Robles', value: require('@/assets/images/users/avatar-3.jpg') },
                { name: 'Mary Gant', value: require('@/assets/images/users/avatar-4.jpg') },
                { name: 'Curtis Saenz', value: require('@/assets/images/users/avatar-1.jpg') },
                { name: 'Virgie Price', value: require('@/assets/images/users/avatar-5.jpg') },
                { name: 'Anthony Mills', value: require('@/assets/images/users/avatar-10.jpg') },
                { name: 'Marian Angel', value: require('@/assets/images/users/avatar-6.jpg') },
                { name: 'Johnnie Walton', value: require('@/assets/images/users/avatar-7.jpg') },
                { name: 'Donna Weston', value: require('@/assets/images/users/avatar-8.jpg') },
                { name: 'Diego Norris', value: require('@/assets/images/users/avatar-9.jpg') },
            ]
        };
    },
    components: {
        Layout,
        flatPickr,
        Multiselect
    },
    watch: {
        todoList() { },
        selectedimage() { },
    },
    computed: {
        resultQuery() {
            if (this.searchQuery) {
                const search = this.searchQuery.toLowerCase();
                return this.todoList.filter((data) => {
                    return data.priority.toLowerCase().includes(search) ||
                        data.id.toLowerCase().includes(search) ||
                        data.status.toLowerCase().includes(search) ||
                        data.todo.toLowerCase().includes(search) ||
                        data.dueDate.toLowerCase().includes(search);
                });
            } else if (this.status !== null) {
                return this.todoList.filter((data) => {
                    if (data.status === this.status || this.status == 'All Tasks') {
                        return data;
                    } else {
                        return null;
                    }
                });
            } else {
                return this.todoList;
            }
        }
    },
    methods: {
        deletedata(event) {
            Swal.fire({
                title: "Are you sure?",
                text: "You won't be able to revert this!",
                icon: "warning",
                showCancelButton: true,
                cancelButtonColor: "#f46a6a",
                confirmButtonColor: "#34c38f",
                confirmButtonText: "Yes, delete it!",
            }).then((result) => {
                if (result.value) {
                    this.todoList.splice(this.todoList.indexOf(event), 1);
                    Swal.fire("Deleted!", "Your file has been deleted.", "success");
                }
            });
        },
        create() {
            this.taskModal = true;
            document.querySelector(".task-modal").innerHTML = "Create Task";
            document.getElementById("addNewTodo").innerHTML = "Add Task";
            document.getElementById('task-title-input').value = '';
            document.getElementById('task-duedate-input').value = '';
            if (document.querySelector('.multiselect-single-label-text')) {
                document.querySelector('.multiselect-single-label-text').innerHTML = '';
                document.querySelector('.multiselect-clear').click();
            }
            this.selectedimage = [];
            this.value = null;

        },

        upsert() {
            if (document.querySelector(".task-modal").innerHTML == "Edit Task") {
                let result = this.todoList.findIndex(o => o.id == document.getElementById('taskid-input').value);
                this.todoList[result].todo = document.getElementById("task-title-input").value;
                this.todoList[result].dueDate = document.getElementById("task-duedate-input").value;
                var editimage = [];
                this.selectedimage.map(function (item) {
                    editimage.push({ assigneeImg: item });
                });
                this.todoList[result].assignedto = editimage;
                this.todoList[result].status = this.statusvalue;
                this.todoList[result].priority = this.priorityvalue ? this.priorityvalue : 'High';
                document.getElementById("createTaskBtn-close").click();
                document.getElementById('creattask-form').reset();
            } else {
                var title = document.getElementById("task-title-input").value;
                var date = document.getElementById("task-duedate-input").value;
                var createimage = [];
                this.selectedimage.map(function (item) {
                    createimage.push({ assigneeImg: item });
                });
                var status = this.statusvalue;
                var priority = this.priorityvalue ? this.priorityvalue : 'High';
                var id = this.todoList.length + 1;
                if (title == "" || date == "" || status == "" || priority == "" || title == null || date == null || status == null || priority == null) {
                    document.getElementById('task-error-msg').innerHTML = "please fill all detail";
                }
                else {
                    var data = {
                        id: id,
                        checkedElem: false,
                        todo: title,
                        assignedto: createimage,
                        dueDate: date,
                        status: status,
                        priority: priority

                    };
                    this.todoList.unshift(data);
                    document.getElementById("createTaskBtn-close").click();
                    document.getElementById('creattask-form').reset();
                    this.statusvalue = '';
                    this.priorityvalue = '';
                    this.date = '';
                    this.selectedimage = [];
                }
            }
        },
        onChange(selected) {
            this.selectedimage = [];
            var selected_images = [];
            selected.map(function (subItem) {
                selected_images.push(subItem);
            });
            this.selectedimage = selected_images;
        },
        editdata(item) {
            this.taskModal = true;
            this.value = null;
            this.selectedimage = [];
            document.querySelector(".task-modal").innerHTML = "Edit Task";
            document.getElementById("addNewTodo").innerHTML = "Save";
            document.getElementById("taskid-input").value = item.id;
            var editimage = [];
            item.assignedto.map(function (item) {
                editimage.push(item.assigneeImg ? item.assigneeImg : item);
            });
            this.selectedimage = editimage;
            document.getElementById("task-title-input").value = item.todo;
            document.getElementById("task-duedate-input").value = item.dueDate;
            this.statusvalue = item.status;
            this.priorityvalue = item.priority;

        },
        loadList() {
            document.getElementById("elmLoader").innerHTML = '';
        },
        load(manyTodos) {
            this.loadList(manyTodos);
        },
        fetchIdFromObj(todo) {
            return parseInt(todo.id);
        },
        sortElementsById() {
            var manyTodos = this.todoList.sort(function (a, b) {
                var x = parseInt(a.id);
                var y = parseInt(b.id);

                if (x > y) {
                    return -1;
                }
                if (x < y) {
                    return 1;
                }
                return 0;
            });
            this.load(manyTodos);
        },

        todoListStatus(e) {
            var todo = this.todoList;
            todo.filter(function (orders) {
                if (orders.id == e.target.id) {
                    if (orders.status == 'Completed') {
                        orders.status = 'Inprogress';
                    } else {
                        orders.status = 'Completed';
                    }
                }
            });
        }
    },
    mounted() {
        var addNewProject = document.getElementById('addNewProject');
        if (addNewProject) {
            document.getElementById("addNewProject").addEventListener("click", function () {
                var projectName = document.getElementById("projectname-input").value;
                var uniqueid = Math.floor(Math.random() * 100);
                const projectlisthtml =
                    '<li id="projectlist-' + uniqueid + '">\
                        <a data-bs-toggle="collapse" href="#projectCollapse-'+ uniqueid + '" class="nav-link fs-13">' + projectName + '</a>\
                        <div class="collapse" id="projectCollapse-'+ uniqueid + '">\
                            <ul class="mb-0 sub-menu list-unstyled ps-3 vstack gap-2 mb-2">\
                                <li>\
                                    <a href="#!"><i class="ri-stop-mini-fill align-middle fs-15 text-danger"></i> v1.0.0</a>\
                                </li>\
                            </ul>\
                        </div>\
                    </li>';

                if (projectName !== "") {
                    var projectListdata = document.getElementById("projectlist-data");
                    projectListdata.insertAdjacentHTML("beforeend", projectlisthtml);
                    var addProjectClose = document.getElementById("addProjectBtn-close");
                    addProjectClose.click();
                    document.getElementById('projectForm').reset();
                }
            });
        }
        this.sortElementsById();
    },

};
</script>
    
<template>
    <Layout>

        <div class="chat-wrapper d-lg-flex gap-1 mx-n4 mt-n4 p-1">
            <div class="file-manager-sidebar">
                <div class="p-4 d-flex flex-column h-100">
                    <div class="mb-3">
                        <b-button variant="info" class="w-100" @click="projectModal = !projectModal"><i
                                class="ri-add-line align-bottom"></i> Add Project</b-button>
                    </div>

                    <div class="px-4 mx-n4" data-simplebar style="height: calc(100vh - 468px);">
                        <ul class="to-do-menu list-unstyled" id="projectlist-data">
                            <li>
                                <b-link v-b-toggle.velzonAdmin class="nav-link fs-13 active">
                                    Velzon
                                    Admin & Dashboard</b-link>
                                <b-collapse id="velzonAdmin" visible>
                                    <ul class="mb-0 sub-menu list-unstyled ps-3 vstack gap-2 mb-2">
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-danger"></i>
                                                v1.4.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-secondary"></i>
                                                v1.5.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-info"></i>
                                                v1.6.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-primary"></i>
                                                v1.7.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-warning"></i>
                                                v1.8.0</b-link>
                                        </li>
                                    </ul>
                                </b-collapse>
                            </li>
                            <li>
                                <b-link v-b-toggle.projectManagement class="nav-link fs-13">
                                    Project
                                    Management</b-link>
                                <b-collapse id="projectManagement">
                                    <ul class="mb-0 sub-menu list-unstyled ps-3 vstack gap-2 mb-2">
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-danger"></i>
                                                v2.1.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-secondary"></i>
                                                v2.2.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-info"></i>
                                                v2.3.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-primary"></i>
                                                v2.4.0</b-link>
                                        </li>
                                    </ul>
                                </b-collapse>
                            </li>
                            <li>
                                <b-link v-b-toggle.skoteAdmin class="nav-link fs-13">Skote Admin
                                    &
                                    Dashboard</b-link>
                                <b-collapse id="skoteAdmin">
                                    <ul class="mb-0 sub-menu list-unstyled ps-3 vstack gap-2 mb-2">
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-danger"></i>
                                                v4.1.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-secondary"></i>
                                                v4.2.0</b-link>
                                        </li>
                                    </ul>
                                </b-collapse>
                            </li>
                            <li>
                                <b-link v-b-toggle.ecommerceProject class="nav-link fs-13">Doot -
                                    Chat
                                    App Template</b-link>
                                <b-collapse id="ecommerceProject">
                                    <ul class="mb-0 sub-menu list-unstyled ps-3 vstack gap-2 mb-2">
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-danger"></i>
                                                v1.0.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-secondary"></i>
                                                v1.1.0</b-link>
                                        </li>
                                        <li>
                                            <b-link href="#!"><i
                                                    class="ri-stop-mini-fill align-middle fs-15 text-info"></i>
                                                v1.2.0</b-link>
                                        </li>
                                    </ul>
                                </b-collapse>
                            </li>
                        </ul>
                    </div>


                    <div class="mt-auto text-center">
                        <img src="@/assets/images/task.png" alt="Task" class="img-fluid" />
                    </div>
                </div>
            </div>
            <!--end side content-->
            <div class="file-manager-content w-100 p-4 pb-0">
                <b-row class="mb-4">
                    <div class="col-auto order-1 d-block d-lg-none">
                        <button type="button" class="btn btn-soft-success btn-icon btn-sm fs-16 file-menu-btn">
                            <i class="ri-menu-2-fill align-bottom"></i>
                        </button>
                    </div>
                    <b-col order="3" order-sm="2" class="mt-3 mt-sm-0" sm>
                        <h5 class="fw-semibold mb-0">Velzon Admin & Dashboard <span
                                class="badge bg-primary align-bottom ms-2">v2.0.0</span></h5>
                    </b-col>

                    <div class="col-auto order-2 order-sm-3 ms-auto">
                        <div class="hstack gap-2">
                            <b-button-group>
                                <b-button variant="soft-danger" class="btn btn-icon fw-semibold"><i
                                        class="ri-arrow-go-back-line"></i></b-button>
                                <b-button variant="soft-success" class="btn btn-icon fw-semibold"><i
                                        class="ri-arrow-go-forward-line"></i></b-button>
                            </b-button-group>
                        </div>
                    </div>
                </b-row>
                <div class="p-3 bg-light rounded mb-4">
                    <b-row class="g-2">
                        <b-col lg="auto">
                            <select class="form-control" data-choices data-choices-search-false
                                name="choices-select-sortlist" id="choices-select-sortlist">
                                <option value="">Sort</option>
                                <option value="By ID">By ID</option>
                                <option value="By Name">By Name</option>
                            </select>
                        </b-col>
                        <b-col lg="auto">
                            <select class="form-control" data-choices data-choices-search-false
                                name="choices-select-status" id="choices-select-status" v-model="status">
                                <option value="All Tasks">All Tasks</option>
                                <option value="Completed">Completed</option>
                                <option value="Inprogress">Inprogress</option>
                                <option value="Pending">Pending</option>
                                <option value="New">New</option>
                            </select>
                        </b-col>
                        <b-col lg>
                            <div class="search-box">
                                <input type="text" id="searchTaskList" class="form-control search"
                                    placeholder="Search task name" v-model="searchQuery">
                                <i class="ri-search-line search-icon"></i>
                            </div>
                        </b-col>
                        <b-col lg="auto">
                            <!-- <b-button variant="primary" class="createTask" type="button" data-bs-toggle="modal"
                                data-bs-target="#createTask" @click="create">
                                <i class="ri-add-fill align-bottom"></i> Add Tasks
                            </b-button> -->
                            <b-button variant="primary" class="createTask" @click="create"> <i
                                    class="ri-add-fill align-bottom"></i> Add Tasks
                            </b-button>
                        </b-col>
                    </b-row>
                </div>

                <div class="todo-content position-relative px-4 mx-n4" id="todo-content">
                    <div id="elmLoader">
                        <div class="spinner-border text-primary avatar-sm" role="status">
                            <span class="visually-hidden">Loading...</span>
                        </div>
                    </div>
                    <div class="todo-task" id="todo-task">
                        <div class="table-responsive">
                            <table class="table align-middle position-relative table-nowrap">
                                <thead class="table-active">
                                    <tr>
                                        <th scope="col">Task Name</th>
                                        <th scope="col">Assigned</th>
                                        <th scope="col">Due Date</th>
                                        <th scope="col">Status</th>
                                        <th scope="col">Priority</th>
                                        <th scope="col">Action</th>
                                    </tr>
                                </thead>

                                <tbody id="task-lists">
                                    <tr v-for="(singleTodo, index) of this.resultQuery" :key="index">
                                        <td>
                                            <div class="d-flex align-items-start">
                                                <div class="flex-shrink-0 me-3">
                                                    <div class="task-handle px-1 bg-light rounded">: :</div>
                                                </div>
                                                <div class="flex-grow-1">
                                                    <div class="form-check">
                                                        <input class="form-check-input" type="checkbox"
                                                            :value="singleTodo.id" :id="singleTodo.id" checked
                                                            v-if="singleTodo.checkedElem"
                                                            @click="(e) => todoListStatus(e)">
                                                        <input class="form-check-input" type="checkbox"
                                                            :value="singleTodo.id" :id="singleTodo.id"
                                                            v-if="!singleTodo.checkedElem"
                                                            @click="(e) => todoListStatus(e)">
                                                        <label class="form-check-label ms-1" :for="singleTodo.id">
                                                            {{ singleTodo.todo }}</label>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                        <td>
                                            <div class="avatar-group">
                                                <span v-for="(img, index) of singleTodo.assignedto" :key="index">
                                                    <b-link href="javascript: void(0);" class="avatar-group-item"
                                                        data-img="{{img.assigneeImg}}" data-bs-toggle="tooltip"
                                                        data-bs-placement="top" title="">
                                                        <img :src="img.assigneeImg" alt=""
                                                            class="rounded-circle avatar-xxs" />
                                                    </b-link>
                                                </span>
                                            </div>
                                        </td>
                                        <td> {{ singleTodo.dueDate }} </td>
                                        <td v-if="singleTodo.status == 'Pending'"><b-badge variant="soft-warning"
                                                class="badge-soft-warning text-uppercase">{{ singleTodo.status }}
                                            </b-badge> </td>
                                        <td v-if="singleTodo.status == 'Inprogress'"><b-badge variant="soft-secondary"
                                                class="badge-soft-secondary text-uppercase">{{ singleTodo.status
}}
                                            </b-badge> </td>
                                        <td v-if="singleTodo.status == 'Completed'"><b-badge variant="soft-success"
                                                class="badge-soft-success text-uppercase">{{ singleTodo.status }}
                                            </b-badge> </td>
                                        <td v-if="singleTodo.status == 'New'"><b-badge variant="soft-info"
                                                class="badge-soft-info text-uppercase">{{ singleTodo.status }}
                                            </b-badge> </td>
                                        <td v-if="singleTodo.priority == 'High'"><b-badge variant="danger"
                                                class="text-uppercase">{{ singleTodo.priority }}</b-badge>
                                        </td>
                                        <td v-if="singleTodo.priority == 'Low'"><b-badge variant="success"
                                                class="text-uppercase">{{ singleTodo.priority }}</b-badge>
                                        </td>
                                        <td v-if="singleTodo.priority == 'Medium'"><b-badge
                                                class="bg-warning text-uppercase">{{ singleTodo.priority }}</b-badge>
                                        </td>
                                        <td>
                                            <div class="hstack gap-2">
                                                <b-button variant="soft-danger" size="sm" class="remove-list"
                                                    data-remove-id={{singleTodo.id}} @click="deletedata(singleTodo)"><i
                                                        class="ri-delete-bin-5-fill align-bottom"></i></b-button>
                                                <b-button variant="soft-primary" size="sm" class="edit-list"
                                                    data-edit-id={{singleTodo.id}} @click="editdata(singleTodo)"><i
                                                        class="ri-pencil-fill align-bottom"></i>
                                                </b-button>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                    <div class="py-4 mt-4 text-center" id="noresult" style="display: none;">
                        <lord-icon src="https://cdn.lordicon.com/msoeawqm.json" trigger="loop"
                            colors="primary:#405189,secondary:#0ab39c" style="width:72px;height:72px"></lord-icon>
                        <h5 class="mt-4">Sorry! No Result Found</h5>
                    </div>
                </div>

            </div>
        </div>

        <b-modal v-model="projectModal" hide-footer title="Create Project" class="v-modal-custom" modal-class="zoomIn"
            centered header-class="p-3 bg-soft-success">
            <b-form id="projectForm" autocomplete="off" class="needs-validation createProject-form" novalidate>
                <div class="mb-4">
                    <label for="projectname-input" class="form-label">Project Name</label>
                    <input type="text" class="form-control" id="projectname-input" autocomplete="off"
                        placeholder="Enter project name" required>
                    <div class="invalid-feedback">Please enter a project name</div>
                    <input type="hidden" class="form-control" id="projectid-input" value=""
                        placeholder="Enter project name">
                </div>
                <div class="hstack gap-2 justify-content-end">
                    <b-button type="button" variant="ghost-success" id="addProjectBtn-close"
                        @click="projectModal = false"><i class="ri-close-line align-bottom"></i> Close</b-button>
                    <b-button type="submit" variant="primary" id="addNewProject">Add Project
                    </b-button>
                </div>
            </b-form>
        </b-modal>

        <b-modal v-model="taskModal" hide-footer title="Create Task" title-class="task-modal" class="v-modal-custom"
            modal-class="zoomIn" centered header-class="p-3 bg-soft-success">
            <div id="task-error-msg" class="alert alert-danger py-2"></div>
            <b-form autocomplete="off" action="" id="creattask-form">
                <input type="hidden" id="taskid-input" class="form-control">
                <div class="mb-3">
                    <label for="task-title-input" class="form-label">Task Title</label>
                    <input type="text" id="task-title-input" class="form-control" placeholder="Enter task title">
                </div>
                <div class="mb-3 position-relative">
                    <label for="task-assign-input" class="form-label">Assigned To</label>
                    <div class="avatar-group justify-content-center" id="assignee-member">
                        <span v-for="(img, index) of selectedimage" :key="index">
                            <b-link href="javascript: void(0);" class="avatar-group-item mb-2" data-img="{{img}}"
                                data-bs-toggle="tooltip" data-bs-placement="top" title="{{img}}">
                                <img :src="img" alt="" class="rounded-circle avatar-xs" />
                            </b-link>
                        </span>
                    </div>
                    <Multiselect v-model="value" :options="options" mode="multiple" :multiple="true"
                        :close-on-select="false" :clear-on-select="false" :searchable="false" :create-option="true"
                        placeholder="Pick some" label="name" @input="onChange">
                        <template v-slot="{ values, isOpen }">
                            <span class="multiselect__single" v-if="values.length && !isOpen">Assigned
                                To<b>{{ values.length
}}</b> Members</span>
                        </template>
                    </Multiselect>
                </div>
                <b-row class="g-4 mb-3">
                    <b-col lg="6">
                        <label for="task-status" class="form-label">Status</label>
                        <Multiselect placeholder="select status" v-model="statusvalue"
                            :options="['New', 'Inprogress', 'Pending', 'Completed']" />
                    </b-col>

                    <b-col lg="6">
                        <label for="priority-field" class="form-label">Priority</label>
                        <Multiselect v-model="priorityvalue" placeholder="select priority"
                            :options="['High', 'Medium', 'Low']" />
                    </b-col>

                </b-row>
                <div class="mb-4">
                    <label for="task-duedate-input" class="form-label">Due Date:</label>
                    <flat-pickr placeholder="Due date" v-model="date" :config="timeConfig"
                        class="form-control flatpickr-input" id="task-duedate-input"></flat-pickr>
                </div>

                <div class="hstack gap-2 justify-content-end">
                    <b-button type="button" variant="ghost-success" id="createTaskBtn-close" @click="taskModal = false">
                        <i class="ri-close-fill align-bottom"></i> Close
                    </b-button>
                    <b-button type="button" variant="primary" id="addNewTodo" @click="upsert">Add
                        Task</b-button>
                </div>
            </b-form>
        </b-modal>
    </Layout>
</template>