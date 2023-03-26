<template>
  <v-card color="white" class="rounded-lg mt-2 card__picker" flat>
    <v-row justify="center" class="pt-2">
      <v-date-picker
        v-model="picker"
        color="#457b9d"
        width="380"
      ></v-date-picker>
    </v-row>

    <v-toolbar color="transparent" flat class="mt-4">
      <h4 class="black--text">Doctors</h4>
      <v-spacer></v-spacer>
      <v-avatar tile color="#ECF5FF">
        <v-icon color="#2784FF">fas fa-angle-up</v-icon>
      </v-avatar>
    </v-toolbar>
    <v-list class="mt-n6" color="transparent" dense>
      <v-list-item v-for="chat in chats" :key="chat.title">
        <v-list-item-avatar tile>
          <v-img :src="chat.img" />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title
            v-text="chat.title"
            class="black--text"
          ></v-list-item-title>
          <v-list-item-subtitle
            v-text="chat.subtitle"
            class="grey--text"
          ></v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    chats: [
      {
        img: "d2.png",
        subtitle: "Therapist",
        title: "Dr. Bilge Köşe",
      },
      {
        img: "d1.png",
        subtitle: "Surgeon",
        title: "Dr. Oğuzhan Ötleş",
      },
      {
        img: "d3.png",
        subtitle: "Neurologist",
        title: "Dr. Eren Alkan",
      },
    ],

    picker: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
      .toISOString()
      .substring(0, 10),
  }),
};
</script>

<style>
.card__picker {
  position: absolute;
  right: 50px;
}
</style>