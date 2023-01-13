<script>
// import {
//   SimpleBar
// } from "simplebar-vue3";

import i18n from "../i18n";

/**
 * Nav-bar Component
 */
export default {
  data() {
    return {
      languages: [{
        flag: require("@/assets/images/flags/us.svg"),
        language: "en",
        title: "English",
      },
      {
        flag: require("@/assets/images/flags/spain.svg"),
        language: "sp",
        title: "Española",
      },
      {
        flag: require("@/assets/images/flags/germany.svg"),
        language: "gr",
        title: "Deutsche",
      },
      {
        flag: require("@/assets/images/flags/italy.svg"),
        language: "it",
        title: "italiana",
      },
      {
        flag: require("@/assets/images/flags/russia.svg"),
        language: "ru",
        title: "русский",
      },
      {
        flag: require("@/assets/images/flags/china.svg"),
        language: "ch",
        title: "中國人",
      },
      {
        flag: require("@/assets/images/flags/french.svg"),
        language: "fr",
        title: "Français",
      },
      {
        flag: require("@/assets/images/flags/ae.svg"),
        language: "ar",
        title: "Arabic",
      },
      ],
      lan: i18n.locale,
      text: null,
      flag: null,
      value: null,
      myVar: 1,
    };
  },
  components: {
    // SimpleBar
  },

  methods: {

    isCustomDropdown() {
      //Search bar
      
    },
    toggleHamburgerMenu() {
      var windowSize = document.documentElement.clientWidth;

      if (windowSize > 767)
        document.querySelector(".hamburger-icon").classList.toggle("open");

      //For collapse horizontal menu
      if (
        document.documentElement.getAttribute("data-layout") === "horizontal"
      ) {
        document.body.classList.contains("menu") ?
          document.body.classList.remove("menu") :
          document.body.classList.add("menu");
      }

      //For collapse vertical menu
      if (document.documentElement.getAttribute("data-layout") === "vertical") {
        if (windowSize < 1025 && windowSize > 767) {
          document.body.classList.remove("vertical-sidebar-enable");
          document.documentElement.getAttribute("data-sidebar-size") == "sm" ?
            document.documentElement.setAttribute("data-sidebar-size", "") :
            document.documentElement.setAttribute("data-sidebar-size", "sm");
        } else if (windowSize > 1025) {
          document.body.classList.remove("vertical-sidebar-enable");
          document.documentElement.getAttribute("data-sidebar-size") == "lg" ?
            document.documentElement.setAttribute("data-sidebar-size", "sm") :
            document.documentElement.setAttribute("data-sidebar-size", "lg");
        } else if (windowSize <= 767) {
          document.body.classList.add("vertical-sidebar-enable");
          document.documentElement.setAttribute("data-sidebar-size", "lg");
        }
      }

      //Two column menu
      if (document.documentElement.getAttribute("data-layout") == "twocolumn") {
        document.body.classList.contains("twocolumn-panel") ?
          document.body.classList.remove("twocolumn-panel") :
          document.body.classList.add("twocolumn-panel");
      }
    },
    toggleMenu() {
      this.$parent.toggleMenu();
    },
    toggleRightSidebar() {
      this.$parent.toggleRightSidebar();
    },
    initFullScreen() {
      document.body.classList.toggle("fullscreen-enable");
      if (
        !document.fullscreenElement &&
        /* alternative standard method */
        !document.mozFullScreenElement &&
        !document.webkitFullscreenElement
      ) {
        // current working methods
        if (document.documentElement.requestFullscreen) {
          document.documentElement.requestFullscreen();
        } else if (document.documentElement.mozRequestFullScreen) {
          document.documentElement.mozRequestFullScreen();
        } else if (document.documentElement.webkitRequestFullscreen) {
          document.documentElement.webkitRequestFullscreen(
            Element.ALLOW_KEYBOARD_INPUT
          );
        }
      } else {
        if (document.cancelFullScreen) {
          document.cancelFullScreen();
        } else if (document.mozCancelFullScreen) {
          document.mozCancelFullScreen();
        } else if (document.webkitCancelFullScreen) {
          document.webkitCancelFullScreen();
        }
      }
    },
    setLanguage(locale, country, flag) {
      this.lan = locale;
      this.text = country;
      this.flag = flag;
      document.getElementById("header-lang-img").setAttribute("src", flag);
      i18n.global.locale = locale;
    },
    toggleDarkMode() {
      if (document.documentElement.getAttribute("data-layout-mode") == "dark") {
        document.documentElement.setAttribute("data-layout-mode", "light");
      } else {
        document.documentElement.setAttribute("data-layout-mode", "dark");
      }
    },
    initTopbarComponents() {
      function updateCartPrice() {
        var currencySign = "$";
        var subtotal = 0;
        Array.from(document.getElementsByClassName("cart-item-price")).forEach(function (e) {
          subtotal += parseFloat(e.innerHTML);
        });
        if (document.getElementById("cart-item-total")) {
          document.getElementById("cart-item-total").innerHTML = currencySign + subtotal.toFixed(2);
        }
      }
      if (document.getElementsByClassName("dropdown-item-cart")) {
        var dropdownItemCart = document.querySelectorAll(".dropdown-item-cart").length;
        Array.from(document.querySelectorAll("#page-topbar .dropdown-menu-cart .remove-item-btn")).forEach(function (item) {
          item.addEventListener("click", function () {
            dropdownItemCart--;
            this.closest(".dropdown-item-cart").remove();
            Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
              e.innerHTML = dropdownItemCart;
            });
            updateCartPrice();
            if (document.getElementById("empty-cart")) {
              document.getElementById("empty-cart").style.display = dropdownItemCart == 0 ? "block" : "none";
            }
            if (document.getElementById("checkout-elem")) {
              document.getElementById("checkout-elem").style.display = dropdownItemCart == 0 ? "none" : "block";
            }
          });
        });
        Array.from(document.getElementsByClassName("cartitem-badge")).forEach(function (e) {
          e.innerHTML = dropdownItemCart;
        });
        if (document.getElementById("empty-cart")) {
          document.getElementById("empty-cart").style.display = "none";
        }
        if (document.getElementById("checkout-elem")) {
          document.getElementById("checkout-elem").style.display = "block";
        }
        updateCartPrice();
      }

      // notification messages
      if (document.getElementsByClassName("notification-check")) {
        Array.from(document.querySelectorAll(".notification-check input")).forEach(function (element) {
          element.addEventListener("click", function (el) {
            el.target.closest(".notification-item").classList.toggle("active");
          });
        });
      }
    }
  },
  computed: {},
  mounted() {
    document.addEventListener("scroll", function () {
      var pageTopbar = document.getElementById("page-topbar");
      if (pageTopbar) {
        document.body.scrollTop >= 50 || document.documentElement.scrollTop >= 50 ? pageTopbar.classList.add(
          "topbar-shadow") : pageTopbar.classList.remove("topbar-shadow");
      }
    });
    if (document.getElementById("topnav-hamburger-icon"))
      document
        .getElementById("topnav-hamburger-icon")
        .addEventListener("click", this.toggleHamburgerMenu);

    this.isCustomDropdown();
    this.initTopbarComponents();
  },
};
</script>

<template>
  <header id="page-topbar">
    <div class="layout-width">
      <div class="navbar-header">
        <div class="d-flex">
          <!-- LOGO -->
          <div class="navbar-brand-box horizontal-logo">
            <router-link to="/" class="logo logo-dark">
              <span class="logo-sm">
                <img src="@/assets/images/logo-sm.png" alt="" height="22" />
              </span>
              <span class="logo-lg">
                <img src="@/assets/images/logo-dark.png" alt="" height="17" />
              </span>
            </router-link>

            <router-link to="/" class="logo logo-light">
              <span class="logo-sm">
                <img src="@/assets/images/logo-sm.png" alt="" height="22" />
              </span>
              <span class="logo-lg">
                <img src="@/assets/images/logo-light.png" alt="" height="17" />
              </span>
            </router-link>
          </div>

          <button type="button" class="
              btn btn-sm
              px-3
              fs-16
              header-item
              vertical-menu-btn
              topnav-hamburger
            " id="topnav-hamburger-icon">
            <i class="ri-menu-fill" style="font-size:25px;color:#a5b0b7"></i>
          </button>
          <div class="d-flex align-items-center" style="font-size:20px">App Builder</div>
            
        </div>

      </div>
    </div>
  </header>
</template>