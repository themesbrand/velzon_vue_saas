<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

export default {
  page: {
    title: "List View",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "List View",
      items: [
        {
          text: "Candidate Lists",
          href: "/",
        },
        {
          text: "List View",
          active: true,
        },
      ],
      searchQuery: null,
      page: 1,
      perPage: 8,
      pages: [],
      candidatelist: [
        {
          id: "1",
          img: require("@/assets/images/users/avatar-10.jpg"),
          name: "Tonya Noble",
          designation: "Web Designer",
          location: "Cullera, Spain",
          type: "Part Time",
          rating: "4.2",
          ratingCount: "2.2k",
          bookmark: "true"
        }, {
          id: "2",
          img: require("@/assets/images/users/avatar-1.jpg"),
          name: "Nicholas Ball",
          designation: "Assistant / Store Keeper",
          location: "San Lorenzo",
          type: "Full Time",
          rating: "4.1",
          ratingCount: "1.72k",
          bookmark: "true"
        }, {
          id: "3",
          img: require("@/assets/images/users/avatar-4.jpg"),
          name: "Zynthia Marrow",
          designation: "Assistant / Store Keeper",
          location: "Cullera, Spain",
          type: "Freelancer",
          rating: "4.0",
          ratingCount: "42.5k",
          bookmark: "false"
        }, {
          id: "4",
          img: require("@/assets/images/users/avatar-2.jpg"),
          name: "Philippa Santiago",
          designation: "Project Manager ",
          location: "Ugashik, US",
          type: "Part Time",
          rating: "4.3",
          ratingCount: "15k",
          bookmark: "true"
        }, {
          id: "5",
          img: require("@/assets/images/users/avatar-4.jpg"),
          name: "Elizabeth Allen",
          designation: "Education Training ",
          location: "Zuweihir, UAE",
          type: "Freelancer",
          rating: "3.5",
          ratingCount: "7.3k",
          bookmark: "false"
        }, {
          id: "6",
          img: require("@/assets/images/users/avatar-5.jpg"),
          name: "Cassian Jenning",
          designation: "Graphic Designer ",
          location: "Limestone, US",
          type: "Part Time",
          rating: "4.3",
          ratingCount: "13.2k",
          bookmark: "false"
        }, {
          id: "7",
          img: require("@/assets/images/users/avatar-6.jpg"),
          name: "Scott Holt",
          designation: "UI/UX Designer ",
          location: "Germany",
          type: "Part Time",
          rating: "3.5",
          ratingCount: "7.3k",
          bookmark: "false"
        }, {
          id: "8",
          img: require("@/assets/images/users/avatar-9.jpg"),
          name: "Philbert Schwartz",
          designation: "React Developer ",
          location: "Zuweihir, UAE",
          type: "Full Time",
          rating: "4.1",
          ratingCount: "1.74k",
          bookmark: "true"
        }, {
          id: "9",
          img: require("@/assets/images/users/avatar-2.jpg"),
          name: "Larry Villa",
          designation: "Assistant / Store Keeper",
          location: "San Lorenzo",
          type: "Full Time",
          rating: "4.0",
          ratingCount: "1.72k",
          bookmark: "false"
        }, {
          id: "10",
          img: require("@/assets/images/users/avatar-10.jpg"),
          name: "Harley Watkins",
          designation: "Project Manager ",
          location: "Texanna, US",
          type: "Full Time",
          rating: "4.2",
          ratingCount: "3.21k",
          bookmark: "false"
        }, {
          id: "11",
          img: require("@/assets/images/users/avatar-2.jpg"),
          name: "Marie Stewart",
          designation: "Web Designer",
          location: "Cullera, Spain",
          type: "Part Time",
          rating: "4.2",
          ratingCount: "2.2k",
          bookmark: "true"
        }, {
          id: "12",
          img: require("@/assets/images/users/avatar-9.jpg"),
          name: "Hadley Leonard",
          designation: "Executive, HR Operations ",
          location: "Zuweihir, UAE",
          type: "Full Time",
          rating: "4.0",
          ratingCount: "3.2k",
          bookmark: "false"
        }, {
          id: "13",
          img: require("@/assets/images/users/avatar-6.jpg"),
          name: "Zoderick Rodriquez",
          designation: "Full Stack Developer",
          location: "Muhtarqah, UAE",
          type: "Freelancer",
          rating: "3.9",
          ratingCount: "98.65k",
          bookmark: "false"
        }, {
          id: "14",
          img: require("@/assets/images/users/avatar-7.jpg"),
          name: "Nadia Harding",
          designation: "Web Designer",
          location: "Pahoa, US",
          type: "Freelancer",
          rating: "4.3",
          ratingCount: "2.93k",
          bookmark: "true"
        }, {
          id: "15",
          img: require("@/assets/images/users/avatar-1.jpg"),
          name: "Addison Black",
          designation: "UI/UX Designer",
          location: "Phoenix, Arizona",
          type: "Part Time",
          rating: "3.8",
          ratingCount: "10.32k",
          bookmark: "false"
        }, {
          id: "16",
          img: require("@/assets/images/users/avatar-4.jpg"),
          name: "Priscilla Wise",
          designation: "Executive, HR Operations",
          location: "Ghurayfah, UAE",
          type: "Full Time",
          rating: "4.0",
          ratingCount: "7.36k",
          bookmark: "false"
        }, {
          id: "17",
          img: require("@/assets/images/users/avatar-8.jpg"),
          name: "Lizzie Chandler",
          designation: "React Developer",
          location: "Maidaq, UAE",
          type: "Part Time",
          rating: "3.9",
          ratingCount: "1.35k",
          bookmark: "false"
        }, {
          id: "18",
          img: require("@/assets/images/users/avatar-1.jpg"),
          name: "Jenson Carlson",
          designation: "Graphic Designer",
          location: "Quesada, US",
          type: "Freelancer",
          rating: "4.2",
          ratingCount: "3.16k",
          bookmark: "false"
        }, {
          id: "19",
          img: require("@/assets/images/users/avatar-1.jpg"),
          name: "Jaylee Ward",
          designation: "Education Training",
          location: "Cullera, Spain",
          type: "Full Time",
          rating: "4.0",
          ratingCount: "3.21k",
          bookmark: "true"
        }, {
          id: "20",
          img: require("@/assets/images/users/avatar-2.jpg"),
          name: "Trista Guerrero",
          designation: "Product Director",
          location: "Jereirah, UAE",
          type: "Full Time",
          rating: "4.1",
          ratingCount: "4.31k",
          bookmark: "false"
        }, {
          id: "21",
          img: require("@/assets/images/users/avatar-1.jpg"),
          name: "James Stone",
          designation: "Graphic Designer",
          location: "Quesada, US",
          type: "Freelancer",
          rating: "4.2",
          ratingCount: "3.16k",
          bookmark: "false"
        }, {
          id: "22",
          img: require("@/assets/images/users/avatar-4.jpg"),
          name: "Mike Watson",
          designation: "Product Director",
          location: "Jereirah, UAE",
          type: "Full Time",
          rating: "4.1",
          ratingCount: "4.13k",
          bookmark: "false"
        }, {
          id: "23",
          img: require("@/assets/images/users/avatar-9.jpg"),
          name: "Mary Sak",
          designation: "Education Training",
          location: "Cullera, Spain",
          type: "Full Time",
          rating: "4.0",
          ratingCount: "3.21k",
          bookmark: "true"
        }, {
          id: "24",
          img: require("@/assets/images/users/avatar-8.jpg"),
          name: "Roderick Jones",
          designation: "React Developer",
          location: "Maidaq, UAE",
          type: "Part Time",
          rating: "3.9",
          ratingCount: "1.35k",
          bookmark: "false"
        }
      ]
    };
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.candidatelist);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.name.toLowerCase().includes(search) ||
            data.designation.toLowerCase().includes(search) ||
            data.type.toLowerCase().includes(search) ||
            data.ratingCount.toLowerCase().includes(search) ||
            data.rating.toLowerCase().includes(search) ||
            data.location.toLowerCase().includes(search)
          );
        });
      } else {
        return this.displayedPosts;
      }
    },
  },
  watch: {
    candidatelist() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  methods: {
    setPages() {
      let numberOfPages = Math.ceil(this.candidatelist.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(candidatelist) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return candidatelist.slice(from, to);
    }
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
    <b-row class="g-4 mb-4">
      <b-col sm="auto">
        <div>
          <b-link href="#!" class="btn btn-success"><i class="ri-add-line align-bottom me-1"></i> Add Candidate</b-link>
        </div>
      </b-col>
      <b-col sm>
        <div class="d-md-flex justify-content-sm-end gap-2">
          <div class="search-box ms-md-2 flex-shrink-0 mb-3 mb-md-0">
            <input type="text" class="form-control" id="searchJob" autocomplete="off"
              placeholder="Search for candidate name or designation..." v-model="searchQuery">
            <i class="ri-search-line search-icon"></i>
          </div>
          <div class="w-md">
            <select class="form-select" data-choices data-choices-search-false>
              <option value="All">All</option>
              <option value="Today">Today</option>
              <option value="Yesterday" selected>Yesterday</option>
              <option value="Last 7 Days">Last 7 Days</option>
              <option value="Last 30 Days">Last 30 Days</option>
              <option value="This Month">This Month</option>
              <option value="Last Year">Last Year</option>
            </select>
          </div>
        </div>
      </b-col>
    </b-row>

    <b-row class="gy-2 mb-2" id="candidate-list">
      <b-col lg="12" v-for="(data, index) of resultQuery" :key="index">
        <b-card no-body class="mb-0">
          <b-card-body>
            <div class="d-lg-flex align-items-center">
              <div class="flex-shrink-0">
                <div class="avatar-sm rounded">
                  <img :src="data.img" alt="" class="member-img img-fluid d-block rounded">
                </div>
              </div>
              <div class="ms-3">
                <b-link href="/pages/profile">
                  <h5 class="fs-16 mb-2">{{ data.name }}</h5>
                </b-link>
                <p class="text-muted mb-0">{{ data.designation }}</p>
              </div>
              <div class="d-flex gap-4 mt-0 text-muted mx-auto">
                <div><i class="ri-map-pin-2-line text-primary me-1 align-bottom"></i> {{ data.location }}</div>
                <div><i class="ri-time-line text-primary me-1 align-bottom"></i> <span class="badge" :class="{
                  'badge-soft-success': data.type == 'Full Time',
                  'badge-soft-danger': data.type == 'Part Time',
                  'badge-soft-primary': data.type == 'Freelancer',
                }">{{ data.type }}</span></div>
              </div>
              <div class="d-flex flex-wrap gap-2 align-items-center mx-auto">
                <b-badge tag="div" variant="bg-success" class="text-bg-success"> <i class="mdi mdi-star me-1"></i>{{
                    data.rating
                }}</b-badge>
                <div class="text-muted">{{ data.ratingCount }} Ratings</div>
              </div>
              <div>
                <b-link href="#!" class="btn btn-soft-success me-1">View Details</b-link>
                <b-link href="#!" class="btn btn-ghost-danger btn-icon custom-toggle"
                  :class="{ 'active': data.bookmark == 'true', '': data.bookmark == 'false' }" data-bs-toggle="button"
                  aria-pressed="false">
                  <span class="icon-on"><i class="ri-bookmark-line align-bottom"></i></span> <span class="icon-off"><i
                      class="ri-bookmark-3-fill align-bottom"></i></span>
                </b-link>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>


    </b-row>

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
            <b-link href="#" class="page-link" id="page-next" @click="page++" v-if="page < pages.length">Next</b-link>
          </div>
        </div>
      </b-col>
    </b-row>
  </Layout>
</template>