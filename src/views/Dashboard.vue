<template>
  <div class="dashboard">
    <v-subheader class="grey--text">Dashboard</v-subheader>
    <v-container>
      <VueCompareImage
        class="hidden-md-and-down"
        hover
        :style="{ minWidth: '1300px' }"
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
      <!-- <vue-typer class="headline" :repeat="0" text="Raja Chaudhary"></vue-typer> -->
    </v-container>
    <!-- <v-container>
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
    </v-container> -->
    <v-container class="my-5">
      <v-card flat class="pa-3">
        <v-layout row wrap class="pa-3">
          <v-flex xs12 md6>
            <div class="caption grey--text">Project Title</div>
            <div>Create a new website</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Person</div>
            <div>Tralf_</div>
          </v-flex>
          <v-flex xs6 sm4 md2>
            <div class="caption grey--text">Due Date</div>
            <div>December 25</div>
          </v-flex>
          <v-flex xs2 sm4 md2>
            <div class="caption grey--text">Status</div>
            <div>Ongoing</div>
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
  components: {
    "vue-typer": VueTyper,
    VueCompareImage,
  },
  data() {
    return {
      text1: ["Full-Stack Developer", "Software Engineer", "Python/Django/Vue"],
      // leftImage: "https://i.imgur.com/CLNHHBM.jpg",   // Old Imgur Links
      // rightImage: "https://i.imgur.com/25Yc1UC.jpg",  // Old Imgur Links
      // leftImage: "https://i.imgur.com/92bWfMT.jpg",   // Old Imgur Links
      // rightImage: "https://i.imgur.com/EJL1rqK.jpg",  // Old Imgur Links
      leftImage: "https://i.imgur.com/yNYY9Nk.jpg",
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
