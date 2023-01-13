<script>
import SwiperCore, { Autoplay, Thumbs, Pagination, Navigation } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/swiper-bundle.css";

SwiperCore.use([Autoplay, Thumbs, Pagination, Navigation]);

import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
  page: {
    title: "Swiper",
    meta: [{ name: "description", content: appConfig.description }],
  },
  data() {
    return {
      title: "Swiper Slider",
      items: [
        {
          text: "Advance UI",
          href: "/",
        },
        {
          text: "Swiper Slider",
          active: true,
        },
      ],
    };
  },
  components: {
    Layout,
    PageHeader,
    Swiper,
    SwiperSlide,
  },
};
</script>

<template>
  <Layout>
    <PageHeader :title="title" :items="items" />

    <b-row>
      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Default Swiper</b-card-title>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>default-swiper</code> class to set a default swiper.
            </p>
            <swiper class="default-swiper rounded" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }">
              <swiper-slide>
                <img src="@/assets/images/small/img-1.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-2.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-3.jpg" alt class="img-fluid" />
              </swiper-slide>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>
      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Navigation & Pagination Swiper</b-card-title>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>navigation-swiper</code> class to set a swiper with
              navigation and pagination.
            </p>
            <swiper class="navigation-swiper rounded" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :navigation="{
  nextEl: '.swiper-button-next',
  prevEl: '.swiper-button-prev',
}" :pagination="{
  clickable: true,
  el: '.swiper-pagination',
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-4.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-5.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-6.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-button-next"></div>
              <div class="swiper-button-prev"></div>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Pagination Dynamic Swiper</b-card-title>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>pagination-dynamic-swiper</code> class to set a dynamic
              swiper with pagination.
            </p>
            <swiper class="pagination-dynamic-swiper rounded" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  clickable: true,
  el: '.swiper-pagination',
  dynamicBullets: true,
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-7.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-8.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-9.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination dynamic-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Pagination Fraction Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>pagination-fraction-swiper</code> class to set a
              fraction swiper with pagination.
            </p>
            <swiper class="pagination-fraction-swiper" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  clickable: true,
  el: '.swiper-pagination',
  type: 'fraction',
}" :navigation="{
  nextEl: '.swiper-button-next',
  prevEl: '.swiper-button-prev',
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-10.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-11.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-12.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-button-next"></div>
              <div class="swiper-button-prev"></div>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Pagination Custom Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>pagination-custom-swiper</code> class to set a swiper
              with custom pagination.
            </p>
            <swiper class="pagination-custom-swiper rounded" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  clickable: true,
  el: '.swiper-pagination',
  renderBullet: function (index, className) {
    return '<span class=' + className + '>' + (index + 1) + '</span>';
  },
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-2.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-3.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-4.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination pagination-custom"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Pagination Progress Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>pagination-progress-swiper</code> class to set a swiper
              with progress pagination.
            </p>
            <swiper class="pagination-progress-swiper rounded" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  clickable: true,
  el: '.swiper-pagination',
  type: 'fraction',
}" :navigation="{
  nextEl: '.swiper-button-next',
  prevEl: '.swiper-button-prev',
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-5.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-6.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-7.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-button-next"></div>
              <div class="swiper-button-prev"></div>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Scrollbar Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>pagination-scrollbar-swiper</code> class to set a swiper
              with scrollbar pagination.
            </p>
            <swiper class="pagination-scrollbar-swiper rounded" :loop="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :scrollbar="{
  el: '.swiper-scrollbar',
  hide: true,
}" :navigation="{
  nextEl: '.swiper-button-next',
  prevEl: '.swiper-button-prev',
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-8.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-9.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-10.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-button-next"></div>
              <div class="swiper-button-prev"></div>
              <div class="swiper-scrollbar"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Vertical Swiper</b-card-title>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>vertical-swiper</code> class to set a vertical swiper.
            </p>
            <swiper class="vertical-swiper rounded" :loop="true" :direction="'vertical'" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
}" style="height: 324px">
              <swiper-slide>
                <img src="@/assets/images/small/img-11.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-12.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-1.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>


      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Mousewheel Control Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>mousewheel-control-swiper</code> class to set a swiper
              with mousewheel scroll.
            </p>
            <swiper class="mousewheel-control-swiper rounded" :loop="true" :direction="'vertical'" :mousewheel="true"
              :autoplay="{
                delay: 2500,
                disableOnInteraction: false,
              }" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
}" style="height: 324px">
              <swiper-slide>
                <img src="@/assets/images/small/img-3.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-4.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-5.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>


      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Effect Fade Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>effect-fade-swiper</code> class to set a swiper with
              fade effect.
            </p>
            <swiper class="effect-fade-swiper rounded" :loop="true" :effect="'fade'" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-6.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-7.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-8.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Effect Creative Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>effect-creative-swiper</code> class to set a swiper with
              creative custom effect.
            </p>
            <swiper class="effect-creative-swiper rounded" :loop="true" :effect="'creative'" :creativeEffect="{
              prev: {
                shadow: true,
                translate: [0, 0, -400],
              },
              next: {
                translate: ['100%', 0, 0],
              },
            }" :autoplay="{
  delay: 2500,
  disableOnInteraction: false,
}" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
  dynamicBullets: true,
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-9.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-10.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-11.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col xl="4" lg="6">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Effect Flip Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>effect-flip-swiper</code> class to set a swiper with
              flip effect.
            </p>
            <swiper class="effect-flip-swiper rounded" :loop="true" :effect="'flip'" :grabCursor="true" :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-12.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-1.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-2.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>

      <b-col lg="12">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Effect Coverflow Swiper</b-card-title>
          </b-card-header>
          <b-card-body>
            <p class="text-muted">
              Use
              <code>effect-coverflow-swiper</code> class to set a swiper
              with coverflow effect.
            </p>
            <swiper class="effect-coverflow-swiper rounded pb-5" :loop="true" :effect="'coverflow'" :grabCursor="true"
              :centeredSlides="true" :slidesPerView="4" :coverflowEffect="{
                rotate: 50,
                stretch: 0,
                depth: 100,
                modifier: 1,
                slideShadows: true,
              }" :autoplay="{
  delay: 2500,
  disableOnInteraction: false,
}" :pagination="{
  el: '.swiper-pagination',
  clickable: true,
  dynamicBullets: true,
}">
              <swiper-slide>
                <img src="@/assets/images/small/img-4.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-5.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-6.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-7.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-8.jpg" alt class="img-fluid" />
              </swiper-slide>
              <swiper-slide>
                <img src="@/assets/images/small/img-9.jpg" alt class="img-fluid" />
              </swiper-slide>
              <div class="swiper-pagination swiper-pagination-dark"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>


      <b-col lg="12">
        <b-card no-body>
          <b-card-header>
            <b-card-title class="mb-0">Responsive Breakpoints Swiper</b-card-title>
          </b-card-header>

          <b-card-body>
            <p class="text-muted">
              Use
              <code>responsive-swiper</code> class to set a responsive
              swiper.
            </p>
            <swiper class="swiper responsive-swiper rounded gallery-light pb-4" :loop="true" :slidesPerView="1"
              :spaceBetween="10" :pagination="{
                el: '.swiper-pagination',
                clickable: true,
              }" :breakpoints="{
  640: {
    slidesPerView: 2,
    spaceBetween: 20,
  },
  768: {
    slidesPerView: 3,
    spaceBetween: 40,
  },
  1200: {
    slidesPerView: 4,
    spaceBetween: 50,
  },
}">
              <swiper-slide>
                <b-card no-body class="gallery-box">
                  <div class="gallery-container">
                    <b-link class="image-popup" href="assets/images/small/img-1.jpg" title>
                      <img class="gallery-img img-fluid mx-auto" src="@/assets/images/small/img-1.jpg" alt />
                      <div class="gallery-overlay">
                        <h5 class="overlay-caption">Glasses and laptop from above</h5>
                      </div>
                    </b-link>
                  </div>
                  <div class="box-content">
                    <div class="d-flex align-items-center mt-1">
                      <div class="flex-grow-1 text-muted">
                        by
                        <b-link href class="text-body text-truncate">Ron Mackie</b-link>
                      </div>
                      <div class="flex-shrink-0">
                        <div class="d-flex gap-3">
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-thumb-up-fill text-muted align-bottom me-1"></i>
                            2.2K
                          </b-button>
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-question-answer-fill text-muted align-bottom me-1"></i>
                            1.3K
                          </b-button>
                        </div>
                      </div>
                    </div>
                  </div>
                </b-card>
              </swiper-slide>
              <swiper-slide>
                <b-card no-body class="gallery-box">
                  <div class="gallery-container">
                    <b-link class="image-popup" href="assets/images/small/img-2.jpg" title>
                      <img class="gallery-img img-fluid mx-auto" src="@/assets/images/small/img-2.jpg" alt />
                      <div class="gallery-overlay">
                        <h5 class="overlay-caption">Working at a coffee shop</h5>
                      </div>
                    </b-link>
                  </div>
                  <div class="box-content">
                    <div class="d-flex align-items-center mt-1">
                      <div class="flex-grow-1 text-muted">
                        by
                        <b-link href class="text-body text-truncate">Nancy Martino</b-link>
                      </div>
                      <div class="flex-shrink-0">
                        <div class="d-flex gap-3">
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-thumb-up-fill text-muted align-bottom me-1"></i>
                            3.2K
                          </b-button>
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-question-answer-fill text-muted align-bottom me-1"></i>
                            1.1K
                          </b-button>
                        </div>
                      </div>
                    </div>
                  </div>
                </b-card>
              </swiper-slide>
              <swiper-slide>
                <div class="gallery-box card mb-0">
                  <div class="gallery-container">
                    <b-link class="image-popup" href="assets/images/small/img-10.jpg" title>
                      <img class="gallery-img img-fluid mx-auto" src="@/assets/images/small/img-10.jpg" alt />
                      <div class="gallery-overlay">
                        <h5 class="overlay-caption">Fun day at the Hill Station</h5>
                      </div>
                    </b-link>
                  </div>
                  <div class="box-content">
                    <div class="d-flex align-items-center mt-1">
                      <div class="flex-grow-1 text-muted">
                        by
                        <b-link href class="text-body text-truncate">Henry Baird</b-link>
                      </div>
                      <div class="flex-shrink-0">
                        <div class="d-flex gap-3">
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-thumb-up-fill text-muted align-bottom me-1"></i>
                            632
                          </b-button>
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-question-answer-fill text-muted align-bottom me-1"></i>
                            95
                          </b-button>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </swiper-slide>
              <swiper-slide>
                <b-card no-body class="gallery-box">
                  <div class="gallery-container">
                    <b-link class="image-popup" href="assets/images/small/img-4.jpg" title>
                      <img class="gallery-img img-fluid mx-auto" src="@/assets/images/small/img-4.jpg" alt />
                      <div class="gallery-overlay">
                        <h5 class="overlay-caption">Drawing a sketch</h5>
                      </div>
                    </b-link>
                  </div>
                  <div class="box-content">
                    <div class="d-flex align-items-center mt-1">
                      <div class="flex-grow-1 text-muted">
                        by
                        <b-link href class="text-body text-truncate">Jason McQuaid</b-link>
                      </div>
                      <div class="flex-shrink-0">
                        <div class="d-flex gap-3">
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-thumb-up-fill text-muted align-bottom me-1"></i>
                            825
                          </b-button>
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-question-answer-fill text-muted align-bottom me-1"></i>
                            101
                          </b-button>
                        </div>
                      </div>
                    </div>
                  </div>
                </b-card>
              </swiper-slide>
              <swiper-slide>
                <b-card no-body class="gallery-box">
                  <div class="gallery-container">
                    <b-link class="image-popup" href="assets/images/small/img-6.jpg" title>
                      <img class="gallery-img img-fluid mx-auto" src="@/assets/images/small/img-6.jpg" alt />
                      <div class="gallery-overlay">
                        <h5 class="overlay-caption">Project discussion with team</h5>
                      </div>
                    </b-link>
                  </div>
                  <div class="box-content">
                    <div class="d-flex align-items-center mt-1">
                      <div class="flex-grow-1 text-muted">
                        by
                        <b-link href class="text-body text-truncate">Erica Kernan</b-link>
                      </div>
                      <div class="flex-shrink-0">
                        <div class="d-flex gap-3">
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-thumb-up-fill text-muted align-bottom me-1"></i>
                            3.4K
                          </b-button>
                          <b-button variant="link" size="sm" type="button"
                            class="fs-12 text-body text-decoration-none px-0">
                            <i class="ri-question-answer-fill text-muted align-bottom me-1"></i>
                            1.3k
                          </b-button>
                        </div>
                      </div>
                    </div>
                  </div>
                </b-card>
              </swiper-slide>
              <div class="swiper-pagination swiper-pagination-dark"></div>
            </swiper>
          </b-card-body>
        </b-card>
      </b-col>
    </b-row>
  </Layout>
</template>
