<template>
  <v-row class="mt-16">
    <v-col cols="5">
      <h1 class="CRT mt-16">Crafted with</h1>
      <br />
      <h1 class="CRT">excellent materia</h1>
      <p class="text-grey CRT">
        Donec vitae odio quis nisl dapibus malesuada. <br />
        Nullam ac aliquet velit. Aliquam vulputate velit<br />
        imperdiet dolor tempor tristique.
      </p>
      <v-btn
        class="text-none text-white mt-10 mr-5 CRT"
        color="black"
        min-width="92"
        rounded
      >
        Explore
      </v-btn>
    </v-col>
    <v-col cols="7">
      <v-row>
        <v-col cols="4" v-for="(cli, i) in clients" :key="i">
          <div>
            <v-hover v-slot="{ isHovering, props }">
              <v-card
                class="mx-auto"
                color="transparent"
                max-width="600"
                v-bind="props"
                flat
              >
                <v-img :src="cli.avatar" cover> </v-img>
                <v-expand-transition>
                  <div
                    v-if="isHovering"
                    class="d-flex transition-fast-in-fast-out bg-green-lighten-2 v-card--reveal text-h2"
                    style="height: 70%"
                  >
                    <v-btn
                      icon="fas fa-plus"
                      color="black"
                      style="z-index: 9999"
                    ></v-btn>
                  </div>
                </v-expand-transition>

                <v-card-text class="pt-6">
                  <div
                    class="font-weight-light text-grey text-h6 mb-2 text-center"
                  >
                    {{ cli.title }}
                  </div>

                  <h5 class="text-h5 font-weight mb-2 text-center">
                    {{ cli.price }}
                  </h5>
                </v-card-text>
              </v-card>
            </v-hover>
          </div>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    model: null,
    clients: [
      { title: "Nordic Chair", avatar: "product-1.png", price: "$50.00" },
      { title: "Kruzo Aero Chair", avatar: "product-2.png", price: "$78.00" },
      { title: "Ergonomic Chair", avatar: "product-3.png", price: "$43.00" },
    ],
  }),
};
</script>
<style>
.CRT {
  margin-left: 100px;
}
.v-card--reveal {
  align-items: end;
  bottom: 0;
  justify-content: right;
  opacity: 0.15;
  position: absolute;
  width: 100%;
  border-radius: 10px;
  padding: 10px;
}
</style>
