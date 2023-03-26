<template>
  <v-app-bar colar="white" app dark flat>
    <v-icon color="black">fas fa-long-arrow-alt-left</v-icon>
    <h4 class="darkcyan--text ml-3">Patient Card</h4>
    <v-spacer></v-spacer>
    <h4 class="white--text text-lighten-2">Appointments history</h4>
    <v-icon x-small color="#76C893" class="ml-2 mr-2">fas fa-caret-down</v-icon>
    <v-btn color="#76C893" class="withoutupercase">
      <v-icon left>fas fa-plus</v-icon> New Patient
    </v-btn>
    <v-badge dot overlap color="green" class="ml-3 mr-2" dark>
      <v-avatar tile color="#76c893">
        <v-icon color="#2a6f97">fas fa-bell</v-icon>
      </v-avatar>
    </v-badge>
    <v-avatar tile color="#87986a">
      <v-img src="1.png"></v-img>
    </v-avatar>
  </v-app-bar>
</template>

<script>
export default {};
</script>

<style>
.v-btn.withoutupercase {
  text-transform: none !important;
}
</style>