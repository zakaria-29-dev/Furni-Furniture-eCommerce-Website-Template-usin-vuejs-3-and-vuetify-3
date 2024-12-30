<template>
  <v-row class="mb-16 pb-16">
    <v-col cols="12">
      <v-toolbar density="compact" color="transparent">
        <v-toolbar-title>Recent Blog</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn> View All Posts </v-btn>
      </v-toolbar>
    </v-col>
    <template v-for="(item, i) in items" :key="i">
      <v-col cols="12" md="4">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            :class="{ 'on-hover': isHovering }"
            :elevation="isHovering ? 12 : 0"
            v-bind="props"
            color="transparent"
            flat
            style="border-radius: 10%"
          >
            <v-img :src="item.img" height="350px" cover> </v-img>
            <v-card-title class="text-h6 d-flex flex-column">
              <p class="mt-4">
                {{ item.title }}
              </p>

              <div>
                <p class="ma-0 text-body-1 font-weight-bold">
                  {{ item.text }}
                </p>
              </div>
            </v-card-title>
          </v-card>
        </v-hover>
      </v-col>
    </template>
  </v-row>
</template>
<script>
export default {
  data: () => ({
    icons: ["mdi-rewind", "mdi-play", "mdi-fast-forward"],
    items: [
      {
        title: "First Time Home Owner Ideas",
        text: `by Kristin Watson on Dec 19, 2021`,
        img: "post-1.jpg",
      },
      {
        title: "How To Keep Your Furniture Clean",
        text: "by Robert Fox on Dec 15, 2021",
        img: "post-2.jpg",
      },
      {
        title: "Small Space Furniture Apartment Ideas",
        text: "by Kristin Watson on Dec 12, 2021",
        img: "post-3.jpg",
      },
    ],
    transparent: "rgba(255, 255, 255, 0)",
  }),
};
</script>
<style scoped>
.v-card {
  transition: opacity 0.4s ease-in-out;
}

.v-card:not(.on-hover) {
  opacity: 0.6;
}

.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
</style>
