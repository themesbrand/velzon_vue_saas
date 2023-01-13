<script>
import {
  SearchIcon,
  InfoIcon,
  MoreVerticalIcon
} from '@zhuowenli/vue-feather-icons';

import {
  required,
  helpers
} from "@vuelidate/validators";
import useVuelidate from "@vuelidate/core";

import Layout from "../../layouts/main.vue";
import appConfig from "../../../app.config";

import {
  chatData,
  chatMessagesData
} from "./data";

export default {
  setup() {
    return {
      v$: useVuelidate()
    };
  },
  page: {
    title: "Chat",
    meta: [{
      name: "description",
      content: appConfig.description
    }],
  },
  data() {
    return {
      chatData: chatData,
      chatMessagesData: chatMessagesData,
      title: "Chat",
      items: [{
        text: "Velzon",
        href: "/",
      },
      {
        text: "Chat",
        active: true,
      },
      ],
      submitted: false,
      form: {
        message: "",
      },
      username: "Steven Franklin",
      profile: require("@/assets/images/users/avatar-2.jpg")
    };
  },
  components: {
    Layout,
    SearchIcon,
    InfoIcon,
    MoreVerticalIcon
  },
  validations: {
    form: {
      message: {
        required: helpers.withMessage("Message is required", required),
      },
    },
  },
  methods: {
    /**
     * Get the name of user
     */
    scrollToBottom(id) {
      setTimeout(function () {
        var simpleBar = document.getElementById(id).querySelector(
          "#chat-conversation .simplebar-content-wrapper") ?
          document.getElementById(id).querySelector(
            "#chat-conversation .simplebar-content-wrapper") : '';

        var offsetHeight = document.getElementsByClassName("chat-conversation-list")[0] ?
          document.getElementById(id).getElementsByClassName("chat-conversation-list")[0]
            .scrollHeight - window.innerHeight + 600 : 0;

        if (offsetHeight)
          simpleBar.scrollTo({
            top: offsetHeight,
            behavior: "smooth"
          });
      }, 300);
    },
    chatUsername(name, image) {
      this.username = name;
      this.profile = image;
      this.usermessage = "Hello";
      this.chatMessagesData = [];
      const currentDate = new Date();
      const hours = (currentDate.getHours() < 10 ? "0" : "") + currentDate.getHours();
      const minutes = (currentDate.getMinutes() < 10 ? "0" : "") + currentDate.getMinutes();

      this.chatMessagesData.push({
        name: this.username,
        message: this.usermessage,
        time: hours + ":" + minutes,
      });
    },

    /**
     * Char form Submit
     */
    formSubmit() {
      this.submitted = true;

      // stop here if form is invalid
      this.v$.$touch();

      if (this.v$.$invalid) {
        return;
      } else {
        const message = this.form.message;
        const currentDate = new Date();
        const hours = (currentDate.getHours() < 10 ? "0" : "") + currentDate.getHours();
        const minutes = (currentDate.getMinutes() < 10 ? "0" : "") + currentDate.getMinutes();

        this.chatMessagesData.push({
          align: "right",
          name: "Henry Wells",
          message,
          time: hours + ":" + minutes,
        });
        var currentChatId = "users-chat";
        this.scrollToBottom(currentChatId);
      }
      this.submitted = false;
      this.form = {};
    },
  },
  mounted() {
    var currentChatId = "users-chat";
    this.scrollToBottom(currentChatId);
    document.getElementById('copyClipBoard').style.display = 'none';
    var userChatElement = document.querySelectorAll(".user-chat");
    document.querySelectorAll(".chat-user-list li a").forEach(function (item) {
      item.addEventListener("click", function () {
        userChatElement.forEach(function (elm) {
          elm.classList.add("user-chat-show");
        });

        // chat user list link active
        var chatUserList = document.querySelector(".chat-user-list li.active");
        if (chatUserList) chatUserList.classList.remove("active");
        this.parentNode.classList.add("active");
      });
    });

    // user-chat-remove
    document.querySelectorAll(".user-chat-remove").forEach(function (item) {
      item.addEventListener("click", function () {
        userChatElement.forEach(function (elm) {
          elm.classList.remove("user-chat-show");
        });
      });
    });
  },
};
</script>

<template>
  <Layout>

    <div class="chat-wrapper d-lg-flex gap-1 mx-n4 mt-n4 p-1">
      <div class="chat-leftsidebar">
        <div class="px-4 pt-4 mb-4">
          <div class="d-flex align-items-start">
            <div class="flex-grow-1">
              <h5 class="mb-4">Chats</h5>
            </div>
            <div class="flex-shrink-0">
              <div v-b-tooltip.hover title="Add Contact">
                <b-button type="button" variant="soft-success" size="sm">
                  <i class="ri-add-line align-bottom"></i>
                </b-button>
              </div>
            </div>
          </div>
          <div class="search-box">
            <input type="text" class="form-control bg-light border-light" placeholder="Search here..." />
            <i class="ri-search-2-line search-icon"></i>
          </div>
        </div>

        <div class="chat-room-list" data-simplebar>
          <div class="d-flex align-items-center px-4 mb-2">
            <div class="flex-grow-1">
              <h4 class="mb-0 fs-11 text-muted text-uppercase">
                Direct Messages
              </h4>
            </div>
            <div class="flex-shrink-0">
              <div v-b-tooltip.hover title="New Message">
                <b-button type="button" variant="soft-success" size="sm">
                  <i class="ri-add-line align-bottom"></i>
                </b-button>
              </div>
            </div>
          </div>

          <div class="chat-message-list">
            <SimpleBar class="list-unstyled chat-list chat-user-list">
              <li class v-for="data of chatData" :key="data.id" @click="chatUsername(data.name, data.image)"
                :class="{ active: username == data.name }">
                <b-link href="javascript: void(0);">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs" v-if="data.image">
                        <img :src="`${data.image}`" class="rounded-circle img-fluid userprofile" alt />
                      </div>
                      <div class="avatar-xxs" v-if="!data.image">
                        <div class="avatar-title rounded-circle bg-danger userprofile">
                          {{ data.name.charAt(0) }}
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-1">
                        {{ data.name }}
                      </p>
                    </div>

                    <div class="flex-shrink-0">
                      <b-badge variant="soft-dark" class="badge-soft-dark rounded p-1">{{ data.time }}</b-badge>
                    </div>
                  </div>
                </b-link>
              </li>
            </SimpleBar>
          </div>

          <div class="d-flex align-items-center px-4 mt-4 pt-2 mb-2">
            <div class="flex-grow-1">
              <h4 class="mb-0 fs-11 text-muted text-uppercase">Channels</h4>
            </div>
            <div class="flex-shrink-0">
              <div v-b-tooltip.hover title="Create group">
                <b-button type="button" variant="soft-success" size="sm">
                  <i class="ri-add-line align-bottom"></i>
                </b-button>
              </div>
            </div>
          </div>

          <div class="chat-message-list">
            <ul class="list-unstyled chat-list chat-user-list mb-0" id="channelList">
              <li>
                <b-link href="javascript: void(0);" class="unread-msg-user">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs">
                        <div class="avatar-title bg-light rounded-circle text-body">
                          #
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-0">Landing Design</p>
                    </div>
                    <div class="flex-shrink-0">
                      <b-badge variant="soft-dark" class="badge-soft-dark rounded p-1">7</b-badge>
                    </div>
                  </div>
                </b-link>
              </li>
              <li>
                <b-link href="javascript: void(0);">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs">
                        <div class="avatar-title bg-light rounded-circle text-body">
                          #
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-0">General</p>
                    </div>
                  </div>
                </b-link>
              </li>
              <li>
                <b-link href="javascript: void(0);" class="unread-msg-user">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs">
                        <div class="avatar-title bg-light rounded-circle text-body">
                          #
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-0">Project Tasks</p>
                    </div>
                    <div class="flex-shrink-0">
                      <b-badge variant="soft-dark" class="badge-soft-dark rounded p-1">3</b-badge>
                    </div>
                  </div>
                </b-link>
              </li>

              <li>
                <b-link href="javascript: void(0);">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs">
                        <div class="avatar-title bg-light rounded-circle text-dark">
                          #
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-0">Meeting</p>
                    </div>
                  </div>
                </b-link>
              </li>
              <li>
                <b-link href="javascript: void(0);">
                  <div class="d-flex align-items-center">
                    <div class="flex-shrink-0 chat-user-img online align-self-center me-2 ms-0">
                      <div class="avatar-xxs">
                        <div class="avatar-title bg-light rounded-circle text-dark">
                          #
                        </div>
                      </div>
                    </div>
                    <div class="flex-grow-1 overflow-hidden">
                      <p class="text-truncate mb-0">Reporting</p>
                    </div>
                  </div>
                </b-link>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="user-chat w-100 overflow-hidden">
        <div class="chat-content d-lg-flex">
          <div class="w-100 overflow-hidden position-relative">
            <div class="position-relative">
              <div class="p-3 user-chat-topbar">
                <b-row class="align-items-center">
                  <b-col sm="4" cols="8">
                    <div class="d-flex align-items-center">
                      <div class="flex-shrink-0 d-block d-lg-none me-3">
                        <b-link href="javascript: void(0);" class="user-chat-remove fs-18 p-1"><i
                            class="ri-arrow-left-s-line align-bottom"></i></b-link>
                      </div>
                      <div class="flex-grow-1 overflow-hidden">
                        <div class="d-flex align-items-center">
                          <div class="flex-shrink-0 chat-user-img online user-own-img align-self-center me-3 ms-0">
                            <img :src="profile ? profile : require('@/assets/images/users/user-dummy-img.jpg')"
                              class="rounded-circle avatar-xs" alt="" />
                            <span class="user-status"></span>
                          </div>
                          <div class="flex-grow-1 overflow-hidden">
                            <h5 class="text-truncate mb-0 fs-16">
                              <b-link class="text-reset username" data-bs-toggle="offcanvas"
                                href="#userProfileCanvasExample" aria-controls="userProfileCanvasExample">{{ username }}
                              </b-link>
                            </h5>
                            <p class="text-truncate text-muted fs-14 mb-0 userStatus">
                              <small>Online</small>
                            </p>
                          </div>
                        </div>
                      </div>
                    </div>
                  </b-col>
                  <b-col sm="8" cols="4">
                    <ul class="list-inline user-chat-nav text-end mb-0">
                      <li class="list-inline-item m-0">
                        <div class="dropdown">
                          <button class="btn btn-ghost-secondary btn-icon" type="button" data-bs-toggle="dropdown"
                            aria-haspopup="true" aria-expanded="false">
                            <search-icon class="icon-sm"></search-icon>
                          </button>
                          <div class="dropdown-menu p-0 dropdown-menu-end dropdown-menu-lg">
                            <div class="p-2">
                              <div class="search-box">
                                <input type="text" class="form-control bg-light border-light"
                                  placeholder="Search here..." onkeyup="searchMessages()" id="searchMessage" />
                                <i class="ri-search-2-line search-icon"></i>
                              </div>
                            </div>
                          </div>
                        </div>
                      </li>

                      <li class="list-inline-item d-none d-lg-inline-block m-0">
                        <b-button type="button" variant="ghost-secondary" class="btn-icon" data-bs-toggle="offcanvas"
                          data-bs-target="#userProfileCanvasExample" aria-controls="userProfileCanvasExample">
                          <info-icon class="icon-sm"></info-icon>
                        </b-button>
                      </li>

                      <li class="list-inline-item m-0">
                        <div class="dropdown">
                          <button class="btn btn-ghost-secondary btn-icon" type="button" data-bs-toggle="dropdown"
                            aria-haspopup="true" aria-expanded="false">
                            <more-vertical-icon class="icon-sm"></more-vertical-icon>
                          </button>
                          <div class="dropdown-menu dropdown-menu-end">
                            <b-link class="dropdown-item d-block d-lg-none user-profile-show" href="#"><i
                                class="ri-user-2-fill align-bottom text-muted me-2"></i>
                              View Profile</b-link>
                            <b-link class="dropdown-item" href="#"><i
                                class="ri-inbox-archive-line align-bottom text-muted me-2"></i>
                              Archive</b-link>
                            <b-link class="dropdown-item" href="#"><i
                                class="ri-mic-off-line align-bottom text-muted me-2"></i>
                              Muted</b-link>
                            <b-link class="dropdown-item" href="#"><i
                                class="ri-delete-bin-5-line align-bottom text-muted me-2"></i>
                              Delete</b-link>
                          </div>
                        </div>
                      </li>
                    </ul>
                  </b-col>
                </b-row>
              </div>

              <div class="position-relative" id="users-chat">
                <div class="chat-conversation p-3 p-lg-4" id="chat-conversation" data-simplebar ref="current">
                  <ul class="list-unstyled chat-conversation-list">
                    <li v-for="data of chatMessagesData" :key="data.message" :class="{
  right: `${data.align}` === 'right',
  left: `${data.align}` !== 'right',
}" class="chat-list">
                      <div class="conversation-list">
                        <div class="chat-avatar" v-if="data.align !== 'right'">
                          <img :src="profile ? profile : require('@/assets/images/users/user-dummy-img.jpg')" alt="" />
                        </div>
                        <div class="user-chat-content">
                          <div class="ctext-wrap">
                            <div class="ctext-wrap-content">
                              <p class="mb-0 ctext-content">
                                {{ data.message }}
                              </p>
                            </div>
                            <div class="dropdown align-self-start message-box-drop">
                              <b-link class="dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown"
                                aria-haspopup="true" aria-expanded="false">
                                <i class="ri-more-2-fill"></i>
                              </b-link>
                              <div class="dropdown-menu">
                                <b-link class="dropdown-item reply-message" href="#"><i
                                    class="ri-reply-line me-2 text-muted align-bottom"></i>Reply</b-link>
                                <b-link class="dropdown-item" href="#"><i
                                    class="ri-share-line me-2 text-muted align-bottom"></i>Forward</b-link>
                                <b-link class="dropdown-item copy-message" href="#"><i
                                    class="ri-file-copy-line me-2 text-muted align-bottom"></i>Copy</b-link>
                                <b-link class="dropdown-item" href="#"><i
                                    class="ri-bookmark-line me-2 text-muted align-bottom"></i>Bookmark</b-link>
                                <b-link class="dropdown-item delete-item" href="#"><i
                                    class="ri-delete-bin-5-line me-2 text-muted align-bottom"></i>Delete</b-link>
                              </div>
                            </div>
                            <div class="conversation-name">
                              <small class="text-muted time">{{
    data.time
}}</small>
                              <span class="text-success check-message-icon"><i
                                  class="ri-check-double-line align-bottom"></i></span>
                            </div>
                          </div>
                        </div>
                      </div>
                    </li>
                  </ul>

                </div>
                <div class="alert alert-warning alert-dismissible copyclipboard-alert px-4 fade show" id="copyClipBoard"
                  role="alert">
                  Message copied
                </div>
              </div>


              <div class="chat-input-section p-3 p-lg-4">
                <form @submit.prevent="formSubmit">
                  <b-row class="g-0 align-items-center">
                    <b-col cols="auto">
                      <div class="chat-input-links me-2">
                        <div class="links-list-item">
                          <b-button type="button" variant="link" class="text-decoration-none emoji-btn" id="emoji-btn">
                            <i class="bx bx-smile align-middle"></i>
                          </b-button>
                        </div>
                      </div>
                    </b-col>
                    <b-col>
                      <div class="chat-input-feedback">
                        Please Enter a Message
                      </div>

                      <input type="text" v-model="form.message" class="form-control chat-input bg-light border-light"
                        placeholder="Enter Message..." :class="{
  'is-invalid': submitted && v$.form.message.$error,
}" />
                      <div v-if="submitted && v$.form.message.$error" class="invalid-feedback">
                        <span v-if="v$.form.message.required.$message">{{
    v$.form.message.required.$message
                          }}</span>
                      </div>
                    </b-col>
                    <b-col cols="auto">
                      <div class="chat-input-links ms-2">
                        <div class="links-list-item">
                          <b-button variant="success" type="submit" class="chat-send">
                            <i class="ri-send-plane-2-fill align-bottom"></i>
                          </b-button>
                        </div>
                      </div>
                    </b-col>
                  </b-row>
                </form>
              </div>

              <div class="replyCard">
                <b-card no-body class="mb-0">
                  <b-card-body class="py-3">
                    <div class="replymessage-block mb-0 d-flex align-items-start">
                      <div class="flex-grow-1">
                        <h5 class="conversation-name"></h5>
                        <p class="mb-0"></p>
                      </div>
                      <div class="flex-shrink-0">
                        <b-button type="button" variant="link" size="sm" id="close_toggle" class="mt-n2 me-n3 fs-18">
                          <i class="bx bx-x align-middle"></i>
                        </b-button>
                      </div>
                    </div>
                  </b-card-body>
                </b-card>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </Layout>
</template>