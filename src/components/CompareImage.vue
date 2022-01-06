<template>
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
  <!-- <VueCompareImage
    class="hidden-lg-and-up"
    hover
    :style="{ maxWidth: '400px' }"
    :sliderLineWidth="sliderLine"
    :handleSize="hSize"
    :leftImage="leftImage2"
    :rightImage="rightImage2"
    :sliderPositionPercentage="sliderPosition"
  /> -->
</template>

<script>
import VueCompareImage from "vue-compare-image";

export default {
  name: "app",
  components: { VueCompareImage },
  data() {
    return {
      leftImage: "https://imgur.com/25Yc1UC",
      rightImage: "https://imgur.com/CLNHHBM",
      leftImage2: "https://i.imgur.com/SXBitjh.jpg",
      rightImage2: "https://i.imgur.com/Dcz2PGx.jpg",
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5,
    };
  },
};
</script>
