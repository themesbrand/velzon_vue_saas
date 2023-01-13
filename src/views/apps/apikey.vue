<script>
import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";
import { CheckCircleIcon, AlertOctagonIcon } from "@zhuowenli/vue-feather-icons";
import { CountTo } from "vue3-count-to";
import animationData from "@/components/widgets/msoeawqm.json";
import Lottie from "@/components/widgets/lottie.vue";
import Swal from "sweetalert2";

export default {
  page: {
    title: "API Key",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "API Key",
      items: [
        {
          text: "Apps",
          href: "/",
        },
        {
          text: "API Key",
          active: true,
        },
      ],
      createApiModal: false,
      page: 1,
      perPage: 8,
      pages: [],
      apikeydata: [
        {
          id: "1",
          name: "Streamlab",
          createby: "Michael Morris",
          apikey: "fef67078-6fb6-4689-b342-6ddc24481728",
          status: "Disable",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "2",
          name: "Streamlab",
          createby: "Zynthia Marrow",
          apikey: "ed4c0d11-7d49-4c94-aae8-83fafb226ee9",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "3",
          name: "Streamlab",
          createby: "Philippa Santiago",
          apikey: "0b53e8e2-e53d-4067-8be0-9cddea19e45e",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "4",
          name: "Streamlab",
          createby: "Elizabeth Allen",
          apikey: "b69ee258-1053-4e08-adbd-d37837f9c558",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "5",
          name: "Streamlab",
          createby: "Cassian Jenning",
          apikey: "33ec3a35-8b44-48f3-ba68-f3ea1e9ef214",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "6",
          name: "Streamlab",
          createby: "Harley Watkins",
          apikey: "84540348-f97d-41de-87c6-f5eae32aecc5",
          status: "Disable",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "7",
          name: "Streamlab",
          createby: "Addison Black",
          apikey: "aecc1ede-f613-48d5-8140-7108b324f0bd",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "8",
          name: "Streamlab",
          createby: "Nicki Butler",
          apikey: "8abba6e5-9622-46d2-8c52-c937e1d20ba2",
          status: "Active",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }, {
          id: "9",
          name: "Streamlab",
          createby: "Tara Hawkins",
          apikey: "9e6d336a-2f98-43e9-9fa6-11b4d5cdaf62",
          status: "Disable",
          create_date: "24 Sep 2022",
          expiry_date: "24 Jan 2023"
        }
      ],
      defaultOptions: {
        animationData: animationData
      },
    };
  },
  computed: {
    displayedPosts() {
      return this.paginate(this.apikeydata);
    },
    resultQuery() {
      if (this.searchQuery) {
        const search = this.searchQuery.toLowerCase();
        return this.displayedPosts.filter((data) => {
          return (
            data.name.toLowerCase().includes(search) ||
            data.designation.toLowerCase().includes(search) ||
            data.postDate.toLowerCase().includes(search) ||
            data.description.toLowerCase().includes(search) ||
            data.location.toLowerCase().includes(search)
          );
        });
      } else {
        return this.displayedPosts;
      }
    },
  },
  watch: {
    apikeydata() {
      this.setPages();
    },
  },
  created() {
    this.setPages();
  },
  methods: {
    setPages() {
      let numberOfPages = Math.ceil(this.apikeydata.length / this.perPage);
      this.pages = [];
      for (let index = 1; index <= numberOfPages; index++) {
        this.pages.push(index);
      }
    },
    paginate(apikeydata) {
      let page = this.page;
      let perPage = this.perPage;
      let from = page * perPage - perPage;
      let to = page * perPage;
      return apikeydata.slice(from, to);
    },

    generateApiID() {
      var d = new Date().getTime();

      if (window.performance && typeof window.performance.now === "function") {
        d += performance.now();
      }

      var uuid = 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function (c) {
        var r = (d + Math.random() * 16) % 16 | 0;
        d = Math.floor(d / 16);
        return (c == 'x' ? r : r & 0x3 | 0x8).toString(16);
      });

      return uuid;
    },

    handleApikeydetails(e, item) {

      this.createApiModal = true;
      const modalHeader = document.querySelector('.exampleModalLabel');
      const createApibtn = document.getElementById('createApimodal-btn');
      const addbtn = document.getElementById('add-btn');
      const editbtn = document.getElementById('edit-btn');
      const apikeyelement = document.getElementById('apikey-element');

      const apikeyId = document.getElementById("apikeyId");
      const apikeyname = document.getElementById("api-key-name");
      const apikey = document.getElementById("api-key");
      if (e.target.id == "createApi-btn" || e.target.id == "addApi-btn") {
        document.getElementById("addform").reset();

        modalHeader.innerHTML = "Create API Key";
        createApibtn.style.display = 'block';
        apikeyelement.style.display = 'none';
        addbtn.style.display = 'none';
        editbtn.style.display = 'none';

      } else if (e.target.id == "edit-item-btn") {
        modalHeader.innerHTML = "Rename API name";
        createApibtn.style.display = 'none';
        addbtn.style.display = 'none';
        editbtn.style.display = 'block';
        apikeyelement.style.display = 'block';

        apikeyId.value = item.id;
        apikeyname.value = item.name;
        apikey.value = item.apikey;

      } else if (e.target.id == "regenerate-api-btn") {
        modalHeader.innerHTML = "Regenerate API";
        createApibtn.style.display = 'none';
        addbtn.style.display = 'none';
        editbtn.style.display = 'block';
        apikeyelement.style.display = 'block';

        apikeyId.value = item.id;
        apikeyname.value = item.name;
        apikey.value = this.generateApiID();

      } else {
        modalHeader.innerHTML = "Create API Key";
        if (apikeyname.value != (null || "")) {
          createApibtn.style.display = 'none';
          apikeyelement.style.display = 'block';
          addbtn.style.display = 'block';
          editbtn.style.display = 'none';
          apikey.value = this.generateApiID();
        } else {
          document.getElementById("api-key-error-msg").classList.remove("d-none");
          document.getElementById("api-key-error-msg").classList.add("d-block");

          setTimeout(() => {
            document.getElementById("api-key-error-msg").classList.add("d-none");
            document.getElementById("api-key-error-msg").classList.remove("d-block");
          }, "2000");

        }
      }
    },

    handleApiKeys() {
      var id = this.apikeydata.length + 1;
      var apikeyname = document.getElementById('api-key-name').value;
      var apikey = document.getElementById('api-key').value;

      if (document.querySelector('.exampleModalLabel').innerHTML == "Create API Key") {
        if (id != null && apikeyname != null && apikey != null) {
          const data = {
            id: id,
            name: apikeyname,
            createby: "Anna Adame",
            status: "Active",
            apikey: apikey,
            create_date: new Date().toUTCString().slice(5, 16),
            expiry_date: new Date().toUTCString().slice(5, 16)
          };
          document.getElementById("close-modal").click();
          this.apikeydata.unshift(data);
        }
        document.getElementById("addform").reset();
      } else if (document.querySelector('.exampleModalLabel').innerHTML == "Rename API name") {
        id = document.getElementById('apikeyId').value;

        this.apikeydata.forEach(element => {
          if (element.id.toString() == id.toString()) {
            element.name = apikeyname;
          }
        });
        document.getElementById("close-modal").click();
      } else {
        id = document.getElementById('apikeyId').value;

        this.apikeydata.forEach(element => {
          if (element.id.toString() == id.toString()) {
            element.apikey = apikey;
          }
        });
        document.getElementById("close-modal").click();
      }
    },
    deleteApikey(event) {
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
          this.apikeydata.splice(this.apikeydata.indexOf(event), 1);
          Swal.fire("Deleted!", "Your file has been deleted.", "success");
        }
      });
    },

    changestatus(data) { data.status == "Active" ? data.status = "Disable" : data.status = "Active"; }

  },
  components: {
    Layout,
    PageHeader,
    CountTo,
    CheckCircleIcon,
    AlertOctagonIcon,
    lottie: Lottie,
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />
    <b-row>
      <b-col lg="4">
        <b-card no-body class="card-height-100">
          <b-card-body>
            <h5 class="card-title mb-3">Developer Plan</h5>
            <div class="progress animated-progress custom-progress mb-1">
              <div class="progress-bar bg-secondary" role="progressbar" style="width: 38%" aria-valuenow="38"
                aria-valuemin="0" aria-valuemax="100"></div>
            </div>
            <p class="text-muted mb-2">You used 215 of 2000 of your API</p>
            <div class="text-end">
              <b-link class="btn btn-primary button create-btn btn-sm" type="button" id="createApi-btn"
                @click="(e) => handleApikeydetails(e)">Create API Key</b-link>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="4">
        <b-card no-body class="card-animate card-height-100">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Successful conversions</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal='0' :endVal='50' :duration='5000'></count-to>
                </h2>
                <p class="mb-0 text-muted"><b-badge class="bg-light text-success mb-0"><i
                      class="ri-arrow-up-line align-middle"></i> 8.24 % </b-badge> 7 last week</p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-success rounded-circle fs-2">
                    <CheckCircleIcon width="24" height="24" class="text-success"></CheckCircleIcon>
                  </span>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col lg="4">
        <b-card no-body class="card-animate card-height-100">
          <b-card-body>
            <div class="d-flex justify-content-between">
              <div>
                <p class="fw-medium text-muted mb-0">Failed conversions</p>
                <h2 class="mt-4 ff-secondary fw-semibold">
                  <count-to :startVal='0' :endVal='8' :duration='5000'></count-to>
                </h2>
                <p class="mb-0 text-muted"><b-badge class="bg-light text-danger mb-0"><i
                      class="ri-arrow-down-line align-middle"></i> 25.87 % </b-badge> 7 last week</p>
              </div>
              <div>
                <div class="avatar-sm flex-shrink-0">
                  <span class="avatar-title bg-soft-danger rounded-circle fs-2">
                    <AlertOctagonIcon width="24" height="24" class="text-danger"></AlertOctagonIcon>
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
        <b-card no-body id="apiKeyList">
          <b-card-header class="d-flex align-items-center">
            <h5 class="card-title flex-grow-1 mb-0">API Keys</h5>
            <div class="d-flex gap-1 flex-wrap">
              <b-button variant="soft-danger" id="remove-actions" onClick="deleteMultiple()"><i
                  class="ri-delete-bin-2-line"></i>
              </b-button>
              <b-link class="btn btn-primary button create-btn" type="button" id="addApi-btn"
                @click="(e) => handleApikeydetails(e)"><i class="ri-add-line align-bottom me-1"></i>
                Add API Key </b-link>
            </div>
          </b-card-header>
          <b-card-body>
            <div>
              <div class="table-responsive table-card mb-3">
                <table class="table align-middle table-nowrap mb-0">
                  <thead class="table-light">
                    <tr>
                      <th scope="col" style="width: 50px;">
                        <div class="form-check">
                          <input class="form-check-input" type="checkbox" id="checkAll" value="option">
                        </div>
                      </th>
                      <th class="sort d-none" data-sort="id" scope="col">Id</th>
                      <th class="sort" data-sort="name" scope="col">Name</th>
                      <th class="sort" data-sort="createBy" scope="col">Created By</th>
                      <th class="sort" data-sort="apikey" scope="col">API Key</th>
                      <th class="sort" data-sort="status" scope="col">Status</th>
                      <th class="sort" data-sort="create_date" scope="col">Create Date</th>
                      <th class="sort" data-sort="expiry_date" scope="col">Expiry Date</th>
                      <th scope="col">Action</th>
                    </tr>
                  </thead>
                  <tbody class="list form-check-all">
                    <tr v-for="(data, index) of resultQuery" :key="index">
                      <th scope="row">
                        <div class="form-check">
                          <input class="form-check-input" type="checkbox" name="chk_child" value="option1">
                        </div>
                      </th>
                      <td class="id" style="display:none;">
                        <b-link href="javascript:void(0);" class="fw-medium link-primary">{{ data.id }}</b-link>
                      </td>
                      <td class="name">{{ data.name }}</td>
                      <td class="createBy">{{ data.createby }}</td>
                      <td class="apikey">
                        <input type="text" class="form-control apikey-value" readonly="" :value="data.apikey">
                      </td>
                      <td class="status"><b-badge variant="badge-soft-success" :class="{
                        'badge-soft-success': data.status == 'Active',
                        'badge-soft-danger': data.status == 'Disable',
                      }">{{ data.status }}</b-badge></td>
                      <td class="create_date">{{ data.create_date }}</td>
                      <td class="expiry_date">{{ data.expiry_date }}</td>
                      <td>
                        <div class="dropdown">
                          <b-button variant="soft-secondary" size="sm" class="dropdown" type="button"
                            data-bs-toggle="dropdown" aria-expanded="false">
                            <i class="ri-more-fill align-middle"></i>
                          </b-button>
                          <ul class="dropdown-menu dropdown-menu-end">
                            <li>
                              <b-link class="dropdown-item edit-item-btn" id="edit-item-btn"
                                @click="(e) => handleApikeydetails(e, data)">Rename</b-link>
                            </li>
                            <li>
                              <b-link class="dropdown-item regenerate-api-btn" id="regenerate-api-btn"
                                @click="(e) => handleApikeydetails(e, data)">Regenerate Key</b-link>
                            </li>
                            <li>
                              <b-link class="dropdown-item disable-btn" id="disable-btn" href="javascript:void(0);"
                                @click="(e) => changestatus(data)">{{ data.status == "Active" ? "Disable" : "Active"
                                }} </b-link>
                            </li>
                            <li>
                              <b-link class="dropdown-item remove-item-btn" href="#deleteApiKeyModal"
                                @click="deleteApikey(data)">Delete</b-link>
                            </li>
                          </ul>
                        </div>
                      </td>
                    </tr>
                  </tbody>
                </table>
                <div class="noresult" style="display: none">
                  <div class="text-center">
                    <lottie class="avatar-xl" colors="primary:#121331,secondary:#08a88a" :options="defaultOptions"
                      :height="75" :width="75" />
                    <h5 class="mt-2">Sorry! No Result Found</h5>
                    <p class="text-muted mb-0">We've searched more than 150+ API Keys We did not find any API for you
                      search.</p>
                  </div>
                </div>
              </div>
              <div class="d-flex justify-content-end mt-3">
                <div class="pagination-wrap hstack gap-2">
                  <b-link class="page-item pagination-prev disabled" href="#" v-if="page != 1" @click="page--">
                    Previous
                  </b-link>
                  <ul class="pagination listjs-pagination mb-0">
                    <li :class="{ active: pageNumber == page, disabled: pageNumber == '...', }"
                      v-for="(pageNumber, index) in pages" :key="index" @click="page = pageNumber">
                      <b-link class="page" href="#">{{ pageNumber }}</b-link>
                    </li>
                  </ul>
                  <b-link class="page-item pagination-next" href="#" @click="page++" v-if="page < pages.length">
                    Next
                  </b-link>
                </div>
              </div>
            </div>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>

    <!-- Modal -->
    <b-modal v-model="createApiModal" id="showModal" title-class="exampleModalLabel" hide-footer class="v-modal-custom"
      centered no-close-on-backdrop>
      <b-form autocomplete="off" id="addform">
        <div id="api-key-error-msg" class="alert alert-danger py-2 d-none">Please enter api key name</div>
        <input type="hidden" id="apikeyId">
        <div class="mb-3">
          <label for="api-key-name" class="form-label">API Key Name <span class="text-danger">*</span></label>
          <input type="text" class="form-control" id="api-key-name" placeholder="Enter api key name">
        </div>
        <div class="mb-3" id="apikey-element" style="display: none;">
          <label for="api-key" class="form-label">API Key</label>
          <input type="text" class="form-control" id="api-key" disabled value="b5815DE8A7224438932eb296Z5">
        </div>
      </b-form>
      <div class="hstack gap-2 justify-content-end mt-3">
        <b-button type="button" variant="secondary" @click="createApiModal = false" id="close-modal">Close</b-button>
        <button type="button" class="btn btn-primary" id="createApimodal-btn"
          @click="(e) => handleApikeydetails(e)">Create API</button>
        <b-button type="button" variant="primary" id="add-btn" @click="handleApiKeys">Add</b-button>
        <b-button type="button" variant="primary" id="edit-btn" @click="handleApiKeys">Save Changes</b-button>
      </div>
    </b-modal>
  </Layout>
</template>