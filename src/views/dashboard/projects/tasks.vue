<script>
export default {
  setup() {
    return {

    };
  },
};
</script>

<template>
  <b-card no-body>
    <b-card-header class="align-items-center d-flex">
      <b-card-title class="mb-0 flex-grow-1 py-1">My Tasks</b-card-title>
      <div class="flex-shrink-0">
        <div class="dropdown card-header-dropdown">
          <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown" aria-haspopup="true"
            aria-expanded="false">
            <span class="text-muted">All Tasks <i class="mdi mdi-chevron-down ms-1"></i></span>
          </b-link>
          <div class="dropdown-menu dropdown-menu-end">
            <b-link class="dropdown-item" href="#">All Tasks</b-link>
            <b-link class="dropdown-item" href="#">Completed </b-link>
            <b-link class="dropdown-item" href="#">Inprogress</b-link>
            <b-link class="dropdown-item" href="#">Pending</b-link>
          </div>
        </div>


      </div>
    </b-card-header>
    <b-card-body>
      <div class="table-responsive table-card">
        <table class="table table-borderless table-nowrap table-centered align-middle mb-0">
          <thead class="table-light text-muted">
            <tr>
              <th scope="col">Name</th>
              <th scope="col">Dedline</th>
              <th scope="col">Status</th>
              <th scope="col">Assignee</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask1" />
                  <label class="form-check-label ms-2" for="checkTask1">
                    Create new Admin Template
                  </label>
                </div>
              </td>
              <td class="text-muted">03 Nov 2021</td>
              <td><b-badge variant="soft-success" class="badge-soft-success">Completed</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Mary Stoner">
                  <img src="@/assets/images/users/avatar-2.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask2" />
                  <label class="form-check-label ms-2" for="checkTask2">
                    Marketing Coordinator
                  </label>
                </div>
              </td>
              <td class="text-muted">17 Nov 2021</td>
              <td><b-badge variant="soft-warning" class="badge-soft-warning">Progress</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Den Davis">
                  <img src="@/assets/images/users/avatar-7.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask3" />
                  <label class="form-check-label ms-2" for="checkTask3">
                    Administrative Analyst
                  </label>
                </div>
              </td>
              <td class="text-muted">26 Nov 2021</td>
              <td><b-badge variant="soft-success" class="badge-soft-success">Completed</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Alex Brown">
                  <img src="@/assets/images/users/avatar-6.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask4" />
                  <label class="form-check-label ms-2" for="checkTask4">
                    E-commerce Landing Page
                  </label>
                </div>
              </td>
              <td class="text-muted">10 Dec 2021</td>
              <td><b-badge variant="soft-danger" class="badge-soft-danger">Pending</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Prezy Morin">
                  <img src="@/assets/images/users/avatar-5.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask5" />
                  <label class="form-check-label ms-2" for="checkTask5">
                    UI/UX Design
                  </label>
                </div>
              </td>
              <td class="text-muted">22 Dec 2021</td>
              <td><b-badge variant="soft-warning" class="badge-soft-warning">Progress</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Stine Nielsen">
                  <img src="@/assets/images/users/avatar-1.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
            <tr>
              <td>
                <div class="form-check">
                  <input class="form-check-input fs-15" type="checkbox" value="" id="checkTask6" />
                  <label class="form-check-label ms-2" for="checkTask6">
                    Projects Design
                  </label>
                </div>
              </td>
              <td class="text-muted">31 Dec 2021</td>
              <td><b-badge variant="soft-danger" class="badge-soft-danger">Pending</b-badge></td>
              <td>
                <b-link href="javascript: void(0);" class="d-inline-block" data-bs-toggle="tooltip"
                  data-bs-placement="top" title="" data-bs-original-title="Jansh William">
                  <img src="@/assets/images/users/avatar-4.jpg" alt="" class="rounded-circle avatar-xxs" />
                </b-link>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="mt-3 text-center">
        <b-link href="javascript:void(0);" class="text-muted text-decoration-underline">Load More</b-link>
      </div>
    </b-card-body>
  </b-card>
</template>
