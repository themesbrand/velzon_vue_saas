<script>
import Layout from "../../layouts/main.vue";
// import PageHeader from "@/components/page-header";

export default {
  data() {
    return {
      title: "Home",
      items: [
        {
          title: "sdfsdf",
          infos: [
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            }
          ]
        },
        {
          title: "sdfsdf",
          infos: [
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            }
          ]
        },
        {
          title: "sdfsdf",
          infos: [
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
          ]
        },
        {
          title: "sdfsdf",
          infos: [
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            }
          ]
        },
        {
          title: "sdfsdf",
          infos: [
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            },
            {
              title: "13123",
              list: ["sdsdf", "sdfsdf", "sdfsdf"]
            }
          ]
        }
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
                  <div class="d-flex justify-content-between">
                    <div style="font-size:20px"><span>Task Manager <i class="ri-settings-3-line"></i></span></div>
                    <div style="font-size:15px"><span><i class="ri-file-copy-line"></i>Access App </span></div>
                    <div style="font-size:15px"><span><i class="ri-file-copy-line"></i> All Apps</span></div>
                  </div>
                </div>
              </b-col>
            </b-row>
            <b-row>
              <b-col md="12">
                <div class="box-container">
                  <div class="box-content">
                    <div class="container">
                      <div class="row">
                        <div class="col mt-3" v-for="(item, index) in items" :key="index">
                          <div class="box-item mb-2">
                            <span>{{ item.title }}</span>
                          </div>
                          <ul v-for="(item2, index2) in item.infos" :key="index2">
                            <span>{{ item2.title }}</span>
                            <li v-for="(item3, index3) in item2.list" :key="index3">
                              {{ item3 }}
                            </li>
                          </ul>
                        </div>
                      </div>
                    </div>
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
.box-header>div>div>span>* {
  vertical-align: middle;
}

.page-apps {
  padding: 30px;

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

.box-content .box-item {
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
}

@media (max-width: 1430px) {
  .box-item>span {
    font-size: 14px;
  }
}

.box-content .box-item>span {
  vertical-align: middle;
  display: table-cell;
}
</style>