<template>
  <div style="height: 600px; width: 100%; background-color: #3f5d50">
    <v-app-bar color="#3F5D50" flat class="px-16">
      <v-app-bar-title>Furni.</v-app-bar-title>
      <v-spacer></v-spacer>
      <v-tabs
        v-model="tab"
        align-tabs="center"
        color="yellow"
        v-for="(link, i) in links"
        :key="i"
      >
        <v-tab :value="i + 1" class="text-none">{{ link }}</v-tab>
      </v-tabs>
      <v-icon class="far fa-user ml-16 mr-4" color=""></v-icon>
      <v-icon class="fas fa-dolly me-4" color=""></v-icon>
    </v-app-bar>
    <v-row>
      <v-col cols="5" class="CG">
        <h1 class="text-white CT" style="font-weight: 700; font-size: 54px">
          Modern Interior
        </h1>
        <br />
        <h1 class="text-white CT" style="font-weight: 700; font-size: 54px">
          Design Studio
        </h1>
        <p class="text-grey CT">
          Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet <br />
          velit. Aliquam vulputate velit imperdiet dolor tempor tristique.
        </p>
        <v-btn
          class="text-none mt-10 mr-5 CT"
          color="yellow"
          min-width="92"
          rounded
        >
          Shop Now
        </v-btn>
        <v-btn
          class="text-none mt-10"
          color="white"
          min-width="92"
          variant="outlined"
          rounded
        >
          Explore
        </v-btn>
      </v-col>
      <v-col cols="7" class="CD">
        <div
          class=""
          style="
            background: url('dots-light.svg');
            width: 255px;
            height: 217px;
            background-repeat: no-repeat;
            position: absolute;
            margin-left: 500px;
            margin-top: 50px;
          "
        ></div>
        <v-img
          src="\couch.png"
          max-height="600"
          contain
          class="mb-n16 mr-10"
        ></v-img>
      </v-col>
    </v-row>
  </div>
</template>
<script setup>
const links = ["Home", "Shop", "About us", "Services", "Blog", "Contact us"];
</script>
<script>
export default {
  data: () => ({
    tab: null,
  }),
};
</script>
<style>
.CG {
  margin-top: 100px;
}
.CT {
  margin-left: 150px;
}
</style>
