<template>
  <v-app
    id="inspire"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <SideBar />
    <Navbar />
    <v-container>
      <v-row>
        <v-col cols="12" sm="9">
          <v-row>
            <v-col cols="12" sm="12">
              <Contact />
            </v-col>
            <v-col cols="12" sm="12">
              <Agenda />
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="10"></v-col>
        <Doctor />
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import SideBar from "../components/SideBar.vue";
import Navbar from "../components/Navbar.vue";
import Doctor from "../components/Doctor.vue";
import Contact from "../components/Contact.vue";
import Agenda from "../components/Agenda.vue";
export default {
  name: "Home",

  components: {
    SideBar,
    Navbar,
    Doctor,
    Contact,
    Agenda,
  },
};
</script>
