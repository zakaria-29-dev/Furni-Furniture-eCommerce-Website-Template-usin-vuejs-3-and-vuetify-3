<template>
  <v-row class="mt-16">
    <v-col cols="7">
      <v-row>
        <v-col cols="8">
          <div
            class=""
            style="
              background: url('dots-green.svg');
              width: 255px;
              height: 217px;
              background-repeat: no-repeat;
              position: absolute;
              margin-left: 0px;
              margin-top: -30px;
            "
          ></div>
          <v-img
            src="\img-grid-1.jpg"
            max-height="600"
            contain
            class="CRT mt-10"
          ></v-img>
        </v-col>
        <v-col cols="4">
          <v-img
            src="\img-grid-2.jpg"
            max-height="200"
            contain
            class="mt-10 ml-n2"
            style="border-radius: 10%"
          ></v-img>
          <v-img
            src="\img-grid-3.jpg"
            max-height="400"
            contain
            class="mt-5"
            style="margin-left: -120px; border-radius: 10%"
          ></v-img>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="5">
      <h2 class="CRT mt-16">We Help You Make Modern</h2>
      <br />
      <h2 class="CRT">Interior Design</h2>
      <p class="text-grey CRT">
        Donec facilisis quam ut purus rutrum lobortis. Donec vitae odio quis
        nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate
        velit<br />
        imperdiet dolor tempor tristique. Pellentesque habitant morbi tristi.<br />
      </p>
      <v-row>
        <v-col cols="6">
          <v-row class="mt-6">
            <v-col cols="2">
              <v-icon class="far fa-circle" size="x-small"></v-icon>
            </v-col>
            <v-col cols="10">
              <p class="text-grey">
                Donec vitae odio quis nisl<br />
                dapibus malesuada
              </p>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="6">
          <v-row class="mt-6">
            <v-col cols="2">
              <v-icon class="far fa-circle" size="x-small"></v-icon>
            </v-col>
            <v-col cols="10">
              <p class="text-grey">
                Donec vitae odio quis nisl<br />
                dapibus malesuada
              </p>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="6">
          <v-row class="">
            <v-col cols="2">
              <v-icon class="far fa-circle" size="x-small"></v-icon>
            </v-col>
            <v-col cols="10">
              <p class="text-grey">
                Donec vitae odio quis nisl<br />
                dapibus malesuada
              </p>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="6">
          <v-row class="">
            <v-col cols="2">
              <v-icon class="far fa-circle" size="x-small"></v-icon>
            </v-col>
            <v-col cols="10">
              <p class="text-grey">
                Donec vitae odio quis nisl<br />
                dapibus malesuada
              </p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-btn
        class="text-none text-white mt-10 mr-5 CRT"
        color="black"
        min-width="92"
        rounded
      >
        Explore
      </v-btn>
    </v-col>
    <v-col cols="12">
      <v-row class="px-16 mt-16">
        <v-col cols="4" v-for="(mode, i) in moders" :key="i">
          <v-card color="transparent" flat class="mx-auto">
            <v-row>
              <v-col cols="4">
                <div
                  class="bg-green-lighten-2 rounded-lg mx-auto"
                  style="
                    height: 120px;
                    width: 120px;
                    margin-top: 10px;
                    opacity: 0.4;
                  "
                >
                  <v-img :src="mode.avatar" cover> </v-img>
                </div>
              </v-col>
              <v-col cols="8">
                <v-card-item>
                  <div>
                    <div class="text-h6 mb-1">
                      {{ mode.title }}
                    </div>
                    <div class="text-caption">
                      {{ mode.obs }} {{ mode.obs1 }}
                    </div>
                  </div>
                </v-card-item>
                <v-card-actions>
                  <v-btn> Read More </v-btn>
                </v-card-actions>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    model: null,
    moders: [
      {
        title: "Nordic Chair",
        avatar: "product-1.png",
        obs: "Donec facilisis quam ut purus rutrum",
        obs1: "lobortis. Donec vitae ",
      },
      {
        title: "Kruzo Aero Chair",
        avatar: "product-2.png",
        obs: "Donec facilisis quam ut purus rutrum",
        obs1: "lobortis. Donec vitae ",
      },
      {
        title: "Ergonomic Chair",
        avatar: "product-3.png",
        obs: "Donec facilisis quam ut purus rutrum",
        obs1: "lobortis. Donec vitae ",
      },
    ],
  }),
};
</script>
