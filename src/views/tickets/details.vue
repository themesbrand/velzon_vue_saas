<script>
import Multiselect from "@vueform/multiselect";
import "@vueform/multiselect/themes/default.css";

import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Tickets Details",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
        };
    },
    components: {
        Layout,
        PageHeader,
        Multiselect,
    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row class="mt-n4">
            <b-col lg="12">
                <b-card no-body class="mt-n4 mx-n4 mb-n5">
                    <div class="bg-soft-warning">
                        <b-card-body class="pb-4 mb-5">
                            <b-row>
                                <b-col md>
                                    <b-row class="align-items-center">
                                        <b-col md="auto">
                                            <div class="avatar-md mb-md-0 mb-4">
                                                <div class="avatar-title bg-white rounded-circle">
                                                    <img src="@/assets/images/companies/img-4.png" alt=""
                                                        class="avatar-sm" />
                                                </div>
                                            </div>
                                        </b-col>
                                        <b-col md>
                                            <h4 class="fw-semibold">#VLZ135 - Create an Excellent UI for a Dashboard
                                            </h4>
                                            <div class="hstack gap-3 flex-wrap">
                                                <div class="text-muted"><i
                                                        class="ri-building-line align-bottom me-1"></i> Themesbrand
                                                </div>
                                                <div class="vr"></div>
                                                <div class="text-muted">Create Date : <span class="fw-medium">20 Dec,
                                                        2021</span></div>
                                                <div class="vr"></div>
                                                <div class="text-muted">Due Date : <span class="fw-medium">29 Dec,
                                                        2021</span></div>
                                                <div class="vr"></div>
                                                <b-badge pill class="bg-info fs-12">New</b-badge>
                                                <b-badge pill variant="danger" class="fs-12">High</b-badge>
                                            </div>
                                        </b-col>
                                    </b-row>
                                </b-col>
                                <b-col md="auto" class="mt-md-0 mt-4">
                                    <div class="hstack gap-1 flex-wrap">
                                        <button type="button" class="btn avatar-xs mt-n1 p-0 favourite-btn active">
                                            <span class="avatar-title bg-transparent fs-15">
                                                <i class="ri-star-fill"></i>
                                            </span>
                                        </button>
                                        <b-dropdown variant="transparent" toggle-class="fs-16 text-body arrow-none"
                                            size="sm" no-caret>
                                            <template #button-content> <i class="ri-share-line"></i>
                                            </template>
                                            <b-dropdown-item href="/apps/tickets-details">
                                                <i class="ri-eye-fill align-bottom me-2 text-muted"></i> View
                                            </b-dropdown-item>
                                            <b-dropdown-item href="#" @click="editdata(data)">
                                                <i class="ri-share-forward-fill align-bottom me-2 text-muted"></i> Share
                                                with
                                            </b-dropdown-item>
                                            <b-dropdown-item href="#" @click="deletedata(data)">
                                                <i class="ri-delete-bin-fill align-bottom me-2 text-muted"></i> Delete
                                            </b-dropdown-item>
                                        </b-dropdown>
                                        <button type="button" class="btn py-0 fs-16 text-body">
                                            <i class="ri-flag-line"></i>
                                        </button>
                                    </div>
                                </b-col>
                            </b-row>
                        </b-card-body>
                    </div>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col xxl="9">
                <b-card no-body>
                    <b-card-body class="p-4">
                        <h6 class="text-uppercase mb-3">Ticket Discripation</h6>
                        <p class="text-muted">It would also help to know what the errors are - it could be something
                            simple like a message saying delivery is not available which could be a problem with your
                            shipping templates. Too much or too little spacing, as in the example below, can make things
                            unpleasant for the reader. The goal is to make your text as comfortable to read as possible.
                            On the note of consistency, color consistency is a MUST. If you’re not trying to create
                            crazy contrast in your design, then a great idea would be for you to use a color palette
                            throughout your entire design. It will subconsciously interest viewers and also is very
                            pleasing to look at. <b-link href="javascript:void(0);"
                                class="link-secondary text-decoration-underline">Example</b-link>
                        </p>
                        <h6 class="text-uppercase mb-3">Create an Excellent UI for a Dashboard</h6>
                        <ul class="text-muted vstack gap-2 mb-4">
                            <li>Pick a Dashboard Type</li>
                            <li>Categorize information when needed</li>
                            <li>Provide Context</li>
                            <li>On using colors</li>
                            <li>On using the right graphs</li>
                        </ul>
                        <div class="mt-4">
                            <h6 class="text-uppercase mb-3">Here is the code you've requsted</h6>
                            <div>
                                <pre class="language-markup rounded-2"><code>var app = document.getElementById(&quot;app&quot;);
var run = (model) =&gt; get(model, &quot;users&quot;, () =&gt;
get(model, &quot;posts&quot;,
() =&gt; {
model.users.forEach(user =&gt; model.userIdx[user.id] = user);
app.innerText = '';
model.posts.forEach(post =&gt;
app.appendChild(renderPost(post, model.userIdx[post.userId])));
}));
app.appendChild(Wrapper.generate(&quot;button&quot;, &quot;Load&quot;).click(() =&gt; run({
userIdx: {}
})).element);</code></pre>
                            </div>
                        </div>
                    </b-card-body>
                    <b-card-body class="p-4">
                        <h5 class="card-title mb-4">Comments</h5>

                        <div data-simplebar style="height: 300px;" class="px-3 mx-n3">
                            <div class="d-flex mb-4">
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-8.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h5 class="fs-13">Joseph Parker <small class="text-muted">20 Dec 2021 -
                                            05:47AM</small></h5>
                                    <p class="text-muted">I am getting message from customers that when they place order
                                        always get error message .</p>
                                    <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                            class="mdi mdi-reply"></i> Reply</b-link>
                                    <div class="d-flex mt-4">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">Alexis Clarke <small class="text-muted">22 Dec 2021 -
                                                    02:32PM</small></h5>
                                            <p class="text-muted">Please be sure to check your Spam mailbox to see if
                                                your email filters have identified the email from Dell as spam.</p>
                                            <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                                    class="mdi mdi-reply"></i> Reply</b-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="d-flex mb-4">
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h5 class="fs-13">Donald Palmer <small class="text-muted">24 Dec 2021 -
                                            05:20PM</small></h5>
                                    <p class="text-muted">If you have further questions, please contact Customer Support
                                        from the “Action Menu” on your <b-link href="javascript:void(0);"
                                            class="text-decoration-underline">Online Order Support</b-link>.</p>
                                    <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                            class="mdi mdi-reply"></i> Reply</b-link>
                                </div>
                            </div>
                            <div class="d-flex">
                                <div class="flex-shrink-0">
                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                        class="avatar-xs rounded-circle" />
                                </div>
                                <div class="flex-grow-1 ms-3">
                                    <h5 class="fs-13">Alexis Clarke <small class="text-muted">26 min ago</small></h5>
                                    <p class="text-muted">Your <b-link href="javascript:void(0)"
                                            class="text-decoration-underline">Online Order Support</b-link> provides you
                                        with
                                        the most current status of your order. To help manage your order refer to the
                                        “Action Menu” to initiate return, contact Customer Support and more.</p>
                                    <b-row class="g-2 mb-3">
                                        <b-col lg="1" sm="2" cols="6">
                                            <img src="@/assets/images/small/img-4.jpg" alt="" class="img-fluid rounded">
                                        </b-col>
                                        <b-col lg="1" sm="2" cols="6">
                                            <img src="@/assets/images/small/img-5.jpg" alt="" class="img-fluid rounded">
                                        </b-col>
                                    </b-row>
                                    <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                            class="mdi mdi-reply"></i> Reply</b-link>
                                    <div class="d-flex mt-4">
                                        <div class="flex-shrink-0">
                                            <img src="@/assets/images/users/avatar-6.jpg" alt=""
                                                class="avatar-xs rounded-circle" />
                                        </div>
                                        <div class="flex-grow-1 ms-3">
                                            <h5 class="fs-13">Donald Palmer <small class="text-muted">8 sec ago</small>
                                            </h5>
                                            <p class="text-muted">Other shipping methods are available at checkout if
                                                you want your purchase delivered faster.</p>
                                            <b-link href="javascript: void(0);" class="badge text-muted bg-light"><i
                                                    class="mdi mdi-reply"></i> Reply</b-link>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <form action="javascript:void(0);" class="mt-3">
                            <b-row class="g-3">
                                <b-col lg="12">
                                    <label for="exampleFormControlTextarea1" class="form-label">Leave a Comments</label>
                                    <textarea class="form-control bg-light border-light"
                                        id="exampleFormControlTextarea1" rows="3"
                                        placeholder="Enter comments"></textarea>
                                </b-col>
                                <b-col lg="12" class="text-end">
                                    <b-link href="javascript:void(0);" class="btn btn-success">Post Comments</b-link>
                                </b-col>
                            </b-row>
                        </form>
                    </b-card-body>
                </b-card>
            </b-col>
            <b-col xxl="3">
                <b-card no-body>
                    <b-card-header>
                        <h5 class="card-title mb-0">Ticket Details</h5>
                    </b-card-header>
                    <b-card-body>
                        <div class="table-responsive table-card">
                            <table class="table table-borderless align-middle mb-0">
                                <tbody>
                                    <tr>
                                        <td class="fw-medium">Ticket</td>
                                        <td>#VLZ135</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Client</td>
                                        <td>Themesbrand</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Project</td>
                                        <td>Velzon - Admin Dashboard</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Assigned To:</td>
                                        <td>
                                            <div class="avatar-group">
                                                <b-link href="javascript:void(0);" class="avatar-group-item"
                                                    v-b-tooltip.hover title="Erica Kernan">
                                                    <img src="@/assets/images/users/avatar-4.jpg" alt=""
                                                        class="rounded-circle avatar-xs" />
                                                </b-link>
                                                <b-link href="javascript:void(0);" class="avatar-group-item"
                                                    v-b-tooltip.hover title="Alexis Clarke">
                                                    <img src="@/assets/images/users/avatar-10.jpg" alt=""
                                                        class="rounded-circle avatar-xs" />
                                                </b-link>
                                                <b-link href="javascript:void(0);" class="avatar-group-item"
                                                    v-b-tooltip.hover title="James Price">
                                                    <img src="@/assets/images/users/avatar-3.jpg" alt=""
                                                        class="rounded-circle avatar-xs" />
                                                </b-link>
                                                <b-link href="javascript: void(0);" class="avatar-group-item"
                                                    v-b-tooltip.hover title="Add Members">
                                                    <div class="avatar-xs">
                                                        <div
                                                            class="avatar-title fs-16 rounded-circle bg-light border-dashed border text-primary">
                                                            +
                                                        </div>
                                                    </div>
                                                </b-link>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Status:</td>
                                        <td>
                                            <Multiselect v-model="value" :close-on-select="true" :searchable="true"
                                                :create-option="true" :options="[
                                                    { value: 'new', label: 'New' },
                                                    { value: 'open', label: 'Open' },
                                                    { value: 'inprogress', label: 'Inprogress' },
                                                    { value: 'closed', label: 'Closed' }
                                                ]" />
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Priority</td>
                                        <td>
                                            <b-badge variant="danger">High</b-badge>
                                        </td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Create Date</td>
                                        <td>20 Dec, 2021</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Due Date</td>
                                        <td>29 Dec, 2021</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Last Activity</td>
                                        <td>14 min ago</td>
                                    </tr>
                                    <tr>
                                        <td class="fw-medium">Labels</td>
                                        <td class="hstack text-wrap gap-1">
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Admin</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">UI</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Dashboard</b-badge>
                                            <b-badge variant="soft-primary" class="badge-soft-primary">Design</b-badge>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </b-card-body>
                </b-card>
                <b-card no-body>
                    <b-card-header>
                        <h6 class="card-title fw-semibold mb-0">Files Attachment</h6>
                    </b-card-header>
                    <b-card-body>
                        <div class="d-flex align-items-center border border-dashed p-2 rounded">
                            <div class="flex-shrink-0 avatar-sm">
                                <div class="avatar-title bg-light rounded">
                                    <i class="ri-file-zip-line fs-20 text-primary"></i>
                                </div>
                            </div>
                            <div class="flex-grow-1 ms-3">
                                <h6 class="mb-1">
                                    <b-link href="javascript:void(0);" class="text-body">Velzon-admin.zip</b-link>
                                </h6>
                                <small class="text-muted">3.2 MB</small>
                            </div>
                            <div class="hstack gap-3 fs-16">
                                <b-link href="javascript:void(0);" class="text-muted"><i class="ri-download-2-line"></i>
                                </b-link>
                                <b-link href="javascript:void(0);" class="text-muted"><i class="ri-delete-bin-line"></i>
                                </b-link>
                            </div>
                        </div>
                        <div class="d-flex  align-items-center border border-dashed p-2 rounded mt-2">
                            <div class="flex-shrink-0 avatar-sm">
                                <div class="avatar-title bg-light rounded">
                                    <i class="ri-file-ppt-2-line fs-20 text-danger"></i>
                                </div>
                            </div>
                            <div class="flex-grow-1 ms-3">
                                <h6 class="mb-1">
                                    <b-link href="javascript:void(0);" class="text-body">Velzon-admin.ppt</b-link>
                                </h6>
                                <small class="text-muted">4.5 MB</small>
                            </div>
                            <div class="hstack gap-3 fs-16">
                                <b-link href="javascript:void(0);" class="text-muted"><i class="ri-download-2-line"></i>
                                </b-link>
                                <b-link href="javascript:void(0);" class="text-muted"><i class="ri-delete-bin-line"></i>
                                </b-link>
                            </div>
                        </div>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>