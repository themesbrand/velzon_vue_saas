<script>
import animationData from "@/components/widgets/spxnqpau.json";
import Lottie from "@/components/widgets/lottie.vue";

export default {
    data() {
        return {
            defaultOptions: { animationData: animationData },
        };
    },
    components: {
        lottie: Lottie
    }
};
</script>

<template>
    <div class="auth-page-wrapper auth-bg-cover py-5 d-flex justify-content-center align-items-center min-vh-100">
        <div class="bg-overlay"></div>
        <div class="auth-page-content overflow-hidden pt-lg-5">
            <b-container>
                <b-row class="justify-content-center">
                    <b-col xl="5">
                        <b-card no-body class="overflow-hidden">
                            <b-card-body class="p-4">
                                <div class="text-center">
                                    <lottie colors="primary:#405189,secondary:#0ab39c" :options="defaultOptions"
                                        style="height:7.5rem;width:7.5rem;" />
                                    <h1 class="text-primary mb-4">Oops !</h1>
                                    <h4 class="text-uppercase">Sorry, Page not Found 😭</h4>
                                    <p class="text-muted mb-4">The page you are looking for not available!</p>
                                    <router-link to="/" class="btn btn-success"><i class="mdi mdi-home me-1"></i>Back to
                                        home</router-link>
                                </div>
                            </b-card-body>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </div>
    </div>
</template>