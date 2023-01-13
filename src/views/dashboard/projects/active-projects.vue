<script>
export default {
  setup() {
    return {
      activeProjects: [
        {
          id: 1,
          projectName: "Brand Logo Design",
          img: require("@/assets/images/users/avatar-1.jpg"),
          projectLead: "Donald Risher",
          percentage: "53%",
          subItem: [
            { id: 1, assImg: require("@/assets/images/users/avatar-1.jpg") },
            { id: 2, assImg: require("@/assets/images/users/avatar-2.jpg") },
            { id: 3, assImg: require("@/assets/images/users/avatar-3.jpg") },
          ],
          badge: "Inprogress",
          badgeClass: "warning",
          dueDate: "06 Sep 2021",
        },
        {
          id: 2,
          projectName: "Redesign - Landing Page",
          img: require("@/assets/images/users/avatar-2.jpg"),
          projectLead: "Prezy William",
          percentage: "0%",
          subItem: [
            { id: 1, assImg: require("@/assets/images/users/avatar-5.jpg") },
            { id: 2, assImg: require("@/assets/images/users/avatar-6.jpg") },
          ],
          badge: "Pending",
          badgeClass: "danger",
          dueDate: "13 Nov 2021",
        },
        {
          id: 3,
          projectName: "Multipurpose Landing Template",
          img: require("@/assets/images/users/avatar-3.jpg"),
          projectLead: "Boonie Hoynas",
          percentage: "100%",
          subItem: [
            { id: 1, assImg: require("@/assets/images/users/avatar-1.jpg") },
            { id: 2, assImg: require("@/assets/images/users/avatar-2.jpg") },
          ],
          badge: "Completed",
          badgeClass: "success",
          dueDate: "26 Nov 2021",
        },
        {
          id: 4,
          projectName: "Chat Application",
          img: require("@/assets/images/users/avatar-5.jpg"),
          projectLead: "Pauline Moll",
          percentage: "64%",
          subItem: [
            { id: 1, assImg: require("@/assets/images/users/avatar-2.jpg") },
          ],
          badge: "Progress",
          badgeClass: "warning",
          dueDate: "15 Dec 2021",
        },
        {
          id: 5,
          projectName: "Create Wireframe",
          img: require("@/assets/images/users/avatar-6.jpg"),
          projectLead: "James Bangs",
          percentage: "77%",
          subItem: [
            { id: 1, assImg: require("@/assets/images/users/avatar-1.jpg") },
            { id: 2, assImg: require("@/assets/images/users/avatar-6.jpg") },
            { id: 3, assImg: require("@/assets/images/users/avatar-4.jpg") },
          ],
          badge: "Progress",
          badgeClass: "warning",
          dueDate: "21 Dec 2021",
        },
      ],
    };
  },
};
</script>

<template>
  <b-card no-body>
    <b-card-header class="d-flex align-items-center">
      <b-card-title class="flex-grow-1 mb-0">Active Projects</b-card-title>
      <div class="flex-shrink-0">
        <b-link href="javascript:void(0);" class="btn btn-soft-info btn-sm">Export Report</b-link>
      </div>
    </b-card-header>
    <b-card-body>
      <div class="table-responsive table-card">
        <table class="table table-nowrap table-centered align-middle">
          <thead class="bg-light text-muted">
            <tr>
              <th scope="col">Project Name</th>
              <th scope="col">Project Lead</th>
              <th scope="col">Progress</th>
              <th scope="col">Assignee</th>
              <th scope="col">Status</th>
              <th scope="col" style="width: 10%">Due Date</th>
            </tr>
          </thead>

          <tbody>
            <tr v-for="(item, index) of activeProjects" :key="index">
              <td class="fw-medium">{{ item.projectName }}</td>
              <td>
                <img :src="item.img" class="avatar-xxs rounded-circle me-1" alt="" />
                <b-link href="javascript: void(0);" class="text-reset">{{ item.projectLead }}</b-link>
              </td>
              <td>
                <div class="d-flex align-items-center">
                  <div class="flex-shrink-0 me-1 text-muted fs-13">{{ item.percentage }}</div>
                  <b-progress class="progress-sm flex-grow-1 rounded" :value="53" variant="primary" />
                </div>
              </td>
              <td>
                <div class="avatar-group flex-nowrap">
                  <div class="avatar-group-item" v-for="(subitem, index) of item.subItem" :key="index">
                    <b-link href="javascript: void(0);" class="d-inline-block">
                      <img :src="subitem.assImg" alt="" class="rounded-circle avatar-xxs" />
                    </b-link>
                  </div>
                </div>
              </td>
              <td><span :class="`badge badge-soft-${item.badgeClass}`">{{ item.badge }}</span></td>
              <td class="text-muted">{{ item.dueDate }}</td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="align-items-center mt-xl-3 mt-4 justify-content-between d-flex">
        <div class="flex-shrink-0">
          <div class="text-muted">
            Showing <span class="fw-semibold">5</span> of
            <span class="fw-semibold">25</span> Results
          </div>
        </div>
        <ul class="pagination pagination-separated pagination-sm mb-0">
          <li class="page-item disabled">
            <b-link href="#" class="page-link">←</b-link>
          </li>
          <li class="page-item">
            <b-link href="#" class="page-link">1</b-link>
          </li>
          <li class="page-item active">
            <b-link href="#" class="page-link">2</b-link>
          </li>
          <li class="page-item">
            <b-link href="#" class="page-link">3</b-link>
          </li>
          <li class="page-item">
            <b-link href="#" class="page-link">→</b-link>
          </li>
        </ul>
      </div>
    </b-card-body>
  </b-card>
</template>
