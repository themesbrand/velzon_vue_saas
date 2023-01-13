<script>
import {
  CountTo
} from "vue3-count-to";
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";
import flatPickr from "vue-flatpickr-component";
import "flatpickr/dist/flatpickr.css";

import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";
import Swal from "sweetalert2";
import axios from 'axios';
import animationData from "@/components/widgets/msoeawqm.json";
import animationData1 from "@/components/widgets/gsqxdxog.json";
import Lottie from "@/components/widgets/lottie.vue";

export default {
  page: {
    title: "List View",
    meta: [{
      name: "description",
      content: appConfig.description
    }],
  },
  data() {
    return {
      title: "List View",
      items: [{
        text: "Tasks",
        href: "/",
      },
      {
        text: "List View",
        active: true,
      },
      ],
      taskListModal: false,
      date3: null,
      rangeDateconfig: {
        wrap: true, // set wrap to true only when using 'input-group'
        altFormat: "M j, Y",
        altInput: true,
        dateFormat: "d M, Y",
        mode: "range",
      },
      config: {
        wrap: true, // set wrap to true only when using 'input-group'
        altFormat: "M j, Y",
        altInput: true,
        dateFormat: "d M, Y",
      },
      timeConfig: {
        enableTime: false,
        dateFormat: "d M, Y",
      },
      filterdate: null,
      filterdate1: null,
      filtervalue: 'All',
      filtervalue1: 'All',
      filtersearchQuery1: null,
      date: null,
      allTask: [{
        id: 1,
        taskId: "#VLZ632",
        project: "Velzon - v1.0.0",
        task: "Error message when placing an orders?",
        creater: "Robert McMahon",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-3.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-1.jpg")
        },
        ],
        dueDate: "25 Jan, 2022",
        status: "Inprogress",
        statusClass: "secondary",
        priority: "High",
        priorityClass: "danger",
      },
      {
        id: 2,
        taskId: "#VLZ453",
        project: "Skote - v1.0.0",
        task: "Profile Page Satructure",
        creater: "Mary Cousar",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-10.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-9.jpg")
        },
        {
          id: 3,
          img: require("@/assets/images/users/avatar-5.jpg")
        },
        ],
        dueDate: "20 Dec, 2021",
        status: "New",
        statusClass: "info",
        priority: "Low",
        priorityClass: "success",
      },
      {
        id: 3,
        taskId: "#VLZ454",
        project: "Skote - v2.3.0",
        task: "Apologize for shopping Error!",
        creater: "Nathan Cole",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-5.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-6.jpg")
        },
        {
          id: 3,
          img: require("@/assets/images/users/avatar-7.jpg")
        },
        {
          id: 4,
          img: require("@/assets/images/users/avatar-8.jpg")
        },
        ],
        dueDate: "23 Oct, 2021",
        status: "Completed",
        statusClass: "success",
        priority: "Medium",
        priorityClass: "warning",
      },
      {
        id: 4,
        taskId: "#VLZ455",
        project: "Minia - v1.4.0",
        task: "Post launch reminder/ post list",
        creater: "Joseph Parker",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-2.jpg")
        },],
        dueDate: "05 Oct, 2021",
        status: "Pending",
        statusClass: "warning",
        priority: "High",
        priorityClass: "danger",
      },
      {
        id: 5,
        taskId: "#VLZ456",
        project: "Minia - v1.2.0",
        task: "Make a creating an account profile",
        creater: "Henry Baird",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-3.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-10.jpg")
        },
        {
          id: 3,
          img: require("@/assets/images/users/avatar-9.jpg")
        },
        ],
        dueDate: "17 Oct, 2021",
        status: "Inprogress",
        statusClass: "secondary",
        priority: "Medium",
        priorityClass: "warning",
      },
      {
        id: 6,
        taskId: "#VLZ657",
        project: "Minimal - v2.1.0",
        task: "Change email option process",
        creater: "Tonya Noble",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-6.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-7.jpg")
        },
        ],
        dueDate: "04 Dec, 2021",
        status: "Completed",
        statusClass: "success",
        priority: "High",
        priorityClass: "danger",
      },
      {
        id: 7,
        taskId: "#VLZ458",
        project: "Dason - v1.1.0",
        task: "User research",
        creater: "Donald Palmer",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-10.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-9.jpg")
        },
        {
          id: 3,
          img: require("@/assets/images/users/avatar-8.jpg")
        },
        {
          id: 4,
          img: require("@/assets/images/users/avatar-1.jpg")
        },
        ],
        dueDate: "11 Oct, 2021",
        status: "New",
        statusClass: "info",
        priority: "Low",
        priorityClass: "success",
      },
      {
        id: 8,
        taskId: "#VLZ459",
        project: "Dorsin - Landing Page",
        task: "Benner design for FB & Twitter",
        creater: "Carter",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-5.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-4.jpg")
        },
        ],
        dueDate: "16 Dec, 2021",
        status: "Pending",
        statusClass: "warning",
        priority: "Medium",
        priorityClass: "warning",
      },
      {
        id: 9,
        taskId: "#VLZ460",
        project: "Qexal - Landing Page",
        task: "Brand logo design",
        creater: "David Nichols",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-6.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-7.jpg")
        },
        {
          id: 3,
          img: require("@/assets/images/users/avatar-8.jpg")
        },
        ],
        dueDate: "29 Dec, 2021",
        status: "Pending",
        statusClass: "warning",
        priority: "High",
        priorityClass: "danger",
      },
      {
        id: 10,
        taskId: "#VLZ461",
        project: "Doot - Chat App Template",
        task: "Additional Calendar",
        creater: "Diana Kohler",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-4.jpg")
        },],
        dueDate: "13 Oct, 2021",
        status: "New",
        statusClass: "info",
        priority: "Low",
        priorityClass: "success",
      },
      {
        id: 11,
        taskId: "#VLZ462",
        project: "Skote - v2.1.0",
        task: "Edit customer testimonial",
        creater: "Nathan Cole",
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-7.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-8.jpg")
        },
        ],
        dueDate: "02 Jan, 2021",
        status: "Inprogress",
        statusClass: "secondary",
        priority: "Medium",
        priorityClass: "warning",
      },
      ],
      searchQuery: null,
      page: 1,
      perPage: 8,
      pages: [],
      defaultOptions: {
        animationData: animationData
      },
      defaultOptions1: {
        animationData: animationData1
      },
    };
  },
  components: {
    CountTo,
    Layout,
    PageHeader,
    lottie: Lottie,
    Multiselect,
    flatPickr,
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.allTask);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.taskId.toLowerCase().includes(search) ||
            data.task.toLowerCase().includes(search) ||
            data.project.toLowerCase().includes(search) ||
            data.creater.toLowerCase().includes(search) ||
            data.dueDate.toLowerCase().includes(search) ||
            data.status.toLowerCase().includes(search) ||
            data.priority.toLowerCase().includes(search)
          );
        });
      } else if (this.filterdate !== null) {
        if (this.filterdate !== null) {
          var date1 = this.filterdate.split(" to ")[0];
          var date2 = this.filterdate.split(" to ")[1];
        }
        return this.displayedPosts.filter((data) => {
          if (
            new Date(data.dueDate.slice(0, 12)) >= new Date(date1) &&
            new Date(data.dueDate.slice(0, 12)) <= new Date(date2)
          ) {
            return data;
          } else {
            return null;
          }
        });
      } else if (this.filtervalue !== null) {
        return this.displayedPosts.filter((data) => {
          if (data.status === this.filtervalue || this.filtervalue == 'All') {
            return data;
          } else {
            return null;
          }
        });
      } else {
        return this.displayedPosts;
      }
    },
  },
  watch: {
    allTask() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  filters: {
    trimWords(value) {
      return value.split(" ").splice(0, 20).join(" ") + "...";
    },
  },
  beforeMount() {
    axios.get('https://api-node.themesbrand.website/apps/task').then((data) => {
      this.allTask = [];
      const monthNames = ["Jan", "Feb", "Mar", "Apr", "May", "Jun", "Jul", "Aug", "Sep",
        "Oct", "Nov", "Dec"
      ];
      data.data.data.forEach(row => {
        var dd = new Date(row.dueDate);
        row.dueDate = dd.getDate() + " " + monthNames[dd.getMonth()] + ", " + dd.getFullYear();
        row.subItem.forEach(imag => {
          imag.image_src = 'https://api-node.themesbrand.website/images/users/' + imag.img;
        });

        // row.image_src = `@/assets/images/products/img-8.png`;
        // row.image_src = 'https://api-node.themesbrand.website/fileupload/users_bucket/' + row.img;
        this.allTask.push(row);
      });
    }).catch((er) => {
      console.log(er);
    });

  },

  methods: {
    SearchData() {
      this.filterdate = this.filterdate1;
      this.filtervalue = this.filtervalue1;
    },
    editdata(data) {
      this.taskListModal = true;
      document.querySelector('.taskModal').innerHTML = "<h5 class='fw-semibold mb-0'>Edit Task</h5>";
      document.getElementById('id').value = data._id;
      document.getElementById('projectName').value = data.project;
      document.getElementById('tasksTitle').value = data.task;
      document.getElementById('createName').value = data.creater;
      document.getElementById('date').value = data.dueDate;
      this.value1 = data.status;
      this.value3 = data.priority;
      document.getElementById('edit-btn').style.display = 'block';
      document.getElementById('add-btn').style.display = 'none';
    },
    updateorder() {
      let result = this.allTask.findIndex(o => o._id == document.getElementById('id').value);

      this.allTask[result].project = document.getElementById('projectName').value;
      this.allTask[result].task = document.getElementById('tasksTitle').value;
      this.allTask[result].creater = document.getElementById('createName').value;
      this.allTask[result].dueDate = document.getElementById('date').value;
      this.allTask[result].status = this.value1;
      this.allTask[result].priority = this.value3;
      document.getElementById('closemodal').click();
      axios.patch(`https://api-node.themesbrand.website/apps/task/${this.allTask[result]._id}`, this.allTask[result])
        .then(() => {

        }).catch((er) => {
          console.log(er);
        });
    },
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
          this.allTask.splice(this.allTask.indexOf(event), 1);
          axios.delete(`https://api-node.themesbrand.website/apps/task/${event._id}`)
            .then(() => {

            }).catch((er) => {
              console.log(er);
            });
          Swal.fire("Deleted!", "Your file has been deleted.", "success");
        }
      });
    },
    deleteMultiple() {
      let ids_array = [];
      var items = document.getElementsByName("chk_child");
      items.forEach(function (ele) {
        if (ele.checked == true) {
          var trNode = ele.parentNode.parentNode.parentNode;
          var id = trNode.querySelector(".id a").innerHTML;
          ids_array.push(id);
        }
      });
      if (typeof ids_array !== "undefined" && ids_array.length > 0) {
        if (confirm("Are you sure you want to delete this?")) {
          var cusList = this.allTask;
          ids_array.forEach(function (id) {
            cusList = cusList.filter(function (allTask) {
              return allTask.taskId != id;
            });
          });
          this.allTask = cusList;
          document.getElementById("checkAll").checked = false;
          var itemss = document.getElementsByName("chk_child");
          itemss.forEach(function (ele) {
            if (ele.checked == true) {
              ele.checked = false;
              ele.closest("tr").classList.remove("table-active");
            }
          });
        } else {
          return false;
        }
      } else {
        Swal.fire({
          title: "Please select at least one checkbox",
          confirmButtonClass: "btn btn-info",
          buttonsStyling: false,
          showCloseButton: true,
        });
      }
    },
    addorder() {
      var id = this.allTask.length + 1;
      var project = document.getElementById('projectName').value;
      var task = document.getElementById('tasksTitle').value;
      var creater = document.getElementById('createName').value;
      var dueDate = document.getElementById('date').value;
      var status = 'Inprogress';
      var priority = 'High';
      var statusClass = 'secondary';
      var priorityClass = 'danger';

      var data = {
        id: id,
        taskId: '#VZ1D24',
        project: project,
        task: task,
        creater: creater,
        dueDate: dueDate,
        status: status,
        priority: priority,
        statusClass: statusClass,
        priorityClass: priorityClass,
        subItem: [{
          id: 1,
          img: require("@/assets/images/users/avatar-3.jpg")
        },
        {
          id: 2,
          img: require("@/assets/images/users/avatar-1.jpg")
        },
        ],
      };
      this.allTask.unshift(data);
      axios.post(`https://api-node.themesbrand.website/apps/task`, data)
        .then(() => {

        }).catch((er) => {
          console.log(er);
        });
      document.getElementById('closemodal').click();
      document.getElementById("addform").reset();
    },
    addnew() {
      this.taskListModal = true;
      document.getElementById("addform").reset();
      document.querySelector('.taskModal').innerHTML = "<h5 class='fw-semibold mb-0'>Add Task</h5>";
      document.getElementById('add-btn').style.display = 'block';
      document.getElementById('edit-btn').style.display = 'none';
    },
    setPages() {
      let numberOfPages = Math.ceil(this.allTask.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(allTask) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return allTask.slice(from, to);
    },
  },
  mounted() {
    var checkAll = document.getElementById("checkAll");
    if (checkAll) {
      checkAll.onclick = function () {
        var checkboxes = document.querySelectorAll(
          '.form-check-all input[type="checkbox"]'
        );

        if (checkAll.checked == true) {
          checkboxes.forEach(function (checkbox) {
            checkbox.checked = true;
            checkbox.closest("tr").classList.add("table-active");
            document.getElementById('remove-actions').style.display = 'block';
          });
        } else {
          checkboxes.forEach(function (checkbox) {
            checkbox.checked = false;
            checkbox.closest("tr").classList.remove("table-active");
            document.getElementById('remove-actions').style.display = 'none';
          });
        }
      };
    }

    var checkboxes = document.querySelectorAll('#tasksTable .form-check-input');
    Array.from(checkboxes).forEach(function (element) {
      element.addEventListener('change', function (event) {
        var checkedCount = document.querySelectorAll('#tasksTable .form-check-input:checked').length;

        if (event.target.closest("tr").classList.contains("table-active")) {
          (checkedCount > 0) ? document.getElementById("remove-actions").style.display = 'block' : document.getElementById("remove-actions").style.display = 'none';
        } else {
          (checkedCount > 0) ? document.getElementById("remove-actions").style.display = 'block' : document.getElementById("remove-actions").style.display = 'none';
        }
      });
    });
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col xxl="3" sm="6">
        <b-card no-body class="card-animate">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Total Tasks</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal="0" :endVal="234" :duration="5000"></count-to>k
                </h2>
                <p class="mb-0 text-muted">
                  <b-badge class="bg-light text-success mb-0">
                    <i class="ri-arrow-up-line align-middle"></i> 17.32 %
                  </b-badge>
                  vs. previous month
                </p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-info text-info rounded-circle fs-4">
                    <i class="ri-ticket-2-line"></i>
                  </span>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xxl="3" sm="6">
        <b-card no-body class="card-animate">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Pending Tasks</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal="0" :endVal="64" :duration="5000"></count-to>k
                </h2>
                <p class="mb-0 text-muted">
                  <b-badge class="bg-light text-danger mb-0">
                    <i class="ri-arrow-down-line align-middle"></i> 0.87 %
                  </b-badge>
                  vs. previous month
                </p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-warning text-warning rounded-circle fs-4">
                    <i class="mdi mdi-timer-sand"></i>
                  </span>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xxl="3" sm="6">
        <b-card no-body class="card-animate">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Completed Tasks</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal="0" :endVal="116" :duration="5000"></count-to>K
                </h2>
                <p class="mb-0 text-muted">
                  <b-badge class="bg-light text-danger mb-0">
                    <i class="ri-arrow-down-line align-middle"></i> 2.52 %
                  </b-badge>
                  vs. previous month
                </p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-success text-success rounded-circle fs-4">
                    <i class="ri-checkbox-circle-line"></i>
                  </span>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xxl="3" sm="6">
        <b-card no-body class="card-animate">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Deleted Tasks</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal="0" :endVal="14" :duration="5000"></count-to>%
                </h2>
                <p class="mb-0 text-muted">
                  <b-badge class="bg-light text-success mb-0">
                    <i class="ri-arrow-up-line align-middle"></i> 0.63 %
                  </b-badge>
                  vs. previous month
                </p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-danger text-danger rounded-circle fs-4">
                    <i class="ri-delete-bin-line"></i>
                  </span>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <b-card no-body id="tasksList">
          <b-card-header class="border-0">
            <div class="d-flex align-items-center">
              <h5 class="card-title mb-0 flex-grow-1">All Tasks</h5>
              <div class="flex-shrink-0">
                <div class="d-flex flex-wrap gap-2">
                  <b-button variant="soft-danger" class="me-1" id="remove-actions" @click="deleteMultiple">
                    <i class="ri-delete-bin-2-line"></i>
                  </b-button>
                  <b-button variant="danger" class="add-btn" @click="addnew">
                    <i class="ri-add-line align-bottom me-1"></i> Create Task
                  </b-button>
                </div>
              </div>
            </div>
          </b-card-header>
          <b-card-body class="border border-dashed border-end-0 border-start-0">
            <b-form>
              <b-row class="g-3">
                <b-col xxl="5" sm="12">
                  <div class="search-box">
                    <input type="text" class="form-control search bg-light border-light"
                      placeholder="Search for tasks or something..." v-model="searchQuery" />
                    <i class="ri-search-line search-icon"></i>
                  </div>
                </b-col>

                <b-col xxl="3" sm="4">
                  <flat-pickr v-model="filterdate1" placeholder="Select date" :config="rangeDateconfig"
                    class="form-control"></flat-pickr>
                </b-col>

                <b-col xxl="3" sm="4">
                  <div class="input-light">
                    <Multiselect v-model="filtervalue1" :close-on-select="true" :searchable="true" :create-option="true"
                      :options="[
                        { value: 'All', label: 'All' },
                        { value: 'New', label: 'New' },
                        { value: 'Pending', label: 'Pending' },
                        { value: 'Inprogress', label: 'Inprogress' },
                        { value: 'Completed', label: 'Completed' },
                      ]" />
                  </div>
                </b-col>
                <b-col xxl="1" sm="4">
                  <b-button type="button" variant="primary" class="w-100" @click="SearchData">
                    <i class="ri-equalizer-fill me-1 align-bottom"></i>
                    Filters
                  </b-button>
                </b-col>
              </b-row>
            </b-form>
          </b-card-body>
          <b-card-body>
            <div class="table-responsive table-card mb-4">
              <table class="table align-middle table-nowrap mb-0" id="tasksTable">
                <thead class="table-light text-muted">
                  <tr>
                    <th scope="col" style="width: 40px">
                      <div class="form-check">
                        <input class="form-check-input" type="checkbox" id="checkAll" value="option" />
                      </div>
                    </th>
                    <th class="sort" data-sort="id">ID</th>
                    <th class="sort" data-sort="project_name">Project</th>
                    <th class="sort" data-sort="tasks_name">Task</th>
                    <th class="sort" data-sort="client_name">Created By</th>
                    <th class="sort" data-sort="assignedto">Assigned To</th>
                    <th class="sort" data-sort="due_date">Due Date</th>
                    <th class="sort" data-sort="status">Status</th>
                    <th class="sort" data-sort="priority">Priority</th>
                  </tr>
                </thead>
                <tbody class="list form-check-all">
                  <tr v-for="(task, index) of resultQuery" :key="index">
                    <th scope="row">
                      <div class="form-check">
                        <input class="form-check-input" type="checkbox" name="chk_child" value="option1" />
                      </div>
                    </th>
                    <td class="id">
                      <router-link to="/apps/tasks-details" class="fw-medium link-primary">{{ task.taskId }}
                      </router-link>
                    </td>
                    <td class="project_name">
                      <router-link to="/apps/projects-overview" class="fw-medium link-primary">{{ task.project }}
                      </router-link>
                    </td>
                    <td>
                      <div class="d-flex">
                        <div class="flex-grow-1 tasks_name">
                          {{ task.task }}
                        </div>
                        <div class="flex-shrink-0 ms-4">
                          <ul class="list-inline tasks-list-menu mb-0">
                            <li class="list-inline-item">
                              <router-link to="/apps/tasks-details"><i
                                  class="ri-eye-fill align-bottom me-2 text-muted"></i></router-link>
                            </li>
                            <li class="list-inline-item" @click="editdata(task)">
                              <b-link href="#"><i class="ri-pencil-fill align-bottom me-2 text-muted"></i></b-link>
                            </li>
                            <li class="list-inline-item">
                              <b-link class="remove-item-btn" @click="deletedata(task)">
                                <i class="ri-delete-bin-fill align-bottom me-2 text-muted"></i>
                              </b-link>
                            </li>
                          </ul>
                        </div>
                      </div>
                    </td>
                    <td class="client_name">{{ task.creater }}</td>
                    <td class="assignedto">
                      <div class="avatar-group">
                        <b-link href="javascript: void(0);" v-for="(task, index) of task.subItem" :key="index"
                          class="avatar-group-item" data-bs-toggle="tooltip" v-b-tooltip.hover title="Frank">
                          <img :src="task.image_src" alt="" class="rounded-circle avatar-xxs" />
                        </b-link>
                      </div>
                    </td>
                    <td class="due_date">{{ task.dueDate }}</td>
                    <td class="status">
                      <span class="badge" :class="{
                        'badge-soft-secondary': task.status == 'Inprogress',
                        'badge-soft-info': task.status == 'New',
                        'badge-soft-success': task.status == 'Completed',
                        'badge-soft-warning': task.status == 'Pending',
                      }">{{
    task.status
}}</span>
                    </td>
                    <td class="priority">
                      <span class="badge text-uppercase" :class="{
                        'bg-danger': task.priority == 'High',
                        'bg-success': task.priority == 'Low',
                        'bg-warning': task.priority == 'Medium',
                      }">{{ task.priority }}</span>
                    </td>
                  </tr>
                </tbody>
              </table>
              <div class="noresult" style="display: none">
                <div class="text-center">
                  <lottie colors="primary:#121331,secondary:#08a88a" :options="defaultOptions" :height="75"
                    :width="75" />
                  <h5 class="mt-2">Sorry! No Result Found</h5>
                  <p class="text-muted mb-0">
                    We've searched more than 200k+ tasks We did not find any
                    tasks for you search.
                  </p>
                </div>
              </div>
            </div>
            <div class="d-flex justify-content-end mt-3">
              <div class="pagination-wrap hstack gap-2">
                <b-link class="page-item pagination-prev disabled" href="#" v-if="page != 1" @click="page--">
                  Previous
                </b-link>
                <ul class="pagination listjs-pagination mb-0">
                  <li :class="{
                    active: pageNumber == page,
                    disabled: pageNumber == '...',
                  }" v-for="(pageNumber, index) in pages.slice(page - 1, page + 5)" :key="index"
                    @click="page = pageNumber">
                    <b-link class="page" href="#">{{ pageNumber }}</b-link>
                  </li>
                </ul>
                <b-link class="page-item pagination-next" href="#" @click="page++" v-if="page < pages.length"> Next
                </b-link>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-modal v-model="taskListModal" id="showmodal" modal-class="zoomIn" hide-footer
      header-class="p-3 bg-soft-info taskModal" class="v-modal-custom" centered size="lg" title="Add Task">
      <b-form id="addform" class="tablelist-form" autocomplete="off">
        <b-row class="g-3">
          <input type="hidden" id="id" name="">
          <b-col lg="12">
            <label for="projectName-field" class="form-label">Project Name</label>
            <input type="text" id="projectName" class="form-control" placeholder="Project name" required />
          </b-col>
          <b-col lg="12">
            <div>
              <label for="tasksTitle-field" class="form-label">Title</label>
              <input type="text" id="tasksTitle" class="form-control" placeholder="Title" required />
            </div>
          </b-col>
          <b-col lg="12">
            <label for="createName-field" class="form-label">Client Name</label>
            <input type="text" id="createName" class="form-control" placeholder="Client name" required />
          </b-col>
          <b-col lg="12">
            <label class="form-label">Assigned To</label>
            <div data-simplebar style="height: 95px">
              <ul class="list-unstyled vstack gap-2 mb-0">
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="anna-adame" />
                    <label class="form-check-label d-flex align-items-center" for="anna-adame">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-1.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2"> Anna Adame </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="frank-hook" />
                    <label class="form-check-label d-flex align-items-center" for="frank-hook">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-3.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2"> Frank Hook </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="alexis-clarke" />
                    <label class="form-check-label d-flex align-items-center" for="alexis-clarke">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-6.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2">
                        Alexis Clarke
                      </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="herbert-stokes" />
                    <label class="form-check-label d-flex align-items-center" for="herbert-stokes">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-2.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2">
                        Herbert Stokes
                      </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="michael-morris" />
                    <label class="form-check-label d-flex align-items-center" for="michael-morris">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-7.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2">
                        Michael Morris
                      </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="nancy-martino" />
                    <label class="form-check-label d-flex align-items-center" for="nancy-martino">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-5.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2">
                        Nancy Martino
                      </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="thomas-taylor" />
                    <label class="form-check-label d-flex align-items-center" for="thomas-taylor">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-8.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2">
                        Thomas Taylor
                      </span>
                    </label>
                  </div>
                </li>
                <li>
                  <div class="form-check d-flex align-items-center">
                    <input class="form-check-input me-3" type="checkbox" value="" id="tonya-noble" />
                    <label class="form-check-label d-flex align-items-center" for="tonya-noble">
                      <span class="flex-shrink-0">
                        <img src="@/assets/images/users/avatar-10.jpg" alt="" class="avatar-xxs rounded-circle" />
                      </span>
                      <span class="flex-grow-1 ms-2"> Tonya Noble </span>
                    </label>
                  </div>
                </li>
              </ul>
            </div>
          </b-col>
          <b-col lg="6">
            <label for="duedate-field" class="form-label">Due Date</label>
            <flat-pickr placeholder="Select date" v-model="date2" :config="timeConfig"
              class="form-control flatpickr-input" id="date"></flat-pickr>
          </b-col>
          <b-col lg="6">
            <label for="ticket-status" class="form-label">Status</label>
            <Multiselect id="statusid" v-model="value1" :close-on-select="true" :searchable="true" :create-option="true"
              :options="[
                { value: '', label: 'Status' },
                { value: 'New', label: 'New' },
                { value: 'Inprogress', label: 'Inprogress' },
                { value: 'Pending', label: 'Pending' },
                { value: 'Completed', label: 'Completed' },
              ]" />
          </b-col>
          <b-col lg="12">
            <label for="priority-field" class="form-label">Priority</label>

            <Multiselect id="priority" v-model="value3" :close-on-select="true" :searchable="true" :create-option="true"
              :options="[
                { value: '', label: 'Priority' },
                { value: 'High', label: 'High' },
                { value: 'Medium', label: 'Medium' },
                { value: 'Low', label: 'Low' },
              ]" />
          </b-col>
        </b-row>

        <div class="hstack gap-2 justify-content-end mt-3">
          <b-button type="button" variant="light" @click="taskListModal = false" id="closemodal"> Close </b-button>
          <b-button type="submit" variant="success" id="add-btn" @click="addorder"> Add Task </b-button>
          <b-button type="button" variant="success" id="edit-btn" @click="updateorder">Update</b-button>
        </div>
      </b-form>
    </b-modal>
  </Layout>
</template>