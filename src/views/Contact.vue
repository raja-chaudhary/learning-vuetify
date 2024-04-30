<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md6 lg6 xl6>
        <h2 class="pb-4 mt-2">
          <span>GetIn</span>
          <span class="deep-purple--text text--accent-2">Touch</span>
        </h2>
        <div class="py-4 subheading font-weight-bold">
          <v-icon medium color="deep-purple accent-2" left
            >mdi-leaf-maple</v-icon
          >
          <span>Toronto,&nbsp;</span>
          <span class="deep-purple--text text--accent-2">Canada</span>
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon medium color="deep-purple accent-2" left>mdi-at</v-icon>
          <a href="mail:raja@rajachaudhary.com  " style="text-decoration: none"
            ><span class="black--text">raja@</span>
            <span class="deep-purple--text text--accent-2"
              >rajachaudhary.com</span
            ></a
          >
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon medium color="deep-purple accent-2" left
            >mdi-cellphone</v-icon
          >
          <a href="tel:2368825646" style="text-decoration: none"
            ><span class="black--text">+1&nbsp;</span>
            <span class="deep-purple--text text--accent-2"
              >(236) 882-5646</span
            ></a
          >
        </div>
        <div class="py-4 subheading font-weight-bold">
          <v-icon medium color="deep-purple accent-2" left>mdi-linkedin</v-icon>
          <a
            href="linkedin.com/in/raja-chaudhary/"
            target="_blank"
            style="text-decoration: none"
            ><span class="black--text">https://www.linkedin.com/in/</span>
            <span class="deep-purple--text text--accent-2"
              >raja-chaudhary/</span
            ></a
          >
        </div>
      </v-flex>

      <v-flex xs12 sm12 md6 lg6 xl6>
        <h2 class="pb-4 mb-4">
          <span>Contact</span>
          <span class="deep-purple--text text--accent-2">Form</span>
        </h2>

        <form method="POST" action="https://formspree.io/f/xzbodpwk">
          <v-text-field
            name="name"
            color="deep-purple accent-2"
            background-color="transparent"
            v-model="name"
            :error-messages="nameErrors"
            label="Name"
            required
            @blur="$v.name.$touch()"
          ></v-text-field>
          <v-text-field
            type="email"
            color="deep-purple accent-2"
            background-color="transparent"
            name="email"
            v-model="email"
            :error-messages="emailErrors"
            label="E-mail"
            required
            @blur="$v.email.$touch()"
          ></v-text-field>
          <v-textarea
            color="deep-purple accent-2"
            background-color="transparent"
            :counter="200"
            :error-messages="bodyErrors"
            v-model="body"
            label="Textarea"
            name="body"
            @blur="$v.body.$touch()"
          ></v-textarea>
          <v-btn
            @click="submit"
            type="submit"
            color="deep-purple accent-2"
            class="white--text mx-1"
            :disabled="body.length <= 20"
            >SEND MESSAGE</v-btn
          >
          <v-btn @click="clear" class="mx-1">clear</v-btn>
        </form>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
import { validationMixin } from "vuelidate";
import {
  required,
  maxLength,
  email,
  minLength,
} from "vuelidate/lib/validators";
export default {
  mixins: [validationMixin],
  validations: {
    name: { required, maxLength: maxLength(20) },
    email: { required, email },
    body: { required, minLength: minLength(20) },
  },
  data() {
    return {
      name: "",
      email: "",
      body: "",
    };
  },
  methods: {
    submit() {
      this.$v.$touch();
    },
    clear() {
      this.$v.$reset();
      this.name = "";
      this.email = "";
      this.body = "";
    },
  },
  computed: {
    nameErrors() {
      const errors = [];
      if (!this.$v.name.$dirty) return errors;
      !this.$v.name.maxLength &&
        errors.push("Name must be at most 20 characters long");
      !this.$v.name.required && errors.push("Name is required.");
      return errors;
    },
    emailErrors() {
      const errors = [];
      if (!this.$v.email.$dirty) return errors;
      !this.$v.email.email && errors.push("Must be valid e-mail");
      !this.$v.email.required && errors.push("E-mail is required");
      return errors;
    },
    bodyErrors() {
      const errors = [];
      if (!this.$v.body.$dirty) return errors;
      !this.$v.body.minLength &&
        errors.push("Text must be at least 20 characters long");
      !this.$v.body.required && errors.push("Text is required");
      return errors;
    },
  },
};
</script>