<template>
  <div class="portfolio">
    <!-- Skills -->
    <div class="text-center deep-purple--text text--accent-2 text-h5 mb-4">
      Skills
    </div>
    <!-- Large Screens -->
    <v-container class="d-none d-sm-flex">
      <v-layout row wrap class="pa-3">
        <v-flex
          xs12
          sm6
          md3
          v-for="skill in skills"
          :key="skill.type"
          class="pa-1"
        >
          <v-card
            class="d-flex flex-column mx-auto"
            max-width="300"
            min-height="260"
          >
            <v-card-text>
              <!-- <div>Word of the Day</div> -->
              <p class="text-h5 text--primary">
                {{ skill.type }}
                <v-icon right class="deep-purple--text text--accent-2 mb-1">{{
                  skill.icon
                }}</v-icon>
              </p>

              <p>{{ skill.exp }}</p>
              <div class="text--primary">
                {{ skill.line1 }}<br />
                {{ skill.line2 }}
              </div>
            </v-card-text>
            <v-spacer></v-spacer>
            <v-card-actions>
              <v-btn
                text
                color="deep-purple accent-2"
                @click="skill.reveal = true"
              >
                Learn More
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <v-card
                v-if="skill.reveal"
                class="
                  d-flex
                  flex-column
                  transition-fast-in-fast-out
                  v-card--reveal
                "
                style="height: 100%"
              >
                <v-card-text class="pb-0">
                  <p class="text-h5 text--primary">
                    Details
                    <v-icon
                      right
                      class="deep-purple--text text--accent-2 mb-1"
                      >{{ skill.icon }}</v-icon
                    >
                  </p>
                  <p class="text-caption">{{ skill.detail }}</p>
                </v-card-text>
                <v-spacer></v-spacer>
                <v-card-actions class="pt-0">
                  <v-btn
                    text
                    color="deep-purple accent-2"
                    @click="skill.reveal = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-expand-transition>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Mobile Carousel -->
    <v-container class="d-flex d-sm-none">
      <v-carousel hide-delimiters height="260">
        <v-carousel-item v-for="skill in skills" :key="skill.type">
          <v-card
            class="d-flex flex-column mx-auto"
            max-width="300"
            min-height="260"
          >
            <v-card-text>
              <!-- <div>Word of the Day</div> -->
              <p class="text-h5 text--primary">
                {{ skill.type }}
                <v-icon right class="deep-purple--text text--accent-2 mb-1">{{
                  skill.icon
                }}</v-icon>
              </p>

              <p>{{ skill.exp }}</p>
              <div class="text--primary">
                {{ skill.line1 }}<br />
                {{ skill.line2 }}
              </div>
            </v-card-text>
            <v-spacer></v-spacer>
            <v-card-actions>
              <v-btn
                text
                color="deep-purple accent-2"
                @click="skill.reveal = true"
              >
                Learn More
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <v-card
                v-if="skill.reveal"
                class="
                  d-flex
                  flex-column
                  transition-fast-in-fast-out
                  v-card--reveal
                "
                style="height: 100%"
              >
                <v-card-text class="pb-0">
                  <p class="text-h5 text--primary">
                    Details
                    <v-icon
                      right
                      class="deep-purple--text text--accent-2 mb-1"
                      >{{ skill.icon }}</v-icon
                    >
                  </p>
                  <p class="text-caption">{{ skill.detail }}</p>
                </v-card-text>
                <v-spacer></v-spacer>
                <v-card-actions class="pt-0">
                  <v-btn
                    text
                    color="deep-purple accent-2"
                    @click="skill.reveal = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-expand-transition>
          </v-card>
        </v-carousel-item>
      </v-carousel>
    </v-container>

    <!-- Frameworks -->
    <div class="text-center deep-purple--text text--accent-2 text-h5 my-4">
      Frameworks
    </div>
    <!-- Large Screens -->
    <v-container class="d-none d-sm-flex">
      <v-layout row wrap class="pa-3">
        <v-flex
          xs12
          sm6
          md3
          v-for="framework in frameworks"
          :key="framework.type"
          class="pa-1"
        >
          <v-card
            class="d-flex flex-column mx-auto"
            max-width="300"
            min-height="260"
          >
            <v-card-text>
              <!-- <div>Word of the Day</div> -->
              <p class="text-h5 text--primary">
                {{ framework.type }}
                <v-icon right class="deep-purple--text text--accent-2 mb-1">{{
                  framework.icon
                }}</v-icon>
              </p>

              <p>{{ framework.exp }}</p>
              <div class="text--primary">
                {{ framework.line1 }}<br />
                {{ framework.line2 }}
              </div>
            </v-card-text>
            <v-spacer></v-spacer>
            <v-card-actions>
              <v-btn
                text
                color="deep-purple accent-2"
                @click="framework.reveal = true"
              >
                Learn More
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <v-card
                v-if="framework.reveal"
                class="
                  d-flex
                  flex-column
                  transition-fast-in-fast-out
                  v-card--reveal
                "
                style="height: 100%"
              >
                <v-card-text class="pb-0">
                  <p class="text-h5 text--primary">
                    Details
                    <v-icon
                      right
                      class="deep-purple--text text--accent-2 mb-1"
                      >{{ framework.icon }}</v-icon
                    >
                  </p>
                  <p class="text-caption">{{ framework.detail }}</p>
                </v-card-text>
                <v-spacer></v-spacer>
                <v-card-actions class="pt-0">
                  <v-btn
                    text
                    color="deep-purple accent-2"
                    @click="framework.reveal = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-expand-transition>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Mobile Carousel -->
    <v-container class="d-flex d-sm-none">
      <v-carousel hide-delimiters height="260">
        <v-carousel-item v-for="framework in frameworks" :key="framework.type">
          <v-card
            class="d-flex flex-column mx-auto"
            max-width="300"
            min-height="260"
          >
            <v-card-text>
              <!-- <div>Word of the Day</div> -->
              <p class="text-h5 text--primary">
                {{ framework.type }}
                <v-icon right class="deep-purple--text text--accent-2 mb-1">{{
                  framework.icon
                }}</v-icon>
              </p>

              <p>{{ framework.exp }}</p>
              <div class="text--primary">
                {{ framework.line1 }}<br />
                {{ framework.line2 }}
              </div>
            </v-card-text>
            <v-spacer></v-spacer>
            <v-card-actions>
              <v-btn
                text
                color="deep-purple accent-2"
                @click="framework.reveal = true"
              >
                Learn More
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <v-card
                v-if="framework.reveal"
                class="
                  d-flex
                  flex-column
                  transition-fast-in-fast-out
                  v-card--reveal
                "
                style="height: 100%"
              >
                <v-card-text class="pb-0">
                  <p class="text-h5 text--primary">
                    Details
                    <v-icon
                      right
                      class="deep-purple--text text--accent-2 mb-1"
                      >{{ framework.icon }}</v-icon
                    >
                  </p>
                  <p class="text-caption">{{ framework.detail }}</p>
                </v-card-text>
                <v-spacer></v-spacer>
                <v-card-actions class="pt-0">
                  <v-btn
                    text
                    color="deep-purple accent-2"
                    @click="framework.reveal = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-expand-transition>
          </v-card>
        </v-carousel-item>
      </v-carousel>
    </v-container>

    <!-- Projects -->
    <div class="text-center deep-purple--text text--accent-2 text-h5 my-4">
      Projects
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // reveal: false,
      skills: [
        {
          type: "Python",
          icon: "mdi-language-python",
          exp: "2+ years of experience",
          line1: "My preferred language.",
          line2:
            "'Extremely comfortable with writing, reading, testing and debugging.'",
          detail:
            "Been continuously using python for past 2 years, previously with my employer and currently for my clients. Have also built various portfolio projects in Python - one of them being a SaaS tool.",
          reveal: false,
        },
        {
          type: "Javascript",
          icon: "mdi-language-javascript",
          exp: "2+ years of experience",
          line1: "Most used language.",
          line2: "'Diversified experience in JS.'",
          detail:
            "Can comfortably write vanilla JS and have also used third-party libraries to implement dynamic effects on websites. Comfortable using JQuery/AJAX for performing asynchronous tasks.",
          reveal: false,
        },
        {
          type: "CSS",
          icon: "mdi-language-css3",
          exp: "2+ years of experience",
          line1: "SASS/Tailwind.",
          line2:
            "'I don't always rely on JS libraries for things that can be achieved using CSS.'",
          detail:
            "Highly proficient with CSS properties, flex/grid layouts. My deliverables always include responsive websites. I also ensure that the website is responsive on all major web browsers.",
          reveal: false,
        },
        {
          type: "GitHub",
          icon: "mdi-github",
          exp: "2+ years of experience",
          line1: "Git/Git CLI.",
          line2:
            "'Always maintaining a version control of all of my projects.'",
          detail:
            "I never start a project without maintaining a git repository for it. I have also hosted various websites using git CLI on hosting services like Heroku.",
          reveal: false,
        },
      ],
      frameworks: [
        {
          type: "Django",
          icon: "mdi-language-python",
          exp: "2+ years of experience",
          line1: "Highly Proficient.",
          line2:
            "'Experience creating all sort of websites including blogs/e-commerce/saas.'",
          detail:
            "The Django MVT model is like a second nature to me. Writing complex queries, creating webhooks, integrating third-party APIs, utilizing multiprocessors etc. I have worked on most of the commonly used Django features.",
          reveal: false,
        },
        {
          type: "Vue",
          icon: "mdi-vuejs",
          exp: "4 months of experience",
          line1: "Currently learning.",
          line2:
            "'Always wanted to work with Vue, great dev community to be a part of.'",
          detail:
            "My portfolio website is built on Vuetify, a framework on top of Vue. Finishing my portfolio website gave me confidence to work more with Vue in the future. I can now create components, routes, can integrate third-party plugins etc.",
          reveal: false,
        },
        {
          type: "HTMX",
          icon: "mdi-code-tags",
          exp: "4 months of experience",
          line1: "Currently learning.",
          line2: "'A perfect front-end framework that compliments Django.'",
          detail:
            "My portfolio website is built on Vuetify, a framework on top of Vue. Finishing my portfolio website gave me confidence to work more with Vue in the future. I can now create components, routes, can integrate third-party plugins etc.",
          reveal: false,
        },
      ],
    };
  },
};
</script>
<style>
.v-card--reveal {
  bottom: 0;
  opacity: 1 !important;
  position: absolute;
  width: 100%;
}
</style>