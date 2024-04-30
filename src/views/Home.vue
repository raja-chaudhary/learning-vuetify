<template>
  <div class="home">
    <!-- <v-subheader class="grey--text">Dashboard</v-subheader> -->
    <v-container>
      <VueCompareImage
        class="hidden-md-and-down"
        hover
        :style="{ minWidth: '1100px' }"
        :sliderLineWidth="sliderLine"
        :handleSize="hSize"
        :leftImage="leftImage"
        :rightImage="rightImage"
        :sliderPositionPercentage="sliderPosition"
      />
      <VueCompareImage
        class="hidden-lg-and-up"
        hover
        :style="{ maxWidth: '400px' }"
        :sliderLineWidth="sliderLine"
        :handleSize="hSize"
        :leftImage="leftImage2"
        :rightImage="rightImage2"
        :sliderPositionPercentage="sliderPosition"
      />
    </v-container>
    <v-container class="d-flex justify-center">
      <v-layout row wrap class="pa-0">
        <v-flex xs12 md12>
          <vue-typer
            class="headline d-flex justify-center"
            :repeat="0"
            text="Raja Chaudhary"
          ></vue-typer>
          <vue-typer
            class="d-flex justify-center"
            :text="text1"
            :repeat="Infinity"
            :shuffle="false"
            initial-action="erasing"
            :pre-type-delay="70"
            :type-delay="70"
            :pre-erase-delay="1980"
            :erase-delay="150"
            erase-style="select-back"
            :erase-on-complete="false"
            caret-animation="smooth"
          ></vue-typer>
        </v-flex>
      </v-layout>
    </v-container>

    <!-- Intro Para -->
    <v-container>
      <div class="text-h5 px-2">
        About<span class="deep-purple--text text--accent-2">Me</span>
      </div>
      <div class="px-2">
        Hi, I’m
        <span class="deep-purple--text text--accent-2">@raja-chaudhary</span>.
        I’m interested in backend development using
        <span class="deep-purple--text text--accent-2">Django (Python)</span> and
        <span class="deep-purple--text text--accent-2"
          >SpringBoot (Java)</span
        >
        . I am comfortable utilizing
        <span class="deep-purple--text text--accent-2">Vue</span> to make my web
        apps more lively and user friendly however, I prefer
        <span class="deep-purple--text text--accent-2">HTMX</span> for front-end
        dynamic rendering. I have more than <span class="deep-purple--text text--accent-2">5+ years of experience</span> in software
        development. I have navigated diverse organizational structures, including startups, freelance contract work,
and top IT firms. Demonstrating agility, reliability, and proficiency in collaborative team environments or independent
roles, I bring accountability and expertise in technologies including AWS services, Splunk monitoring, LaunchDarkly
feature toggling and more. Proven ability to contribute to software development at any scale.
      </div>
    </v-container>

    <!-- Social Media Links -->
    <v-container class="my-5">
      <v-card flat class="pa-3">
        <v-layout row wrap class="pa-3">
          <v-flex xs4 sm4 md4 class="px-0">
            <div
              class="
                subtitle-2
                text-decoration-underline
                deep-purple--text
                text--accent-2
              "
            >
              Social Media
            </div>
            <div class="my-2 px-1" style="height: 50px">
              <span class="hidden-sm-and-down">LinkedIn</span>
              <a
                href="https://www.linkedin.com/in/raja-chaudhary/"
                target="_blank"
                class="my-2"
                style="text-decoration: none"
                ><v-icon right class="deep-purple--text text--accent-2"
                  >mdi-linkedin</v-icon
                ></a
              >
            </div>
            <div class="my-2 px-1" style="height: 50px">
              <span class="hidden-sm-and-down">GitHub</span>
              <a
                href="https://github.com/raja-chaudhary"
                target="_blank"
                class="my-2"
                style="text-decoration: none"
                ><v-icon right class="deep-purple--text text--accent-2"
                  >mdi-github</v-icon
                ></a
              >
            </div>
          </v-flex>
          <v-flex xs4 sm4 md4 class="px-0">
            <div
              class="
                subtitle-2
                text-decoration-underline
                deep-purple--text
                text--accent-2
              "
            >
              Username/Link
            </div>
            <div class="my-2 px-1 hidden-sm-and-down" style="height: 50px">
              <a
                href="https://www.linkedin.com/in/raja-chaudhary/"
                target="_blank"
                class="my-2"
                style="text-decoration: none"
                >linkedin.com/raja-chaudhary</a
              >
            </div>
            <div class="my-2 px-1 hidden-sm-and-up body-2" style="height: 50px">
              <a
                href="https://www.linkedin.com/in/raja-chaudhary/"
                target="_blank"
                class="my-2"
                style="text-decoration: none"
                >linkedin.com/raja-chaudhary</a
              >
            </div>
            <div class="my-2 px-1 hidden-sm-and-down" style="height: 50px">
              <a
                href="https://github.com/raja-chaudhary"
                class="my-2"
                style="text-decoration: none"
                >github.com/raja-chaudhary</a
              >
            </div>
            <div class="my-2 px-1 hidden-sm-and-up body-2" style="height: 50px">
              <a
                href="https://github.com/raja-chaudhary"
                class="my-2"
                style="text-decoration: none"
                >github.com/raja-chaudhary</a
              >
            </div>
          </v-flex>
          <v-flex xs4 sm4 md4>
            <div
              class="
                subtitle-2
                text-decoration-underline
                deep-purple--text
                text--accent-2
              "
            >
              Status
            </div>
            <div
              class="my-2 pa-1 green--text text--darken-1 hidden-sm-and-down"
              style="height: 50px"
            >
              Actively Looking for Job
            </div>
            <div
              class="
                body-2
                my-2
                px-1
                green--text
                text--darken-1
                hidden-sm-and-up
              "
              style="height: 50px; line-height: normal"
            >
              Actively Looking for Job
            </div>
            <div
              class="my-2 pa-1 yellow--text text--darken-4 hidden-sm-and-down"
              style="height: 50px"
            >
              Moderately Active
            </div>
            <div
              class="
                my-2
                px-1
                yellow--text
                text--darken-4
                hidden-sm-and-up
                body-2
              "
              style="height: 50px; line-height: normal"
            >
              Moderately Active
            </div>
          </v-flex>
        </v-layout>
      </v-card>
    </v-container>
  </div>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";
export default {
  name: "app",
  metaInfo: {
    title: "Home",
    titleTemplate: "Raja Chaudhary → %s",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { name: "description", content: "Raja Chaudhary's Portfolio Website" },
      { charset: "utf-8" },
      { property: "og:title", content: "Raja Chaudhary" },
      { property: "og:site_name", content: "Raja Chaudhary" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "http://www.rajachaudhary.com" },
      {
        property: "og:image",
        content: "https://i.imgur.com/CyLZ4N9.jpg",
      },
      {
        property: "og:description",
        content: "Raja Chaudhary's Portfolio Website",
      },
    ],
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage,
  },
  data() {
    return {
      text1: [
        "Full-Stack Developer",
        "Software Developer",
        "Python/Django/Java/SpringBoot/Vue/HTMX",
      ],
      // leftImage: "https://i.imgur.com/CLNHHBM.jpg",   // Old Imgur Links
      // rightImage: "https://i.imgur.com/25Yc1UC.jpg",  // Old Imgur Links
      // leftImage: "https://i.imgur.com/92bWfMT.jpg",   // Old Imgur Links
      // rightImage: "https://i.imgur.com/EJL1rqK.jpg",  // Old Imgur Links
      leftImage: "https://i.imgur.com/5UxuZLj.jpg",
      rightImage: "https://i.imgur.com/MlY2iZp.jpg",
      leftImage2: "https://i.imgur.com/up14PTL.jpg",
      rightImage2: "https://i.imgur.com/WyEj77R.jpg",
      sliderLine: 0.1,
      hSize: 0,
      sliderPosition: 0.5,
    };
  },
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }
  50% {
    transform: rotateZ(10deg);
  }
}
.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: #7c4dff;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}
.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: #7c4dff;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
