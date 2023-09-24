<template>
  <v-app-bar class="bg-blue">
    <v-app-bar-title>My Contacts App</v-app-bar-title>
  </v-app-bar>
  <v-container>
    <v-row no-gutters class="align-center">
      <v-col md="3" lg="3"
        ><v-sheet class="m-2 pa-2">
          <h1>{{ size }} Contacts</h1>
        </v-sheet>
      </v-col>
      <v-col md="3" lg="3"> </v-col>
      <v-col md="6" lg="6">
        <v-text-field
          label="Prepend inner"
          prepend-inner-icon="mdi-magnify"
          variant="outlined"
        ></v-text-field>
      </v-col>
    </v-row>
  </v-container>
  <v-container>
    <v-row>
      <v-col cols="3" v-for="(contact, index) in contacts" :key="index">
        <Contact
          :name="contact.name"
          :email="contact.email"
          :picture="contact.picture"
        />
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import { useFetch } from "@vueuse/core";
import Contact from "./Contact.vue";

// Parse the JSON string
const { isFetching, error, data } = await useFetch(
  "https://randomuser.me/api/?results=100"
);
const d = JSON.parse(data._value);
const contacts = d.results;

const t = "hello";

export default {
  data() {
    return {
      contacts: [],
      size: 0,
    };
  },
  mounted() {
    this.contacts = d.results;
    this.size = contacts.length;
  },
  components: {
    Contact,
  },
};
</script>
<style>
.bordered {
  border: 1px black solid;
}
v-text-field:active {
  background: #000;
}
</style>
