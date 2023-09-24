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
        <v-button class=""
          ><v-icon size="30" icon="mdi-arrow-left" class="mr-2"></v-icon>Go back
          to contact List</v-button
        >

        <v-card class="mt-5" height="300">
          <v-card-title col="12">fee</v-card-title>

          <v-row>
            <v-col class="ml-5">
              <v-img
                class="text-white"
                height="200"
                width="150"
                src="https://randomuser.me/api/portraits/men/84.jpg"
                cover
              ></v-img>
            </v-col>
            <v-card-text class="py-0">
              <v-row class="mt-3" no-gutters>
                <v-col cols="3" class="">
                  <v-icon size="30" icon="mdi-phone"></v-icon
                ></v-col>
                <v-col class="text-h4" cols="9"> 64&deg;F </v-col>
              </v-row>
              <v-row class="mt-3" no-gutters>
                <v-col cols="3" class="">
                  <v-icon size="30" icon="mdi-cake"></v-icon
                ></v-col>
                <v-col class="text-h4" cols="9"> 64&deg;F </v-col>
              </v-row>
              <v-row class="mt-3" no-gutters>
                <v-col cols="3" class="">
                  <v-icon size="30" icon="mdi-card"></v-icon
                ></v-col>
                <v-col class="text-h4" cols="9"> 64&deg;F </v-col>
              </v-row>
              <v-row class="mt-3" no-gutters>
                <v-col cols="3" class="">
                  <v-icon size="30" icon="mdi-earth"></v-icon
                ></v-col>
                <v-col class="text-h4" cols="9"> 64&deg;F </v-col>
              </v-row>
            </v-card-text>
          </v-row>
        </v-card>
      </v-col>
      <v-col md="3" lg="3"></v-col>
    </v-row>
  </v-container>
</template>

<script></script>
