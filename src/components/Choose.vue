<template>
  <v-row class="mt-16">
    <v-col cols="7">
      <h1 class="CRT mt-16">Why Choose Us</h1>
      <p class="text-grey CRT">
        Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet<br />
        velit. Aliquam vulputate velit imperdiet dolor tempor tristique.
      </p>
      <v-row>
        <v-col cols="6" v-for="(cho, i) in chooses" :key="i">
          <v-card class="mx-auto my-8" max-width="344" color="transparent" flat>
            <v-card-item>
              <v-icon :class="cho.icon" color=""></v-icon>
              <v-card-title>
                {{ cho.title }}
              </v-card-title>
            </v-card-item>

            <v-card-text class="text-grey">
              {{ cho.desciption }}
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="5">
      <div
        class=""
        style="
          background: url('dots-yellow.svg');
          width: 255px;
          height: 217px;
          background-repeat: no-repeat;
          position: absolute;
          margin-left: -100px;
          margin-top: -30px;
        "
      ></div>
      <v-img
        src="\why-choose-us-img.jpg"
        max-height="550"
        contain
        class="mr-12 mt-10"
      ></v-img>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    model: null,
    chooses: [
      {
        title: "Fast & Free Shipping",
        icon: "fas fa-shipping-fast",
        desciption:
          "Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate.",
      },
      {
        title: "Easy to Shop",
        icon: "fas fa-shopping-bag",
        desciption:
          "Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate.",
      },
      {
        title: "24/7 Support",
        icon: "far fa-life-ring",
        desciption:
          "Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate.",
      },
      {
        title: "Hassle Free Returns",
        icon: "fas fa-sync-alt",
        desciption:
          "Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate.",
      },
    ],
  }),
};
</script>
<style>
</style>
