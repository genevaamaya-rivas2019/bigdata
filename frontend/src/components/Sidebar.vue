<template>
  <div>
    <div>
    <v-navigation-drawer fixed permanent class="mt-cos">
      <v-card>
        <center>
          <div class="pt-5">
            <img src="@/assets/pnlogo.png" id="profile">
          </div>
          <v-list>
            <v-list-item two-line>
              <v-list-item-content>
                <v-list-item-title class="title">Educator</v-list-item-title>
                <v-list-item-subtitle>Gateway for life</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </center>
        <v-divider></v-divider>

        <v-list nav dense>
          <v-list-item link class="ml-6" @click="gotoRoute('/educator')">
            <v-list-item-icon>
              <v-icon>mdi-view-dashboard</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>
          <v-list-item link class="ml-6" @click="gotoRoute('/unread-request')">
            <v-list-item-icon>
              <v-icon>mdi-eye</v-icon>
            </v-list-item-icon>
            <v-list-item-title>View Request</v-list-item-title>
          </v-list-item>
          <v-list-item link class="ml-6" @click="gotoRoute('/pending-request')">
            <v-list-item-icon>
              <v-icon>mdi-account-edit</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Pending</v-list-item-title>
          </v-list-item>
          <v-list-item link class="ml-6" @click="gotoRoute('/editpassword')">
            <v-list-item-icon>
              <v-icon>mdi-account-edit</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Edit Password</v-list-item-title>
          </v-list-item>
          <v-expansion-panels  class="ma-0 pa-0">
            <v-expansion-panel>
              <v-expansion-panel-header>
                <v-list-item>
                  <v-list-item-icon>
                    <v-icon>mdi-folder</v-icon>
                  </v-list-item-icon>
                  <v-list-item-title>Reports</v-list-item-title>
                </v-list-item>
              </v-expansion-panel-header>
              <v-expansion-panel-content>
                <v-list>
                  <v-list-item link class="ml-6 text-center" @click="gotoRoute('/approved-request')">
                    <v-list-item-icon>
                      <v-icon>mdi-chart-areaspline</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Approved<br> Request</v-list-item-title>
                  </v-list-item>
                  <v-list-item link class="ml-6 text-center" @click="gotoRoute('/rejected-request')">
                    <v-list-item-icon>
                      <v-icon>mdi-chart-areaspline</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>Rejected<br> Request</v-list-item-title>
                  </v-list-item>
                  <v-list-item link class="ml-6 text-center" @click="gotoRoute('/stamp')">
                    <v-list-item-icon>
                      <v-icon>mdi-chart-pie</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>
                      TimeSpan
                      <br>Per Request
                    </v-list-item-title>
                  </v-list-item>
                  <v-list-item link class="ml-6 text-center" @click="gotoRoute('/mostlyrequested')">
                    <v-list-item-icon>
                      <v-icon>mdi-chart-pie</v-icon>
                    </v-list-item-icon>
                    <v-list-item-title>
                      Most Frequent
                      <br>Request/month
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-expansion-panel-content>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-list>
        <!-- </v-navigation-drawer> -->
      </v-card>
    </v-navigation-drawer>
  </div>
  </div>
</template>
<script>
// import io from "socket.io-client";
// var socket = io.connect("http://localhost:3232");
// import axios from 'axios'
/* eslint-disable */
export default {
  name: "sidebar",
  data() {
    return {
      yes: true,
      vrnum: 0,
    };
  },
  created() {
    // let myroute = this.$route.name
    // if(myroute === "student"){
    //   this.isStudent = true
    //   this.dontshow = true
    // }
    // this.onNewRequest();
    // axios.get("http://localhost:3232/unread").then(resp=>{
    //   this.vrnum = resp.data.count
    // })
  },
  methods: {
    gotoRoute(next) {
      this.$router.push({ path: next });
    },
    // passdata(data) {
    //   this.vrnum = data;
    // },
    // onNewRequest() {
    //   socket.on("newrequest", data => {
    //     this.passdata(data);
    //   });
    // }
  }
};
</script>
<style scoped>
#profile {
  height: 70px;
  width: 70px;
  border-radius: 50%;
}
.mt-cos {
  margin-top: 80px;
}
.vr-nt {
  color: red;
  border-radius: 50%;
  font-weight: bold;
}
</style>