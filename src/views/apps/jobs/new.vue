<script>
import Layout from "../../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../../app.config";

export default {
  page: {
    title: "New Job",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "New Job",
      items: [
        {
          text: "Jobs",
          href: "/",
        },
        {
          text: "New Job",
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
        <b-card no-body>
          <b-form action="#">
            <b-card-header>
              <h5 class="card-title mb-0">Create Job</h5>
            </b-card-header>
            <b-card-body>
              <b-row class="g-4">
                <b-col lg="6">
                  <div>
                    <label for="job-title-Input" class="form-label">Job Title <span class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="job-title-Input" placeholder="Enter job title"
                      required />
                  </div>
                </b-col>
                <b-col lg="6">
                  <div>
                    <label for="job-position-Input" class="form-label">Job Position <span
                        class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="job-position-Input" placeholder="Enter job position"
                      required />
                  </div>
                </b-col>
                <b-col lg="6">
                  <div>
                    <label for="job-category-Input" class="form-label">Job Category <span
                        class="text-danger">*</span></label>
                    <select class="form-control" data-choices name="job-category-Input" required>
                      <option value="">Select Category</option>
                      <option value="Accounting & Finance">Accounting & Finance</option>
                      <option value="Purchasing Manager">Purchasing Manager</option>
                      <option value="Education & training">Education & training</option>
                      <option value="Marketing & Advertising">Marketing & Advertising</option>
                      <option value="It / Software Jobs">It / Software Jobs</option>
                      <option value="Digital Marketing">Digital Marketing</option>
                      <option value="Administrative Officer">Administrative Officer</option>
                      <option value="Government Jobs">Government Jobs</option>
                    </select>
                  </div>
                </b-col>
                <b-col lg="6">
                  <div>
                    <label for="job-type-Input" class="form-label">Job Type <span class="text-danger">*</span></label>
                    <select class="form-control" data-choices name="job-type-Input" required>
                      <option value="">Select job type</option>
                      <option value="Full Time">Full Time</option>
                      <option value="Part Time">Part Time</option>
                      <option value="Freelance">Freelance</option>
                      <option value="Intership">Intership</option>
                    </select>
                  </div>
                </b-col>

                <b-col lg="12">
                  <div>
                    <label for="description-field" class="form-label">Description <span
                        class="text-danger">*</span></label>
                    <textarea class="form-control" id="description-field" rows="3" placeholder="Enter description"
                      required></textarea>
                  </div>
                </b-col>

                <b-col md="6">
                  <div>
                    <label for="vancancy-Input" class="form-label">No. of Vancancy <span
                        class="text-danger">*</span></label>
                    <input type="number" class="form-control" id="vancancy-Input" placeholder="No. of vancancy"
                      required />
                  </div>
                </b-col>
                <b-col md="6">
                  <div>
                    <label for="experience-Input" class="form-label">Experience <span
                        class="text-danger">*</span></label>
                    <select class="form-control" data-choices name="experience-Input">
                      <option value="">Select Experience</option>
                      <option value="0 Year">0 Year</option>
                      <option value="2 Yeasr">2 Years</option>
                      <option value="3 Years">3 Years</option>
                      <option value="4 Years">4 Years</option>
                      <option value="5 Years">5 Years</option>
                    </select>
                  </div>
                </b-col>

                <b-col lg="6">
                  <div>
                    <label for="last-apply-date-Input" class="form-label">Last Date of Apply <span
                        class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="last-apply-date-Input" data-provider="flatpickr"
                      data-date-format="d M, Y" placeholder="Select date" required />
                  </div>
                </b-col>

                <b-col lg="6">
                  <div>
                    <label for="close-date-Input" class="form-label">Close Date <span
                        class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="close-date-Input" data-provider="flatpickr"
                      data-date-format="d M, Y" placeholder="Select date" required />
                  </div>
                </b-col>

                <b-col md="6">
                  <div>
                    <label for="start-salary-Input" class="form-label">Start Salary</label>
                    <input type="number" class="form-control" id="start-salary-Input" placeholder="Enter start salary"
                      required />
                  </div>
                </b-col>

                <b-col md="6">
                  <div>
                    <label for="last-salary-Input" class="form-label">Last Salary</label>
                    <input type="number" class="form-control" id="last-salary-Input" placeholder="Enter end salary"
                      required />
                  </div>
                </b-col>

                <b-col md="6">
                  <div>
                    <label for="country-Input" class="form-label">Country <span class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="country-Input" placeholder="Enter country" required />
                  </div>
                </b-col>

                <b-col md="6">
                  <div>
                    <label for="city-Input" class="form-label">State <span class="text-danger">*</span></label>
                    <input type="text" class="form-control" id="city-Input" placeholder="Enter city" required />
                  </div>
                </b-col>

                <b-col lg="12">
                  <div>
                    <label for="website-field" class="form-label">Tags</label>
                    <input class="form-control" id="choices-text-unique-values" data-choices
                      data-choices-text-unique-true type="text" value="Design, Remote" required />
                  </div>
                </b-col>

                <b-col lg="12">
                  <div class="hstack justify-content-end gap-2">
                    <b-button type="button" variant="ghost-danger"><i class="ri-close-line align-bottom"></i>
                      Cancel</b-button>
                    <b-button type="submit" variant="primary">Add Job</b-button>
                  </div>
                </b-col>
              </b-row>
            </b-card-body>
          </b-form>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>