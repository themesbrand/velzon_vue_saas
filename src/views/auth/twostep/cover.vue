<script>
export default {

};
</script>

<template>
    <div class="auth-page-wrapper auth-bg-cover py-5 d-flex justify-content-center align-items-center min-vh-100">
        <div class="bg-overlay"></div>
        <div class="auth-page-content overflow-hidden pt-lg-5">
            <b-container>
                <b-row>
                    <b-col lg="12">
                        <b-card no-body class="overflow-hidden">
                            <b-row class="justify-content-center g-0">
                                <b-col lg="6">
                                    <div class="p-lg-5 p-4 auth-one-bg h-100">
                                        <div class="bg-overlay"></div>
                                        <div class="position-relative h-100 d-flex flex-column">
                                            <div class="mb-4">
                                                <router-link to="/" class="d-block">
                                                    <img src="@/assets/images/logo-light.png" alt="" height="18">
                                                </router-link>
                                            </div>
                                            <div class="mt-auto">
                                                <div class="mb-3">
                                                    <i class="ri-double-quotes-l display-4 text-success"></i>
                                                </div>

                                                <div id="qoutescarouselIndicators" class="carousel slide"
                                                    data-bs-ride="carousel">
                                                    <div class="carousel-indicators">
                                                        <button type="button" data-bs-target="#qoutescarouselIndicators"
                                                            data-bs-slide-to="0" class="active" aria-current="true"
                                                            aria-label="Slide 1"></button>
                                                        <button type="button" data-bs-target="#qoutescarouselIndicators"
                                                            data-bs-slide-to="1" aria-label="Slide 2"></button>
                                                        <button type="button" data-bs-target="#qoutescarouselIndicators"
                                                            data-bs-slide-to="2" aria-label="Slide 3"></button>
                                                    </div>
                                                    <div class="carousel-inner text-center text-white-50 pb-5">
                                                        <div class="carousel-item active">
                                                            <p class="fs-15">" Great! Clean code, clean design, easy for
                                                                customization. Thanks very much! "</p>
                                                        </div>
                                                        <div class="carousel-item">
                                                            <p class="fs-15">" The theme is really great with an amazing
                                                                customer support."</p>
                                                        </div>
                                                        <div class="carousel-item">
                                                            <p class="fs-15">" Great! Clean code, clean design, easy for
                                                                customization. Thanks very much! "</p>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>
                                </b-col>

                                <b-col lg="6">
                                    <div class="p-lg-5 p-4">
                                        <div class="mb-4">
                                            <div class="avatar-lg mx-auto">
                                                <div
                                                    class="avatar-title bg-light text-primary display-5 rounded-circle">
                                                    <i class="ri-mail-line"></i>
                                                </div>
                                            </div>
                                        </div>
                                        <div class="text-muted text-center mx-lg-3">
                                            <h4 class="">Verify Your Email</h4>
                                            <p>Please enter the 4 digit code sent to <span
                                                    class="fw-semibold">example@abc.com</span></p>
                                        </div>

                                        <div class="mt-4">
                                            <form>
                                                <b-row>
                                                    <b-col cols="3">
                                                        <div class="mb-3">
                                                            <label for="digit1-input" class="visually-hidden">Dight
                                                                1</label>
                                                            <input type="text"
                                                                class="form-control form-control-lg bg-light border-light text-center"
                                                                onkeyup="moveToNext(this, 2)" maxLength="1"
                                                                id="digit1-input">
                                                        </div>
                                                    </b-col>

                                                    <b-col cols="3">
                                                        <div class="mb-3">
                                                            <label for="digit2-input" class="visually-hidden">Dight
                                                                2</label>
                                                            <input type="text"
                                                                class="form-control form-control-lg bg-light border-light text-center"
                                                                onkeyup="moveToNext(this, 3)" maxLength="1"
                                                                id="digit2-input">
                                                        </div>
                                                    </b-col>

                                                    <b-col cols="3">
                                                        <div class="mb-3">
                                                            <label for="digit3-input" class="visually-hidden">Dight
                                                                3</label>
                                                            <input type="text"
                                                                class="form-control form-control-lg bg-light border-light text-center"
                                                                onkeyup="moveToNext(this, 4)" maxLength="1"
                                                                id="digit3-input">
                                                        </div>
                                                    </b-col>

                                                    <b-col cols="3">
                                                        <div class="mb-3">
                                                            <label for="digit4-input" class="visually-hidden">Dight
                                                                4</label>
                                                            <input type="text"
                                                                class="form-control form-control-lg bg-light border-light text-center"
                                                                onkeyup="moveToNext(this, 4)" maxLength="1"
                                                                id="digit4-input">
                                                        </div>
                                                    </b-col>
                                                </b-row>

                                                <div class="mt-3">
                                                    <b-button type="button" variant="success" class="w-100">Confirm</b-button>
                                                </div>

                                            </form>

                                        </div>

                                        <div class="mt-5 text-center">
                                            <p class="mb-0">Didn't receive a code ? <router-link
                                                    to="/auth/reset-pwd-cover"
                                                    class="fw-semibold text-primary text-decoration-underline">Resend
                                                </router-link>
                                            </p>
                                        </div>
                                    </div>
                                </b-col>
                            </b-row>
                        </b-card>
                    </b-col>
                </b-row>
            </b-container>
        </div>

        <footer class="footer">
            <b-container>
                <b-row>
                    <b-col lg="12">
                        <div class="text-center">
                            <p class="mb-0">&copy; {{ new Date().getFullYear() }} Velzon. Crafted with <i
                                    class="mdi mdi-heart text-danger"></i> by Themesbrand</p>
                        </div>
                    </b-col>
                </b-row>
            </b-container>
        </footer>
    </div>
</template>