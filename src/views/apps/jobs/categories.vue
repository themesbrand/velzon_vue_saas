<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";
import Lottie from "@/components/widgets/lottie.vue";
import animationData from "@/components/widgets/xulniijg.json";
import animationData1 from "@/components/widgets/oclwxpmm.json";
import animationData2 from "@/components/widgets/dklbhvrt.json";
import animationData3 from "@/components/widgets/adwosptt.json";
import animationData4 from "@/components/widgets/kkcllwsu.json";
import animationData5 from "@/components/widgets/rahcoaeu.json";
import animationData6 from "@/components/widgets/smauprql.json";
import animationData7 from "@/components/widgets/itykargr.json";
import animationData8 from "@/components/widgets/cnyeuzxc.json";
import animationData9 from "@/components/widgets/sygggnra.json";
import animationData10 from "@/components/widgets/hfmdczge.json";
import animationData11 from "@/components/widgets/xhebrhsj.json";
import animationData12 from "@/components/widgets/ucvsemjq.json";
import animationData13 from "@/components/widgets/pvbjsfif.json";
import animationData14 from "@/components/widgets/auvicynv.json";

export default {
  page: {
    title: "Job Categories",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Job Categories",
      items: [
        {
          text: "Jobs",
          href: "/",
        },
        {
          text: "Job Categories",
          active: true,
        },
      ],
      defaultOptions: {
        animationData: animationData
      },
      defaultOptions1: {
        animationData: animationData1
      },
      defaultOptions2: {
        animationData: animationData2
      },
      defaultOptions3: {
        animationData: animationData3
      },
      defaultOptions4: {
        animationData: animationData4
      },
      defaultOptions5: {
        animationData: animationData5
      },
      defaultOptions6: {
        animationData: animationData6
      },
      defaultOptions7: {
        animationData: animationData7
      },
      defaultOptions8: {
        animationData: animationData8
      },
      defaultOptions9: {
        animationData: animationData9
      },
      defaultOptions10: {
        animationData: animationData10
      },
      defaultOptions11: {
        animationData: animationData11
      },
      defaultOptions12: {
        animationData: animationData12
      },
      defaultOptions13: {
        animationData: animationData13
      },
      defaultOptions14: {
        animationData: animationData14
      },

    };
  },
  components: {
    Layout,
    PageHeader,
    lottie: Lottie,
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col col lg="12">
        <b-card no-body>
          <b-card-header>
            <b-row class="justify-content-between gy-3">
              <b-col lg="3">
                <div class="search-box">
                  <input type="text" class="form-control search" placeholder="Search for job categories...">
                  <i class="ri-search-line search-icon"></i>
                </div>
              </b-col>
              <b-col lg="auto">
                <div class="d-md-flex text-nowrap gap-2">
                  <b-button variant="info" class="add-btn"><i class="ri-add-fill me-1 align-bottom"></i> Add Categories</b-button>
                  <b-button variant="danger" ><i class="ri-filter-2-line me-1 align-bottom"></i> Filters</b-button>
                  <button type="button" id="dropdownMenuLink1" data-bs-toggle="dropdown" aria-expanded="false"
                    class="btn btn-soft-info"><i class="ri-more-2-fill"></i></button>
                  <ul class="dropdown-menu" aria-labelledby="dropdownMenuLink1">
                    <li>
                      <b-link class="dropdown-item" href="#">All</b-link>
                    </li>
                    <li>
                      <b-link class="dropdown-item" href="#">Last Week</b-link>
                    </li>
                    <li>
                      <b-link class="dropdown-item" href="#">Last Month</b-link>
                    </li>
                    <li>
                      <b-link class="dropdown-item" href="#">Last Year</b-link>
                    </li>
                  </ul>
                </div>
              </b-col>
            </b-row>
          </b-card-header>
        </b-card>
      </b-col>
    </b-row>

    <b-row class="row-cols-xxl-5 row-cols-lg-3 row-cols-md-2 row-cols-1">
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions" :height="50" :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Business Development</h5>
            </b-link>
            <p class="text-muted mb-0">102 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions1" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Automotive Jobs</h5>
            </b-link>
            <p class="text-muted mb-0">64 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions2" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Construction / Facilities</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions3" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Design, Art & Multimedia</h5>
            </b-link>
            <p class="text-muted mb-0">49 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions4" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Healthcare</h5>
            </b-link>
            <p class="text-muted mb-0">97 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions5" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Sales & Marketing</h5>
            </b-link>
            <p class="text-muted mb-0">312 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions6" :trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Accounting / Finance</h5>
            </b-link>
            <p class="text-muted mb-0">62 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions7" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Project Management</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions8" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Costomer Services</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions9" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Content Writer</h5>
            </b-link>
            <p class="text-muted mb-0">746 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions10" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Government Jobs</h5>
            </b-link>
            <p class="text-muted mb-0">642 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions11" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Digital Marketing</h5>
            </b-link>
            <p class="text-muted mb-0">364 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions12" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Education & training</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions13" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">IT & Software</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col>
        <b-card no-body>
          <b-card-body class="text-center py-4">
            <lottie class="avatar-xl icon-primary" colors="primary:#405189" :options="defaultOptions14" trigger="hover" :height="50"
              :width="50" />
            <b-link href="#!" class="stretched-link">
              <h5 class="mt-4">Catering & Tourism</h5>
            </b-link>
            <p class="text-muted mb-0">35 Position</p>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <b-row>
      <b-col lg="12">
        <div class="text-center mb-3">
          <b-button variant="link" class="text-success mt-2" id="loadmore"><i class="mdi mdi-loading mdi-spin fs-20 align-middle me-2"></i> Load More </b-button>
        </div>
      </b-col>
    </b-row>
  </Layout>
</template>