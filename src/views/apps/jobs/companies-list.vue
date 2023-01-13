<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

export default {
  page: {
    title: "Companies List",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Companies List",
      items: [
        {
          text: "Jobs",
          href: "/",
        },
        {
          text: "Companies List",
          active: true,
        },
      ],
      page: 1,
      perPage: 16,
      pages: [],
      companies: [
        {
          id: "1",
          image_src: require("@/assets/images/companies/img-3.png"),
          name: "Martin's Solutions",
          industry_type: "IT Department",
          vacancy: "97",
          company_info: "The IT department of a company ensures that the network of computers within the organisation are well-connected and functioning properly. All the other departments within the company rely on them to ensure that their respective functions can go on seamlessly.",
          location: "Cullera, Spain",
          employee: "250-300",
          rating: "4.8",
          website: "www.martinsolution.com",
          email: "info@martinsolution.com",
          since: "1995"
        }, {
          id: "2",
          image_src: require("@/assets/images/companies/img-4.png"),
          name: "Syntyce Solutions",
          industry_type: "Health Services",
          vacancy: "31",
          company_info: "These cases are perfectly simple and easy to distinguish. In a free hour, when our power of choice is untrammelled and when nothing prevents to do what we like best, every pleasure is to be welcomed and every pain avoided, because it is pleasure.",
          location: "San Lorenzo",
          employee: "400-450",
          rating: "4.4",
          website: "www.syntycesolution.com",
          email: "info@syntycesolution.com",
          since: "2001"
        }, {
          id: "3",
          image_src: require("@/assets/images/companies/img-1.png"),
          name: "Moetic Fashion",
          industry_type: "Textiles: Clothing, Footwear",
          vacancy: "641",
          company_info: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim quia voluptas sit.",
          location: "Cullera, Spain",
          employee: "900-950",
          rating: "4.2",
          website: "-",
          email: "email@moeticfashion.com",
          since: "2000"
        }, {
          id: "4",
          image_src: require("@/assets/images/companies/img-5.png"),
          name: "Meta4Systems",
          industry_type: "Computer Industry",
          vacancy: "322",
          company_info: "In a free hour, when our power of choice is untrammelled and when nothing prevents our being able to do what we like best. But in certain circumstances and owing to the claims of duty or the obligations of business it will frequently occur.",
          location: "Ugashik, US",
          employee: "10-50",
          rating: "4.5",
          website: "www.meta4systems.com",
          email: "support@meta4systems.com",
          since: "2019"
        }, {
          id: "5",
          image_src: require("@/assets/images/companies/img-1.png"),
          name: "Kent's",
          industry_type: "IT Department",
          vacancy: "10",
          company_info: "A UI/UX designer's job is to create user-friendly interfaces that enable users to understand how to use complex technical. If you're passionate, you'll find great fulfillment in being involved in the design process for the next hot gadget.",
          location: "Zuweihir, UAE",
          employee: "10-50",
          rating: "4.1",
          website: "-",
          email: "-",
          since: "2018"
        }, {
          id: "6",
          image_src: require("@/assets/images/companies/img-7.png"),
          name: "Micro Design",
          industry_type: "Financial Services",
          vacancy: "140",
          company_info: "As a Product Designer, you will work within a Product Delivery Team fused with UX, engineering, product and data talent.If several languages coalesce, the grammar of the resulting If several languages coalesce, the grammar of the resulting.",
          location: "Limestone, US",
          employee: "300-350",
          rating: "4.5",
          website: "www.microdesign.com",
          email: "info@microdesign.com",
          since: "2016"
        }, {
          id: "7",
          image_src: require("@/assets/images/companies/img-6.png"),
          name: "Zoetic Fashion",
          industry_type: "Textiles: Clothing, Footwear",
          vacancy: "21",
          company_info: "To achieve this, it would be necessary to have uniform grammar, pronunciation and more common words. If several languages coalesce, the grammar of the resulting language is more simple and regular than that of the individual languages existing.",
          location: "Germany",
          employee: "10-50",
          rating: "3.9",
          website: "-",
          email: "info@zoeticfashion.com",
          since: "2018"
        }, {
          id: "8",
          image_src: require("@/assets/images/companies/img-8.png"),
          name: "Digitech Galaxy",
          industry_type: "Telecommunications Services",
          vacancy: "154",
          company_info: "The IT department of a company ensures that the network of computers within the organisation are well-connected and functioning properly. All the other departments within the company rely on them to ensure that their respective functions can go on seamlessly.",
          location: "Zuweihir, UAE",
          employee: "400-415",
          rating: "4.0",
          website: "-",
          email: "-",
          since: "2014"
        }, {
          id: "9",
          image_src: require("@/assets/images/companies/img-9.png"),
          name: "Erlebacher's",
          industry_type: "Health Services",
          vacancy: "134",
          company_info: "Their separate existence is a myth. For science, music, sport, etc, Europe uses the same vocabulary. The languages only differ in their grammar, their pronunciation and their most common words. Everyone realizes why a new common language would be desirable.",
          location: "San Lorenzo",
          employee: "350-400",
          rating: "4.4",
          website: "-",
          email: "info@erlebacher.com",
          since: "2016"
        }, {
          id: "10",
          image_src: require("@/assets/images/companies/img-5.png"),
          name: "iTest Factory",
          industry_type: "Chemical Industries",
          vacancy: "126",
          company_info: "The new common language will be more simple and regular than the existing European languages. It will be as simple as Occidental; in fact, it will be Occidental. it will seem like simplified English, as a skeptical Cambridge friend of mine told me what Occidental.",
          location: "Texanna, US",
          employee: "250-300",
          rating: "4.5",
          website: "-",
          email: "info@itest.com",
          since: "2016"
        }, {
          id: "11",
          image_src: require("@/assets/images/companies/img-7.png"),
          name: "Zoetic Fashion",
          industry_type: "Textiles: Clothing, Footwear",
          vacancy: "47",
          company_info: "The IT department of a company ensures that the network of computers within the organisation are well-connected and functioning properly. All the other departments within the company rely on them to ensure that their respective functions can go on seamlessly.",
          location: "Cullera, Spain",
          employee: "120-150",
          rating: "4.7",
          website: "www.zoeticfashion.com",
          email: "info@zoeticfashion.com",
          since: "2015"
        }, {
          id: "12",
          image_src: require("@/assets/images/companies/img-3.png"),
          name: "Micro Design",
          industry_type: "IT Department",
          vacancy: "23",
          company_info: "Everyone realizes why a new common language would be desirable: one could refuse to pay expensive translators. To achieve this, it would be necessary to have uniform grammar, pronunciation and more common words. If several languages coalesce of the resulting.",
          location: "Zuweihir, UAE",
          employee: "80-100",
          rating: "4.6",
          website: "www.microdesign.com",
          email: "info@microdesign.com",
          since: "2014"
        }, {
          id: "13",
          image_src: require("@/assets/images/companies/img-4.png"),
          name: "Syntyce Solutions",
          industry_type: "Computer Industry",
          vacancy: "11",
          company_info: "The IT department of a company ensures that the network of computers within the organisation are well-connected and functioning properly. All the other departments within the company rely on them to ensure that their respective functions can go on seamlessly.",
          location: "Muhtarqah, UAE",
          employee: "50-70",
          rating: "4.2",
          website: "www.syntycesolutions.com",
          email: "support@syntycesolutions.com",
          since: "2016"
        }, {
          id: "14",
          image_src: require("@/assets/images/companies/img-1.png"),
          name: "Asiatic Solutions",
          industry_type: "Health Services",
          vacancy: "9",
          company_info: "To achieve this, it would be necessary to have uniform grammar, pronunciation and more common words. If several languages coalesce, the grammar of the resulting language is new common language will be more simple and regular than the existing European languages.",
          location: "Pahoa, US",
          employee: "30-50",
          rating: "3.8",
          website: "www.asiaticsolution.com",
          email: "info@asiaticsolution.com",
          since: "2019"
        }, {
          id: "15",
          image_src: require("@/assets/images/companies/img-1.png"),
          name: "Great Clothes",
          industry_type: "Textiles: Clothing, Footwear",
          vacancy: "60",
          company_info: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit.",
          location: "Phoenix, Arizona",
          employee: "120-150",
          rating: "4.0",
          website: "-",
          email: "-",
          since: "2017"
        }, {
          id: "16",
          image_src: require("@/assets/images/companies/img-5.png"),
          name: "Kent's Solutions",
          industry_type: "IT Department",
          vacancy: "26",
          company_info: "It is a paradisematic country, in which roasted parts of sentences fly into your mouth. Even the all-powerful Pointing has no control about the blind texts it is an almost unorthographic life One day however a small line of blind text by the name of Lorem Ipsum.",
          location: "Ghurayfah, UAE",
          employee: "50-80",
          rating: "4.2",
          website: "www.kentssolution.com",
          email: "info@kentssolution.com",
          since: "2018"
        }, {
          id: "17",
          image_src: require("@/assets/images/companies/img-4.png"),
          name: "Syntyce Solutions",
          industry_type: "Computer Industry",
          vacancy: "11",
          company_info: "The IT department of a company ensures that the network of computers within the organisation are well-connected and functioning properly. All the other departments within the company rely on them to ensure that their respective functions can go on seamlessly.",
          location: "Maidaq, UAE",
          employee: "50-70",
          rating: "4.2",
          website: "www.syntycesolutions.com",
          email: "support@syntycesolutions.com",
          since: "2016"
        }, {
          id: "18",
          image_src: require("@/assets/images/companies/img-4.png"),
          name: "Syntyce Solutions",
          industry_type: "Health Services",
          vacancy: "31",
          company_info: "These cases are perfectly simple and easy to distinguish. In a free hour, when our power of choice is untrammelled and when nothing prevents to do what we like best, every pleasure is to be welcomed and every pain avoided, because it is pleasure.",
          location: "Quesada, US",
          employee: "400-450",
          rating: "4.4",
          website: "www.syntycesolution.com",
          email: "info@syntycesolution.com",
          since: "2001"
        }, {
          id: "19",
          image_src: require("@/assets/images/companies/img-5.png"),
          name: "iTest Factory",
          industry_type: "Chemical Industries",
          vacancy: "126",
          company_info: "The new common language will be more simple and regular than the existing European languages. It will be as simple as Occidental; in fact, it will be Occidental. it will seem like simplified English, as a skeptical Cambridge friend of mine told me what Occidental.",
          location: "Cullera, Spain",
          employee: "250-300",
          rating: "4.5",
          website: "-",
          email: "info@itest.com",
          since: "2016"
        }, {
          id: "20",
          image_src: require("@/assets/images/companies/img-6.png"),
          name: "Zoetic Fashion",
          industry_type: "Textiles: Clothing, Footwear",
          vacancy: "21",
          company_info: "To achieve this, it would be necessary to have uniform grammar, pronunciation and more common words. If several languages coalesce, the grammar of the resulting language is more simple and regular than that of the individual languages existing.",
          location: "Jereirah, UAE",
          employee: "10-50",
          rating: "3.9",
          website: "-",
          email: "info@zoeticfashion.com",
          since: "2018"
        }
      ],
    };
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.companies);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.name.toLowerCase().includes(search) ||
            data.industry_type.toLowerCase().includes(search) ||
            data.vacancy.toLowerCase().includes(search) ||
            data.since.toLowerCase().includes(search) ||
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
    companies() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  methods: {
    showdetail(data) {
      document.querySelector('.company-logo').setAttribute('src', data.image_src);
      document.querySelector('.overview-companyname').innerHTML = data.name;
      document.querySelector('.overview-industryType').innerHTML = data.industry_type;
      document.querySelector('.overview-companydesc').innerHTML = data.company_info;
      document.querySelector('.overview-company_location').innerHTML = data.location;
      document.querySelector('.overview-employee').innerHTML = data.employee;
      document.querySelector('.overview-vacancy').innerHTML = data.vacancy;
      document.querySelector('.overview-rating').innerHTML = data.rating;
      document.querySelector('.overview-website').innerHTML = data.website;
      document.querySelector('.overview-email').innerHTML = data.email;
      document.querySelector('.overview-since').innerHTML = data.since;
    },

    setPages() {
      let numberOfPages = Math.ceil(this.companies.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(companies) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return companies.slice(from, to);
    },
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
      <b-col xxl="9">
        <b-card no-body>
          <b-card-body>
            <b-form>
              <b-row class="g-3">
                <b-col xxl="5" sm="6">
                  <div class="search-box">
                    <input type="text" class="form-control search bg-light border-light" id="searchCompany"
                      placeholder="Search for company, industry type...">
                    <i class="ri-search-line search-icon"></i>
                  </div>
                </b-col>

                <b-col xxl="3" sm="6">
                  <input type="text" class="form-control bg-light border-light" id="datepicker"
                    data-date-format="d M, Y" placeholder="Select date">
                </b-col>

                <b-col xxl="2" sm="4">
                  <div class="input-light">
                    <select class="form-control" data-choices data-choices-search-false name="choices-single-default"
                      id="idType">
                      <option value="all" selected>All</option>
                      <option value="Full Time">Full Time</option>
                      <option value="Part Time">Part Time</option>
                      <option value="Intership">Intership</option>
                      <option value="Freelance">Freelance</option>
                    </select>
                  </div>
                </b-col>

                <b-col xxl="2" sm="4">
                  <b-button type="button" variant="success" class="w-100" onclick="filterData();">
                    <i class="ri-equalizer-fill me-1 align-bottom"></i> Filters
                  </b-button>
                </b-col>
              </b-row>
            </b-form>
          </b-card-body>
        </b-card>

        <b-row class="job-list-row" id="companies-list">

          <b-col xxl="3" md="6" v-for="(data, index) of resultQuery" :key="index">
            <b-card no-body class="companiesList-card">
              <b-card-body>
                <div class="avatar-sm mx-auto">
                  <div class="avatar-title bg-light rounded">
                    <img :src="data.image_src" alt="" class="avatar-xxs companyLogo-img">
                  </div>
                </div>
                <div class="text-center">
                  <b-link href="#!">
                    <h5 class="mt-3 company-name">{{ data.name }}</h5>
                  </b-link>
                  <div class="d-none company-desc">{{ data.company_info }}
                  </div>
                  <p class="text-muted industry-type">{{ data.industry_type }}</p>
                  <div class="d-none"> <span class="employee">{{ data.employee }}</span>
                    <span class="location">{{ data.location }}</span>
                    <span class="rating">{{ data.rating }}</span>
                    <span class="website">{{ data.website }}</span>
                    <span class="email">{{ data.email }}</span>
                    <span class="since">{{ data.since }}</span>
                  </div>
                </div>
                <div>
                  <b-button type="button" variant="soft-primary" class="w-100 viewcompany-list"
                    @click="showdetail(data)"><span class="vacancy">{{
                        data.vacancy
                    }}</span> Jobs Available</b-button>
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
                <b-link href="javascript:void(0);" class="page-link" id="page-prev" v-if="page != 1" @click="page--">
                  Previous</b-link>
              </div>
              <span id="page-num" class="pagination">

                <span id="page-num" class="pagination">
                  <div class="page-item" :class="{ active: pageNumber == page, disabled: pageNumber == '...', }"
                    v-for="(pageNumber, index) in pages" :key="index" @click="page = pageNumber">
                    <b-link class="page-link clickPageNumber" href="javascript:void(0);">{{ pageNumber }}</b-link>
                  </div>
                </span>


              </span>
              <div class="page-item">
                <b-link href="javascript:void(0);" class="page-link" id="page-next" @click="page++"
                  v-if="page < pages.length">Next</b-link>
              </div>
            </div>
          </b-col>
        </b-row>
      </b-col>

      <b-col xxl="3">
        <b-card no-body id="company-overview">
          <b-card-body>
            <div class="avatar-lg mx-auto mb-3">
              <div class="avatar-title bg-light rounded">
                <img src="@/assets/images/companies/img-6.png" alt="" class="avatar-sm company-logo" id="company-logo">
              </div>
            </div>

            <div class="text-center">
              <b-link href="#!">
                <h5 class="overview-companyname" id="overview-companyname">Syntyce Solutions</h5>
              </b-link>
              <p class="text-muted overview-industryType" id="overview-industryType">IT Department</p>

              <ul class="list-inline mb-0">
                <li class="list-inline-item avatar-xs">
                  <b-link href="javascript:void(0);" class="avatar-title bg-soft-success text-success fs-15 rounded">
                    <i class="ri-global-line"></i>
                  </b-link>
                </li>
                <li class="list-inline-item avatar-xs">
                  <b-link href="javascript:void(0);" class="avatar-title bg-soft-danger text-danger fs-15 rounded">
                    <i class="ri-mail-line"></i>
                  </b-link>
                </li>
                <li class="list-inline-item avatar-xs">
                  <b-link href="javascript:void(0);" class="avatar-title bg-soft-warning text-warning fs-15 rounded">
                    <i class="ri-question-answer-line"></i>
                  </b-link>
                </li>
              </ul>
            </div>
          </b-card-body>

          <b-card-body>
            <h6 class="text-muted text-uppercase fw-semibold mb-3">Information</h6>
            <p class="text-muted mb-4 overview-companydesc" id="overview-companydesc">The IT department of a company
              ensures that the network of
              computers within the organisation are well-connected and functioning properly. All the other departments
              within the company rely on them to ensure that their respective functions can go on seamlessly.</p>

            <div class="table-responsive table-card">
              <table class="table table-borderless mb-4">
                <tbody>
                  <tr>
                    <td class="fw-medium" scope="row">Industry Type</td>
                    <td class="overview-industryType" id="overview-industryType">Chemical Industries</td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Location</td>
                    <td class="overview-company_location" id="overview-company_location">Damascus, Syria</td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Employee</td>
                    <td class="overview-employee" id="overview-employee">10-50</td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Vacancy</td>
                    <td class="overview-vacancy" id="overview-vacancy">23</td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Rating</td>
                    <td><span class="overview-rating" id="overview-rating">4.8</span> <i
                        class="ri-star-fill text-warning align-bottom"></i>
                    </td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Website</td>
                    <td>
                      <b-link href="javascript:void(0);" class="link-primary text-decoration-underline overview-website"
                        id="overview-website">www.syntycesolution.com</b-link>
                    </td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Contact Email</td>
                    <td class="overview-email" id="overview-email">info@syntycesolution.com</td>
                  </tr>
                  <tr>
                    <td class="fw-medium" scope="row">Since</td>
                    <td class="overview-since" id="overview-since">1995</td>
                  </tr>
                </tbody>
              </table>
            </div>

            <div class="hstack gap-3">
              <b-button type="button" variant="soft-success" class="custom-toggle w-100" data-bs-toggle="button">
                <span class="icon-on"><i class="ri-add-line align-bottom me-1"></i> Follow</span>
                <span class="icon-off"><i class="ri-user-unfollow-line align-bottom me-1"></i> Unfollow</span>
              </b-button>
              <b-link href="#!" class="btn btn-primary w-100">More View <i class="ri-arrow-right-line align-bottom"></i>
              </b-link>
            </div>
          </b-card-body>
        </b-card>

        <b-card no-body class="overflow-hidden shadow-none">
          <b-card-body class="bg-soft-danger">
            <div class="d-flex align-items-center">
              <div class="flex-shrink-0">
                <div class="avatar-sm">
                  <div class="avatar-title bg-soft-danger text-danger rounded-circle fs-17">
                    <i class="ri-gift-line"></i>
                  </div>
                </div>
              </div>
              <div class="flex-grow-1 ms-2">
                <h6 class="fs-16">Free trial</h6>
                <p class="text-muted mb-0">28 days left</p>
              </div>
              <div>
                <b-link href="/pages/pricing" class="btn btn-danger">Upgrade</b-link>
              </div>
            </div>
          </b-card-body>
          <b-card-body class="bg-soft-danger border-top border-danger border-opacity-25 border-top-dashed">
            <b-link href="#!" class="d-flex justify-content-between align-items-center text-body">
              <span>See benefits</span>
              <i class="ri-arrow-right-s-line fs-18"></i>
            </b-link>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>