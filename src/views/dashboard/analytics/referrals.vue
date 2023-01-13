<script>
export default {

};
</script>

<template>
    <b-card no-body class="card-height-100">
        <b-card-header class="align-items-center d-flex">
            <b-card-title class="mb-0 flex-grow-1">Top Referrals Pages</b-card-title>
            <div class="flex-shrink-0">
                <b-button type="button" variant="soft-primary" size="sm">
                    Export Report
                </b-button>
            </div>
        </b-card-header>

        <b-card-body>

            <b-row class="align-items-center">
                <b-col cols="6">
                    <h6 class="text-muted text-uppercase fw-semibold text-truncate fs-12 mb-3">Total Referrals Page</h6>
                    <h4 class="fs- mb-0">725,800</h4>
                    <p class="mb-0 mt-2 text-muted"><b-badge variant="soft-success" class="badge-soft-success mb-0">
                            <i class="ri-arrow-up-line align-middle"></i> 15.72 %
                        </b-badge> vs. previous month</p>
                </b-col>
                <b-col cols="6">
                    <div class="text-center">
                        <img src="@/assets/images/illustrator-1.png" class="img-fluid" alt="">
                    </div>
                </b-col>
            </b-row>
            <div class="mt-3 pt-2">

                <b-progress class="progress-lg rounded-pill">
                    <b-progress-bar :value="25" variant="primary" class="rounded-0" />
                    <b-progress-bar :value="18" variant="info" class="rounded-0" />
                    <b-progress-bar :value="22" variant="success" class="rounded-0" />
                    <b-progress-bar :value="16" variant="warning" class="rounded-0" />
                    <b-progress-bar :value="19" variant="danger" class="rounded-0" />
                  </b-progress>
            </div>

            <div class="mt-3 pt-2">
                <div class="d-flex mb-2">
                    <div class="flex-grow-1">
                        <p class="text-truncate text-muted fs-14 mb-0"><i
                                class="mdi mdi-circle align-middle text-primary me-2"></i>www.google.com</p>
                    </div>
                    <div class="flex-shrink-0">
                        <p class="mb-0">24.58%</p>
                    </div>
                </div>
                <div class="d-flex mb-2">
                    <div class="flex-grow-1">
                        <p class="text-truncate text-muted fs-14 mb-0"><i
                                class="mdi mdi-circle align-middle text-info me-2"></i>www.youtube.com</p>
                    </div>
                    <div class="flex-shrink-0">
                        <p class="mb-0">17.51%</p>
                    </div>
                </div>
                <div class="d-flex mb-2">
                    <div class="flex-grow-1">
                        <p class="text-truncate text-muted fs-14 mb-0"><i
                                class="mdi mdi-circle align-middle text-success me-2"></i>www.meta.com</p>
                    </div>
                    <div class="flex-shrink-0">
                        <p class="mb-0">23.05%</p>
                    </div>
                </div>
                <div class="d-flex mb-2">
                    <div class="flex-grow-1">
                        <p class="text-truncate text-muted fs-14 mb-0"><i
                                class="mdi mdi-circle align-middle text-warning me-2"></i>www.medium.com</p>
                    </div>
                    <div class="flex-shrink-0">
                        <p class="mb-0">12.22%</p>
                    </div>
                </div>
                <div class="d-flex">
                    <div class="flex-grow-1">
                        <p class="text-truncate text-muted fs-14 mb-0"><i
                                class="mdi mdi-circle align-middle text-danger me-2"></i>Other</p>
                    </div>
                    <div class="flex-shrink-0">
                        <p class="mb-0">17.58%</p>
                    </div>
                </div>
            </div>

            <div class="mt-2 text-center">
                <b-link href="javascript:void(0);" class="text-muted text-decoration-underline">Show All</b-link>
            </div>

        </b-card-body>
    </b-card>
</template>