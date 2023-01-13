<script>
export default {

};
</script>

<template>
    <b-card no-body class="card-height-100">
        <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Top Pages</b-card-title>
            <div class="flex-shrink-0">
                <div class="dropdown card-header-dropdown">
                    <b-link class="text-reset dropdown-btn" href="#" data-bs-toggle="dropdown" aria-haspopup="true"
                        aria-expanded="false">
                        <span class="text-muted fs-16"><i class="mdi mdi-dots-vertical align-middle"></i></span>
                    </b-link>
                    <div class="dropdown-menu dropdown-menu-end">
                        <b-link class="dropdown-item" href="#">Today</b-link>
                        <b-link class="dropdown-item" href="#">Last Week</b-link>
                        <b-link class="dropdown-item" href="#">Last Month</b-link>
                        <b-link class="dropdown-item" href="#">Current Year</b-link>
                    </div>
                </div>
            </div>
        </b-card-header>
        <b-card-body>
            <div class="table-responsive table-card">
                <table class="table align-middle table-borderless table-centered table-nowrap mb-0">
                    <thead class="text-muted table-light">
                        <tr>
                            <th scope="col" style="width: 62;">Active Page</th>
                            <th scope="col">Active</th>
                            <th scope="col">Users</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/themesbrand/skote-25867</b-link>
                            </td>
                            <td>99</td>
                            <td>25.3%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/dashonic/chat-24518</b-link>
                            </td>
                            <td>86</td>
                            <td>22.7%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/skote/timeline-27391</b-link>
                            </td>
                            <td>64</td>
                            <td>18.7%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/themesbrand/minia-26441</b-link>
                            </td>
                            <td>53</td>
                            <td>14.2%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/dashon/dashboard-29873</b-link>
                            </td>
                            <td>33</td>
                            <td>12.6%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/doot/chats-29964</b-link>
                            </td>
                            <td>20</td>
                            <td>10.9%</td>
                        </tr>
                        <tr>
                            <td>
                                <b-link href="javascript:void(0);">/minton/pages-29739</b-link>
                            </td>
                            <td>10</td>
                            <td>07.3%</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </b-card-body>
    </b-card>
</template>