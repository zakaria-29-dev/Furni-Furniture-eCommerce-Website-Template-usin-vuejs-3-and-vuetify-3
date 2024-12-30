<template>
  <v-row>
    <v-col cols="12">
      <v-carousel
        height="400"
        hide-delimiter-background
        cycle
        show-arrows="hover"
        color="green"
      >
        <v-carousel-item v-for="(slide, i) in slides" :key="i">
          <v-sheet height="100%" color="transparent">
            <div
              class="d-flex fill-height justify-center align-center text-center px-16"
            >
              <div class="">
                <h1>{{ slide.title }}</h1>
                <p class="px-16">{{ slide.text }}</p>
                <v-avatar
                  :image="slide.avatar"
                  size="48"
                  class="mt-2"
                ></v-avatar>
                <h4>{{ slide.name }}</h4>
                <p>{{ slide.cert }}</p>
              </div>
            </div>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
    </v-col>
  </v-row>
</template>
<script>
export default {
  data() {
    return {
      slides: [
        {
          title: "Testimonials",
          text: "Donec facilisis quam ut purus rutrum lobortis. Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate velit imperdiet dolor tempor tristique. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Integer convallis volutpat dui quis scelerisque.",
          avatar: "person-1.jpg",
          name: "Maria Jones",
          cert: "CEO, Co-Founder, XYZ Inc.",
        },
        {
          title: "Testimonials",
          text: "Donec facilisis quam ut purus rutrum lobortis. Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate velit imperdiet dolor tempor tristique. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Integer convallis volutpat dui quis scelerisque.",
          avatar: "person_3.jpg",
          name: "Maria Jones",
          cert: "CEO, Co-Founder, XYZ Inc.",
        },
        {
          title: "Testimonials",
          text: "Donec facilisis quam ut purus rutrum lobortis. Donec vitae odio quis nisl dapibus malesuada. Nullam ac aliquet velit. Aliquam vulputate velit imperdiet dolor tempor tristique. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Integer convallis volutpat dui quis scelerisque.",
          avatar: "person_4.jpg",
          name: "Maria Jones",
          cert: "CEO, Co-Founder, XYZ Inc.",
        },
      ],
    };
  },
};
</script>
