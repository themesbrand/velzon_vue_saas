<script>
function getChartColorsArray(colors) {
  colors = JSON.parse(colors);
  return colors.map(function (value) {
    var newValue = value.replace(" ", "");
    if (newValue.indexOf(",") === -1) {
      var color = getComputedStyle(document.documentElement).getPropertyValue(newValue);
      if (color) {
        color = color.replace(" ", "");
        return color;
      } else return newValue;
    } else {
      var val = value.split(',');
      if (val.length == 2) {
        var rgbaColor = getComputedStyle(document.documentElement).getPropertyValue(val[0]);
        rgbaColor = "rgba(" + rgbaColor + "," + val[1] + ")";
        return rgbaColor;
      } else {
        return newValue;
      }
    }
  });
}
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";

export default {
  page: {
    title: "Job Lists",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Job Lists",
      items: [
        {
          text: "Jobs",
          href: "/",
        },
        {
          text: "Job Lists",
          active: true,
        },
      ],
      createJobModal: false,
      searchQuery: null,
      jobvalue: null,
      tagvalue: null,
      tagoption: [{
        value: 'Design',
        label: 'Design'
      },
      {
        value: 'Remote',
        label: 'Remote'
      },
      {
        value: 'UI/UX Designer',
        label: 'UI/UX Designer'
      },
      {
        value: 'Designer',
        label: 'Designer'
      },
      ],
      page: 1,
      perPage: 3,
      pages: [],
      joblist: [
        {
          id: "1",
          img: require("@/assets/images/small/img-2.jpg"),
          logo: require("@/assets/images/companies/img-3.png"),
          designation: "UI/UX designer",
          name: "Nesta Technologies",
          description: "A UI/UX designer's job is to create user-friendly interfaces that enable users to understand how to use complex technical products. If you're passionate about the latest technology trends and devices, you'll find great fulfillment in being involved in the design process for the next hot gadget.",
          tags: ["Design", "Remote", "UI/UX Designer", "Designer"],
          type: "Full Time",
          experience: "2 Year",
          location: "Escondido, California",
          applied: "640 Applied",
          postDate: "11 Sep, 2022"
        }, {
          id: "2",
          img: require("@/assets/images/small/img-4.jpg"),
          logo: require("@/assets/images/companies/img-4.png"),
          designation: "Marketing Director",
          name: "Meta4Systems",
          description: "These cases are perfectly simple and easy to distinguish. In a free hour, when our power of choice is untrammelled and when nothing prevents to do what we like best, every pleasure is to be welcomed and every pain avoided. No one rejects, dislikes, or avoids pleasure itself, because it is pleasure.",
          tags: ["Design", "Remote", "UI/UX Designer", "Designer"],
          type: "Intership",
          experience: "Fresher",
          location: "Vinninga, Sweden",
          applied: "134 Applied",
          postDate: "13 Sep, 2022"
        }, {
          id: "3",
          img: require("@/assets/images/small/img-7.jpg"),
          logo: require("@/assets/images/companies/img-5.png"),
          designation: "Product Sales Specialist",
          name: "Digitech Galaxy",
          description: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit.",
          tags: ["Design", "Remote", "UI/UX Designer", "Designer"],
          type: "Part Time",
          experience: "0 - 5 Year",
          location: "Cullera, Spain",
          applied: "79 Applied",
          postDate: "14 Sep, 2022"
        }, {
          id: "4",
          img: require("@/assets/images/small/img-3.jpg"),
          logo: require("@/assets/images/companies/img-6.png"),
          designation: "Project Manager",
          name: "Syntyce Solutions",
          description: "In a free hour, when our power of choice is untrammelled and when nothing prevents our being able to do what we like best. But in certain circumstances and owing to the claims of duty or the obligations of business it will frequently occur that pleasures have to be repudiated.",
          tags: ["Design", "Remote", "UI/UX Designer", "Designer"],
          type: "Freelance",
          experience: "1 Year",
          location: "Stordorf, Germany",
          applied: "36 Applied",
          postDate: "14 Sep, 2022"
        }, {
          id: "5",
          img: require("@/assets/images/small/img-8.jpg"),
          logo: require("@/assets/images/companies/img-7.png"),
          designation: "Product Designer",
          name: "Themesbrand",
          description: "A UI/UX designer's job is to create user-friendly interfaces that enable users to understand how to use complex technical products. If you're passionate about the latest technology trends and devices, you'll find great fulfillment in being involved in the design process for the next hot gadget.",
          tags: ["Design", "Remote", "UI/UX Designer", "Designer"],
          type: "Full Time",
          experience: "1 - 2 Year",
          location: "United Kingdom",
          applied: "74 Applied",
          postDate: "15 Sep, 2022"
        }
      ],

      series: [98, 63, 35],
      chartOptions: {
        labels: ["New Application", "Approved", "Rejected"],
        chart: {
          height: 300,
          type: "donut",
        },
        legend: {
          position: "bottom",
        },
        stroke: {
          show: false,
        },
        dataLabels: {
          dropShadow: {
            enabled: false,
          },
        },
        colors: getChartColorsArray('["--vz-info", "--vz-primary", "--vz-danger", "--vz-danger", "--vz-info"]'),
      },
    };
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.joblist);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.designation.toLowerCase().includes(search) ||
            data.name.toLowerCase().includes(search) ||
            data.description.toLowerCase().includes(search) ||
            data.type.toLowerCase().includes(search) ||
            data.experience.toLowerCase().includes(search) ||
            data.location.toLowerCase().includes(search)
          );
        });
      } else {
        return this.displayedPosts;
      }
    },
  },

  watch: {
    joblist() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  methods: {
    showdetail(data) {
      document.getElementById('cover-img').setAttribute('src', data.img);
      document.querySelector('.view-companylogo').setAttribute('src', data.logo);
      document.querySelector('.view-title').innerHTML = data.designation;
      document.querySelector('.view-companyname').innerHTML = data.name;
      document.querySelector('.view-location').innerHTML = data.location;
      document.querySelector('.view-desc').innerHTML = data.description;
      document.querySelector('.view-type').innerHTML = data.type;
      document.querySelector('.view-postdate').innerHTML = data.postDate;
      document.querySelector('.view-experience').innerHTML = data.experience;
    },
    addorder() {
      var id = this.joblist.length + 1;
      var jobtitle = document.getElementById('jobtitle-field').value;
      var companyname = document.getElementById('companyname-field').value;
      var experience = document.getElementById('experience-field').value;
      var location = document.getElementById('location-field').value;
      var Salary = document.getElementById('Salary-field').value;
      var description = document.getElementById('description-field').value;

      if (id != null && jobtitle != null && companyname != null && experience != null && location != null && Salary !=
        null && description != null) {
        var data = {
          id: id,
          img: require("@/assets/images/small/img-9.jpg"),
          logo: require("@/assets/images/users/multi-user.jpg"),
          designation: jobtitle,
          name: companyname,
          experience: `${experience} Year`,
          location: location,
          description: description,
          type: (this.jobvalue || "Full Time"),
          applied: "0 Applied",
          postDate: new Date().toUTCString().slice(5, 16),
          tags: this.tagvalue,
        };
        document.getElementById("close-jobListModal").click();
        this.joblist.unshift(data);
      }
      document.getElementById('edtclosemodal').click();
      document.getElementById("createjobform").reset();
    },
    setPages() {
      let numberOfPages = Math.ceil(this.joblist.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(joblist) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return joblist.slice(from, to);
    }
  },
  components: {
    Layout,
    PageHeader,
    Multiselect
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col lg="12">
        <b-card no-body>
          <b-card-body>
            <div class="d-flex align-items-center">
              <h6 class="card-title mb-0 flex-grow-1">Search Jobs</h6>
              <div class="flex-shrink-0">
                <b-button variant="primary" @click="createJobModal = !createJobModal"><i
                    class="ri-add-line align-bottom me-1"></i> Create New Job</b-button>
              </div>
            </div>

            <b-row class="mt-3 gy-3">
              <b-col xxl="10" md="6">
                <div class="search-box">
                  <input type="text" class="form-control search bg-light border-light" id="searchJob" autocomplete="off"
                    placeholder="Search for jobs or companies..." v-model="searchQuery">
                  <i class="ri-search-line search-icon"></i>
                </div>
              </b-col>
              <b-col xxl="2" md="6">
                <div class="input-light">
                  <select class="form-control" data-choices data-choices-search-false name="choices-single-default"
                    id="idStatus">
                    <option value="All">All Selected</option>
                    <option value="Newest" selected>Newest</option>
                    <option value="Popluar">Popluar</option>
                    <option value="Oldest">Oldest</option>
                  </select>
                </div>
              </b-col>
              <b-col xl="12" id="found-job-alert" v-if="resultQuery >= 0">
                <div class="alert alert-success mb-0 text-center" role="alert">
                  <strong id="total-result">{{ resultQuery.length }}</strong> jobs found
                </div>
              </b-col>
            </b-row>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col xxl="9">
        <div id="job-list">
          <b-card no-body class="joblist-card" v-for="(data, index) of resultQuery" :key="index">
            <b-card-body>
              <div class="d-flex mb-4">
                <div class="avatar-sm">
                  <div class="avatar-title bg-light rounded"> <img :src="data.logo" alt=""
                      class="avatar-xxs companyLogo-img"> </div>
                </div>
                <div class="ms-3 flex-grow-1"> <img :src="data.img" alt="" class="d-none cover-img">
                  <b-link href="#!">
                    <h5 class="job-title">{{ data.designation }}</h5>
                  </b-link>
                  <p class="company-name text-muted mb-0">{{ data.name }}</p>
                </div>
                <div>
                  <b-button type="button" variant="ghost-primary" class="btn-icon custom-toggle"
                    data-bs-toggle="button">
                    <span class="icon-on"><i class="ri-bookmark-line"></i></span>
                    <span class="icon-off"><i class="ri-bookmark-fill"></i></span>
                  </b-button>
                </div>
              </div>
              <p class="text-muted job-description">{{ data.description }}</p>
              <div>
                <span v-for="(tag, index) of data.tags" :key="index">
                  &nbsp;<b-badge variant="soft-primary" class="badge-soft-primary me-1"> {{ tag }}</b-badge>
                </span>
              </div>
            </b-card-body>
            <b-card-footer class="border-top-dashed">
              <div class="d-flex justify-content-between align-items-center flex-wrap gap-3">
                <div><i class="ri-briefcase-2-line align-bottom me-1"></i> <span class="job-type">{{ data.type }}</span>
                </div>
                <div class="d-none"><span class="job-experience">{{ data.experience }}</span></div>
                <div><i class="ri-map-pin-2-line align-bottom me-1"></i> <span class="job-location">{{ data.location
                }}</span></div>
                <div><i class="ri-user-3-line align-bottom me-1"></i> {{ data.applied }}</div>
                <div><i class="ri-time-line align-bottom me-1"></i> <span class="job-postdate">{{ data.postDate
                }}</span>
                </div>
                <div>
                  <b-link href="#!" class="btn btn-primary viewjob-list" @click="showdetail(data)">View More <i
                      class="ri-arrow-right-line align-bottom ms-1"></i></b-link>
                </div>
              </div>
            </b-card-footer>
          </b-card>

        </div>
        <b-row class="g-0 justify-content-end mb-4" id="pagination-element">
          <b-col sm="6">
            <div
              class="pagination-block pagination pagination-separated justify-content-center justify-content-sm-end mb-sm-0"
              v-if="pages.length > 1">
              <div class="page-item">
                <b-link href="#" class="page-link" id="page-prev" v-if="page != 1" @click="page--">Previous</b-link>
              </div>
              <span id="page-num" class="pagination">
                <div class="page-item" :class="{ active: pageNumber == page, disabled: pageNumber == '...', }"
                  v-for="(pageNumber, index) in pages" :key="index" @click="page = pageNumber">
                  <b-link class="page-link clickPageNumber" href="javascript:void(0);">{{ pageNumber }}</b-link>
                </div>
              </span>
              <div class="page-item">
                <b-link href="#" class="page-link" id="page-next" @click="page++" v-if="page < pages.length">Next
                </b-link>
              </div>
            </div>
          </b-col>
        </b-row>
      </b-col>

      <b-col xxl="3">
        <b-card no-body class="job-list-view-card overflow-hidden" id="job-overview">
          <img src="@/assets/images/small/img-10.jpg" alt="" id="cover-img" class="img-fluid background object-cover">
          <b-card-body>
            <div class="avatar-md mt-n5">
              <div class="avatar-title bg-light rounded-circle">
                <img src="@/assets/images/companies/img-7.png" alt="" class="avatar-xs view-companylogo">
              </div>
            </div>
            <div class="mt-3">
              <h5 class="view-title">Product Designer</h5>
              <div class="hstack gap-3 mb-3">
                <span class="text-muted"><i class="ri-building-line me-1 align-bottom"></i> <span
                    class="view-companyname">Themesbrand</span></span>
                <span class="text-muted"><i class="ri-map-pin-2-line me-1 align-bottom"></i> <span
                    class="view-location">United Kingdom</span></span>
              </div>
              <p class="text-muted view-desc">A UI/UX designer's job is to create user-friendly interfaces that enable
                users to understand how to use complex technical products. If you're passionate about the latest
                technology trends and devices, you'll find great fulfillment in being involved in the design process for
                the next hot gadget.</p>
              <div class="py-3 border border-dashed border-start-0 border-end-0 mt-4">
                <b-row>
                  <b-col lg="4" sm="6">
                    <div>
                      <p class="mb-2 text-uppercase fw-medium fs-12 text-muted">Job Type</p>
                      <h5 class="fs-14 mb-0 view-type">Full Time</h5>
                    </div>
                  </b-col>
                  <b-col lg="4" sm="6">
                    <div>
                      <p class="mb-2 text-uppercase fw-medium fs-12 text-muted">Post Date</p>
                      <h5 class="fs-14 mb-0 view-postdate">15 Sep, 2022</h5>
                    </div>
                  </b-col>
                  <b-col lg="4" sm="6">
                    <div>
                      <p class="mb-2 text-uppercase fw-medium fs-12 text-muted">Experience</p>
                      <h5 class="fs-14 mb-0 view-experience">0 - 5 Year</h5>
                    </div>
                  </b-col>
                </b-row>
              </div>
            </div>

            <div class="mt-4">
              <h5 class="mb-3">Application Summary</h5>

              <div>
                <apexchart class="apex-charts" dir="ltr" height="260px" :series="series" :options="chartOptions">
                </apexchart>
              </div>
            </div>
            <div class="mt-4">
              <b-button type="button" variant="success" class="w-100">Apply Now</b-button>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <!-- create job modal  -->
    <b-modal v-model="createJobModal" id="CreateJobModal" hide-footer hide-header class="v-modal-custom" centered
      no-close-on-backdrop>
      <b-form id="createjobform" autocomplete="off" class="needs-validation" novalidate>
        <input type="hidden" id="id-field" />
        <b-row class="g-3">
          <b-col lg="12">
            <div class="px-1 pt-1">
              <div class="modal-team-cover position-relative mb-0 mt-n4 mx-n4 rounded-top overflow-hidden">
                <img src="@/assets/images/small/img-9.jpg" alt="" id="modal-cover-img" class="img-fluid">

                <div class="d-flex position-absolute start-0 end-0 top-0 p-3">
                  <div class="flex-grow-1">
                    <h5 class="modal-title text-white" id="exampleModalLabel">Create New Job</h5>
                  </div>
                  <div class="flex-shrink-0">
                    <div class="d-flex gap-3 align-items-center">
                      <div>
                        <label for="cover-image-input" class="mb-0" data-bs-toggle="tooltip" data-bs-placement="top"
                          title="Select Cover Image">
                          <div class="avatar-xs">
                            <div class="avatar-title bg-light border rounded-circle text-muted cursor-pointer">
                              <i class="ri-image-fill"></i>
                            </div>
                          </div>
                        </label>
                        <input class="form-control d-none" value="" id="cover-image-input" type="file"
                          accept="image/png, image/gif, image/jpeg">
                      </div>
                      <button type="button" class="btn-close btn-close-white" id="close-jobListModal"
                        @click="createJobModal = false"></button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="text-center mb-4 mt-n5 pt-2">
              <div class="position-relative d-inline-block">
                <div class="position-absolute bottom-0 end-0">
                  <label for="companylogo-image-input" class="mb-0" data-bs-toggle="tooltip" data-bs-placement="right"
                    title="Select Image">
                    <div class="avatar-xs cursor-pointer">
                      <div class="avatar-title bg-light border rounded-circle text-muted">
                        <i class="ri-image-fill"></i>
                      </div>
                    </div>
                  </label>
                  <input class="form-control d-none" value="" id="companylogo-image-input" type="file"
                    accept="image/png, image/gif, image/jpeg">
                </div>
                <div class="avatar-lg p-1">
                  <div class="avatar-title bg-light rounded-circle">
                    <img src="@/assets/images/users/multi-user.jpg" id="companylogo-img"
                      class="avatar-md rounded-circle object-cover" />
                  </div>
                </div>
              </div>
              <h5 class="fs-13 mt-3">Company Logo</h5>
            </div>
            <div>
              <label for="jobtitle-field" class="form-label">Job Title</label>
              <input type="text" id="jobtitle-field" class="form-control" placeholder="Enter job title" required />
            </div>
          </b-col>
          <b-col lg="6">
            <div>
              <label for="companyname-field" class="form-label">Company Name</label>
              <input type="text" id="companyname-field" class="form-control" placeholder="Enter company name"
                required />
            </div>
          </b-col>
          <b-col lg="6">
            <div>
              <label for="job_type-field" class="form-label">Job Type</label>

              <Multiselect v-model="jobvalue" placeholder="Select Job Type"
                :options="['Full Time', 'Part Time', 'Freelance', 'Intership']" />
            </div>
          </b-col>
          <b-col lg="4">
            <div>
              <label for="experience-field" class="form-label">Experience</label>
              <input type="text" id="experience-field" class="form-control" placeholder="Enter experience" required />
            </div>
          </b-col>
          <b-col lg="4">
            <div>
              <label for="location-field" class="form-label">Location</label>
              <input type="text" id="location-field" class="form-control" placeholder="Enter location" required />
            </div>
          </b-col>
          <b-col lg="4">
            <div>
              <label for="Salary-field" class="form-label">Salary</label>
              <input type="number" id="Salary-field" class="form-control" placeholder="Enter salary" required />
            </div>
          </b-col>
          <b-col lg="12">
            <div>
              <label for="website-field" class="form-label">Tags</label>
              <Multiselect v-model="tagvalue" mode="tags" :close-on-select="true" :searchable="true"
                id="taginput-choices" :create-option="false" :options="tagoption" />
            </div>
          </b-col>
          <b-col lg="12">
            <div>
              <label for="description-field" class="form-label">Description</label>
              <textarea class="form-control" id="description-field" rows="3" placeholder="Enter description"
                required></textarea>
            </div>
          </b-col>
        </b-row>
        <div class="hstack gap-2 justify-content-end mt-3">
          <b-button type="button" variant="light" @click="createJobModal = false" id="edtclosemodal">Close</b-button>
          <b-button type="button" variant="success" id="add-btn" @click="addorder">Add Job</b-button>
        </div>
      </b-form>
    </b-modal>
  </Layout>
</template>