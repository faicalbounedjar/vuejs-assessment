<template>
  <router-link
    :to="{
      name: 'contact',
      params: {
        cell: cell,
      },
      query: {
        first: name.first,
        last: name.last,
        email: email,
        picture: picture.large,
        cell: cell,
        dob: dob.date.substring(0, 10),
        location: location.country,
        phone: phone,
        socialnumber: socialnumber,
      },
    }"
  >
    <v-hover v-slot="{ isHovering, props }" open-delay="100">
      <v-card class="tr" height="300">
        <v-img
          class="text-white"
          height="200"
          :src="picture.large"
          cover
        ></v-img>
        <h3 class="mx-5 mt-5">{{ name.first }} {{ name.last }}</h3>
        <v-card-subtitle class="">
          <v-icon class="mr-3" end icon="mdi-email"></v-icon>
          {{ email }}
        </v-card-subtitle>
      </v-card>
    </v-hover>
  </router-link>
</template>
<script>
import SvgIcon from "@jamescoyle/vue-icon";
import { mdiEmailOutline } from "@mdi/js";
export default {
  props: {
    name: "",
    email: "",
    picture: "",
    cell: "",
    dob: "",
    location: "",
    phone: "",
    socialnumber: "",
  },
  components: {
    SvgIcon,
  },
  data() {
    return {
      path: mdiEmailOutline,
    };
  },
};
</script>
<style>
.tr {
  cursor: pointer;
}
.tr:hover {
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
}
</style>
