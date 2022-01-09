<template>
  <nav>
    <v-app-bar flat app>
      <v-app-bar-nav-icon
        class="deep-purple--text text--accent-2"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase">
        <span class="font-weight-light">Raja</span>
        <span class="deep-purple--text text--accent-2">Chaudhary</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <a href="./resume.pdf" target="_blank" style="text-decoration: none"
        ><v-btn plain color="black" class="d-none d-sm-flex">
          <span class="font-weight-light">Resume</span>
          <v-icon class="deep-purple--text text--accent-2"
            >mdi-file-pdf-box</v-icon
          >
        </v-btn></a
      >
      <a href="./resume.pdf" target="_blank" style="text-decoration: none"
        ><v-btn plain color="black" class="d-flex d-sm-none">
          <span class="font-weight-light caption">Resume</span>
          <v-icon class="deep-purple--text text--accent-2"
            >mdi-file-pdf-box</v-icon
          >
        </v-btn></a
      >
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app class="deep-purple accent-2">
      <v-list dense>
        <v-list-item
          v-for="link in links"
          :key="link.text"
          router
          :to="link.route"
        >
          <v-list-item-action>
            <v-icon right class="white--text">{{ link.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title class="white--text">
              {{ link.text }}
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        { icon: "mdi-shield-home-outline", text: "Home", route: "/" },
        {
          icon: "mdi-folder-star-outline",
          text: "Skills & Portfolio",
          route: "/portfolio",
        },
        {
          icon: "mdi-human-greeting-proximity",
          text: "Contact",
          route: "/contact",
        },
      ],
    };
  },
};
</script>