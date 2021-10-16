<template>
  <div class="home">
    <h1>Home Page</h1>
    <v-btn class="pink white--text mx-lg-3">click me</v-btn>
    <v-btn depressed color="pink mx-lg-3">click me</v-btn>
    <v-btn text color="pink mx-lg-3">click me</v-btn>

    <v-btn depressed class="pink white--text mx-lg-3">
      <v-icon left>mdi-email-alert</v-icon>
      <span>email me</span>
    </v-btn>

    <v-btn fab depressed dark color="purple lighter-2">
      <v-icon>mdi-heart</v-icon>
    </v-btn>
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>
