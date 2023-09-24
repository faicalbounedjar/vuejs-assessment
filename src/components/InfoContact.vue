<template>
  <v-app-bar class="bg-blue">
    <v-app-bar-title>My Contacts App</v-app-bar-title>
  </v-app-bar>
  <!-- button to go back -->

  <!-- card -->
  <v-container>
    <v-row>
      <v-col md="3" lg="3"></v-col>
      <v-col>
        <router-link to="/"
          ><v-button class="link p-5"
            ><v-icon size="30" icon="mdi-arrow-left" class="mr-2"></v-icon>Go
            back to contact List
          </v-button></router-link
        >

        <v-card class="mt-5" height="300">
          <v-row
            ><v-col md="6" lg="3">
              <v-img
                class="text-white mt-10"
                height="200"
                width="150"
                :src="url"
                cover
              ></v-img>
            </v-col>
            <v-col md="6" lg="9">
              <v-card-title col="12"
                >{{ $route.query.first }} {{ $route.query.last }}
              </v-card-title>
              <v-card-text class="py-0">
                <v-row class="mt-3" no-gutters>
                  <v-col cols="3" class="">
                    <v-icon size="30" icon="mdi-phone"></v-icon
                  ></v-col>
                  <v-col class="text-h5" cols="9">
                    {{ $route.query.phone }}
                  </v-col>
                </v-row>

                <v-row class="mt-3" no-gutters>
                  <v-col cols="3" class="">
                    <v-icon size="30" icon="mdi-cake"></v-icon
                  ></v-col>
                  <v-col class="text-h5" cols="9"
                    >{{ $route.query.dob }}
                  </v-col>
                </v-row>
                <v-row class="mt-3" no-gutters>
                  <v-col cols="3" class="">
                    <v-icon size="30" icon="mdi-card-account-details"></v-icon
                  ></v-col>
                  <v-col class="text-h5" cols="9"
                    >{{ $route.query.socialnumber }}
                  </v-col>
                </v-row>
                <v-row class="mt-3" no-gutters>
                  <v-col cols="3" class="">
                    <v-icon class="gray" size="30" icon="mdi-earth"></v-icon
                  ></v-col>
                  <v-col class="text-h5" cols="9">
                    {{ $route.query.location }}
                  </v-col>
                </v-row>
              </v-card-text>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col md="3" lg="3"></v-col>
    </v-row>
  </v-container>
</template>

<script>
import { useFetch } from "@vueuse/core";
export default {
  data() {
    return {
      url: null,
      cell: null,
    };
  },
  mounted() {
    this.cell = this.$route.params.cell;
    this.url = this.$route.query.picture;
  },
};
</script>

<style>
.link {
  text-decoration: none;
  color: black;

  padding: 15px;
}
.link:hover {
  background: #bdbdbd;
  transition: all;
}
</style>
