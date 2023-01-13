<script>
import { layoutComputed } from "@/state/helpers";
import { SimpleBar } from "simplebar-vue3";

export default {
  components: {
    SimpleBar,
  },
  data() {
    return {
      settings: {
        minScrollbarLength: 60,
      },
      menuItems: [
        { id : 0, title: "Home", link: "home" },
        { id : 1, title: "Tasks Manager", link: "tasksmanager" },
        { id : 2,  title: "Contack List", link: "contactlist" },
        { id : 3,  title: "Customer Potal", link: "customerporal" },
        { id : 4,  title: "Test3", link: "test3" },
        { id : 5,  title: "New App", link: "newapp" },
        { id : 5,  title: "Test3", link: "test3" },
        { id : 6,  title: "Asset Manager 01", link: "assetmanager01" },
        { id : 7,  title: "HR Manager", link: "hrmanager" },
        { id : 8,  title: "Christine App", link: "christine App" },
        { id : 9,  title: "Testing", link: "testing" },
        { id : 10,  title: "IT Services", link: "itservices" },
        { id : 11,  title: "Non Surgical Spinal Care", link: "nonsurgicalspinalcare" },
      ],
    };
  },
  computed: {
    ...layoutComputed,
    layoutType: {
      get() {
        return this.$store ? this.$store.state.layout.layoutType : {} || {};
      },
    },
  },

  watch: {
    $route: {
      handler: "onRoutechange",
      immediate: true,
      deep: true,
    },
  },

  mounted() {
    if (document.querySelectorAll(".navbar-nav .collapse")) {
      let collapses = document.querySelectorAll(".navbar-nav .collapse");

      collapses.forEach((collapse) => {
        // Hide sibling collapses on `show.bs.collapse`
        collapse.addEventListener("show.bs.collapse", (e) => {
          e.stopPropagation();
          let closestCollapse = collapse.parentElement.closest(".collapse");
          if (closestCollapse) {
            let siblingCollapses = closestCollapse.querySelectorAll(".collapse");
            siblingCollapses.forEach((siblingCollapse) => {
              if (siblingCollapse.classList.contains("show")) {
                siblingCollapse.classList.remove("show");
              }
            });
          } else {
            let getSiblings = (elem) => {
              // Setup siblings array and get the first sibling
              let siblings = [];
              let sibling = elem.parentNode.firstChild;
              // Loop through each sibling and push to the array
              while (sibling) {
                if (sibling.nodeType === 1 && sibling !== elem) {
                  siblings.push(sibling);
                }
                sibling = sibling.nextSibling;
              }
              return siblings;
            };
            let siblings = getSiblings(collapse.parentElement);
            siblings.forEach((item) => {
              if (item.childNodes.length > 2)
                item.firstElementChild.setAttribute("aria-expanded", "false");
              let ids = item.querySelectorAll("*[id]");
              ids.forEach((item1) => {
                item1.classList.remove("show");
                if (item1.childNodes.length > 2) {
                  let val = item1.querySelectorAll("ul li a");

                  val.forEach((subitem) => {
                    if (subitem.hasAttribute("aria-expanded"))
                      subitem.setAttribute("aria-expanded", "false");
                  });
                }
              });
            });
          }
        });

        // Hide nested collapses on `hide.bs.collapse`
        collapse.addEventListener("hide.bs.collapse", (e) => {
          e.stopPropagation();
          let childCollapses = collapse.querySelectorAll(".collapse");
          childCollapses.forEach((childCollapse) => {
            let childCollapseInstance = childCollapse;
            childCollapseInstance.style.display = "none";
          });
        });
      });
    }
  },

  methods: {
    onRoutechange(ele) {
      this.initActiveMenu(ele.path);
      if (document.getElementsByClassName("mm-active").length > 0) {
        const currentPosition = document.getElementsByClassName("mm-active")[0].offsetTop;
        if (currentPosition > 500)
          if (this.$refs.isSimplebar)
            this.$refs.isSimplebar.value.getScrollElement().scrollTop =
              currentPosition + 300;
      }
    },

    initActiveMenu(ele) {
      setTimeout(() => {
        if (document.querySelector("#navbar-nav")) {
          let a = document
            .querySelector("#navbar-nav")
            .querySelector('[href="' + ele + '"]');
          if (a) {
            a.classList.add("active");
            let parentCollapseDiv = a.closest(".collapse.menu-dropdown");
            if (parentCollapseDiv) {
              parentCollapseDiv.classList.add("show");
              parentCollapseDiv.parentElement.children[0].classList.add("active");
              parentCollapseDiv.parentElement.children[0].setAttribute(
                "aria-expanded",
                "true"
              );
              if (parentCollapseDiv.parentElement.closest(".collapse.menu-dropdown")) {
                parentCollapseDiv.parentElement
                  .closest(".collapse")
                  .classList.add("show");
                if (
                  parentCollapseDiv.parentElement.closest(".collapse")
                    .previousElementSibling
                )
                  parentCollapseDiv.parentElement
                    .closest(".collapse")
                    .previousElementSibling.classList.add("active");
                const grandparent = parentCollapseDiv.parentElement
                  .closest(".collapse")
                  .previousElementSibling.parentElement.closest(".collapse");
                if (grandparent && grandparent && grandparent.previousElementSibling) {
                  grandparent.previousElementSibling.classList.add("active");
                  grandparent.classList.add("show");
                }
              }
            }
          }
        }
      }, 0);
    },
  },
};
</script>

<template>
  <b-container fluid>
    <div id="two-column-menu"></div>

    <template v-if="layoutType === 'twocolumn'">
      <SimpleBar class="navbar-nav" id="navbar-nav">
        <li class="menu-title">
          <span data-key="t-menu"> Home </span>
        </li>
        <li class="menu-title">
          <span data-key="t-menu"> {{ $t("t-menu") }}</span>
        </li>
        <li class="nav-item">
          <b-link class="nav-link menu-link" href="#sidebarDashboards" data-bs-toggle="collapse" role="button"
            aria-expanded="false" aria-controls="sidebarDashboards">
            <i class="bx bxs-dashboard"></i>
            <span data-key="t-dashboards"> {{ $t("t-dashboards") }}</span>
          </b-link>
        </li>
      </SimpleBar>
    </template>

    <template v-else>
      <ul class="navbar-nav h-100" id="navbar-nav">
        <li class="menu-title">
          <span data-key="t-menu"> Home </span>
        </li>
        <li class="menu-title">
          <span data-key="t-menu"> Apps </span>
        </li>
        <li class="nav-item">
          <router-link class="nav-link menu-link" :to="item.link" role="button"
            aria-expanded="false" v-for="item in menuItems" :key="item.id">
            <span>{{ item.title }}</span>
          </router-link>
        </li>
      </ul>
    </template>
  </b-container>
</template>
