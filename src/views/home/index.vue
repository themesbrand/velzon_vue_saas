<script>
import Layout from "../../layouts/main.vue";
// import PageHeader from "@/components/page-header";

export default {
  data() {
    return {
      title: "Home",
      items: [[
        [{ id: 1, title: "Tasks Manager", link: "tasksmanager" },
        { id: 2, title: "Contack List", link: "contactlist" },
        { id: 3, title: "Customer Potal", link: "customerporal" }],
        [{ id: 4, title: "Test3", link: "test3" },
        { id: 5, title: "New App", link: "newapp" },
        { id: 6, title: "Test3", link: "test3" }],], [
        [{ id: 7, title: "Asset Manager 01", link: "assetmanager01" },
        { id: 8, title: "HR Manager", link: "hrmanager" },
        { id: 9, title: "Christine App", link: "christine App" }],
        [{ id: 10, title: "Testing", link: "testing" },
        { id: 11, title: "IT Services", link: "itservices" },
        { id: 12, title: "Non Surgical Spinal Care", link: "nonsurgicalspinalcare" }],]
      ]
    };
  },
  components: {
    Layout,
    // PageHeader,
  },
  mounted() {

  },
  methods: {
    changeRoute( routeObj ){
      this.$router.push(routeObj)
    }
  }
};
</script>

<template>
  <Layout>
    <!-- <PageHeader :title="title" :items="items" /> -->

    <b-row>
      <b-col cols="12">
        <div class="page-apps">
          <div class="box">
            <b-row>
              <b-col md="12">
                <div class="box-header">
                  <div class="item"><span>Apps</span></div>
                  <div class="item">
                    <b-button variant="info" class="waves-effect waves-light">Add App</b-button>
                  </div>
                </div>
              </b-col>
            </b-row>
            <b-row class="mt-1">
              <b-col md="12">
                <div class="box-container">
                  <div class="box-content">
                    <b-row v-for="(item, index) in items" :key="index">
                      <b-col xl="6" v-for="(it, idx) in item" :key="idx">
                        <b-row>
                          <b-col v-for="(ii, id) in it" :key="id" lg="4" class="mt-3">
                            <div class="box-item" v-on:click="changeRoute({ name: 'tasksmanager' })">
                              <span>{{ ii.title }}</span>
                            </div>
                          </b-col>
                        </b-row>
                      </b-col>
                    </b-row>
                  </div>
                </div>
              </b-col>
            </b-row>
          </div>
        </div>
      </b-col>
    </b-row>
  </Layout>
</template>

<style>
.page-apps {
  padding: 30px;

}

.box-header>.item:first-of-type {
  float: left;
  font-size: 20px;
}

.box-header>.item:nth-of-type(2) {
  float: right;
}

.box-container {
  background-color: #ebeef1;
  padding: 20px;
}

.box-content {
  background-color: white;
  border-radius: 10px;
  padding: 25px;
  padding-top: 9px;
}

.page-apps .box-content .box-item {
  width: 100%;
  height: 70px;
  background-color: #cbddf7;
  border-radius: 7px;
  border-left: #ffe699 solid 8px;
  padding: 5px 15px;
  font-size: 18px;
  text-align: center;
  line-height: 23px;
  vertical-align: middle;
  display: table;
  min-width: 130px;
  overflow-y: hidden;
  cursor: pointer;
}

@media (max-width: 1450px) {
  .box-item>span {
    font-size: 14px;
  }
}

.box-content .box-item>span {
  vertical-align: middle;
  display: table-cell;
}
</style>