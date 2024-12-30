<template>
  <v-footer class="">
    <v-row justify="center" no-gutters class="mt-16">
      <v-col cols="6" class="px-8">
        <div class="text-subtitle-1 text-medium-emphasis">
          <v-btn
            class="text-none"
            prepend-icon="far fa-envelope"
            variant="text"
          >
            Subscribe to Newsletter
          </v-btn>
        </div>
        <v-row>
          <v-col cols="5">
            <v-text-field
              density="compact"
              placeholder="Enter your name"
              variant="outlined"
              color="teal-lighten-5"
            ></v-text-field>
          </v-col>
          <v-col cols="5">
            <v-text-field
              density="compact"
              placeholder="Enter your email"
              color="teal-lighten-5"
              variant="outlined"
            ></v-text-field>
          </v-col>
          <v-col cols="2">
            <v-btn
              class="me-2 text-none text-white"
              color="#344D43"
              prepend-icon="fas fa-paper-plane"
              variant="flat"
            >
              Share
            </v-btn>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="6">
        <v-img
          src="\sofa.png"
          cover
          max-height="400"
          max-width="400"
          style="margin-top: -150px; margin-left: 150px"
        >
        </v-img>
      </v-col>
      <v-col cols="12">
        <h1 style="color: #344d43; margin-left: 50px; margin-top: -100px">
          Furni.
        </h1>
      </v-col>
      <v-col cols="12">
        <v-row>
          <v-col cols="4">
            <p class="text-grey ml-10">
              Donec facilisis quam ut purus rutrum lobortis. Donec vitae odio
              quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam
              vulputate velit imperdiet dolor tempor tristique. Pellentesque
              habitant
            </p>
            <div>
              <div class="ml-8 mt-5">
                <v-btn
                  v-for="icon in icons"
                  :key="icon"
                  :icon="icon"
                  class="mx-1 text-teal"
                  color="#EFF2F1"
                ></v-btn>
              </div>
            </div>
          </v-col>
          <v-col cols="2">
            <p class="text-grey">About us</p>
            <p class="text-grey">Services</p>
            <p class="text-grey">Blog</p>
            <p class="text-grey">Contact us</p>
          </v-col>
          <v-col cols="2">
            <p class="text-grey">Support</p>
            <p class="text-grey">Knowledge base</p>
            <p class="text-grey">Live chat</p>
          </v-col>
          <v-col cols="2">
            <p class="text-grey">Jobs</p>
            <p class="text-grey">Our team</p>
            <p class="text-grey">Leadership</p>
            <p class="text-grey">Privacy Policy</p>
          </v-col>
          <v-col cols="2">
            <p class="text-grey">Nordic Chair</p>
            <p class="text-grey">Kruzo Aero</p>
            <p class="text-grey">Ergonomic Chair</p>
          </v-col>
        </v-row>
      </v-col>
      <v-col class="text-center mt-4" cols="12">
        <v-divider class="mx-10"></v-divider>
      </v-col>
      <v-col cols="12">
        <v-row class="my-12 px-16">
          <v-col cols="8">
            <p class="text-grey">
              Copyright ©2024. All Rights Reserved. — Designed with love by
              Untree.co
            </p>
          </v-col>
          <v-col cols="4">
            <p class="text-grey">Terms & Conditions --- Privacy Policy</p>
          </v-col>
        </v-row>
      </v-col>
      <div class="px-4 py-4 bgCol text-center w-100 text-white"></div>
    </v-row>
  </v-footer>
</template>

  <script>
export default {
  data: () => ({
    icons: [
      "fab fa-facebook",
      "fab fa-twitter",
      "fab fa-linkedin",
      "fab fa-instagram-square",
    ],
  }),
};
</script>

  <style>
.v-footer {
  padding: 0 0 !important;
}
.bgCol {
  background-color: #eff2f1;
}
.bgTop {
  background-color: #111111;
}
.bgMidum {
  background-color: #1f1f1f;
}
</style>

