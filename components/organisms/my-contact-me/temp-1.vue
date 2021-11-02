<template>
  <div class="project-container">
    <v-container fill-height class="my-16 py-16">
      <v-row>
        <v-col cols="12" class="d-flex justify-center">
          <div class="display-3 white--text">
            <div class="mb-4">Contact Me</div>
            <v-divider
              v-for="i in 5"
              :key="i"
              class="mx-16 my_primary"
            ></v-divider>
          </div>
        </v-col>
      </v-row>
      <v-row class="mt-16">
        <v-col cols="12" md="5">
          <div class="headline white--text font-weight-light mb-16">
            Contact Info
          </div>
          <div class="white--text mb-10">
            <v-icon color="my_primary" size="28" class="mt-n2">
              mdi-map-marker
            </v-icon>
            <span class="ml-2 title"> DroitThemes, Mirpur DOHS, Dhaka </span>
          </div>
          <div class="white--text mb-10">
            <v-icon color="my_primary" size="28" class="mt-n1">
              mdi-email
            </v-icon>
            <span class="ml-2 title"> rangielaurente12stem@gmail.com </span>
          </div>
          <div class="white--text mb-16">
            <v-icon color="my_primary" size="28" class="mt-n1">
              mdi-cellphone
            </v-icon>
            <span class="ml-2 title"> +63-938-073-8443 </span>
          </div>
          <div class="white--text">
            <div class="headline white--text mb-6">Follow Me</div>
            <v-icon color="my_primary" size="28" class="mt-n1">
              mdi-linkedin
            </v-icon>
            <v-icon color="my_primary" size="28" class="mt-n1 ml-1">
              mdi-instagram
            </v-icon>
          </div>
        </v-col>
        <v-col cols="12" md="7">
          <v-form>
            <v-row>
              <v-col cols="12">
                <label class="white--text title">Name</label>
                <v-text-field
                  height="65"
                  class="mt-2 text-black"
                  color="my_primary"
                  :dark="isFocusName"
                  :solo="!isFocusName"
                  @focus="focusName"
                  @blur="focusName"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <label class="white--text title">Phone Number</label>
                <v-text-field
                  color="my_primary"
                  :dark="isFocusPhone"
                  :solo="!isFocusPhone"
                  @focus="focusPhone"
                  @blur="focusPhone"
                  height="65"
                  class="mt-2"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <label class="white--text title">Email</label>
                <v-text-field
                  color="my_primary"
                  :dark="isFocusEmail"
                  :solo="!isFocusEmail"
                  @focus="focusEmail"
                  @blur="focusEmail"
                  height="65"
                  class="mt-2"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <label class="white--text title">Your Message</label>
                <v-textarea
                  color="my_primary"
                  :dark="isFocusMessage"
                  :solo="!isFocusMessage"
                  @focus="focusMessage"
                  @blur="focusMessage"
                  class="mt-2"
                ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-hover v-slot="{ hover }">
                  <v-btn
                    width="30%"
                    height="70"
                    class="
                      rounded-lg
                      white--text
                      text-capitalize
                      title
                      font-weight-black
                    "
                    :outlined="hover"
                    color="my_primary"
                  >
                    Send Message
                  </v-btn>
                </v-hover>
              </v-col>
            </v-row>
          </v-form>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "contactForm",
  data() {
    return {
      isFocusName: false,
      isFocusPhone: false,
      isFocusEmail: false,
      isFocusMessage: false
    };
  },

  methods: {
    focusName() {
      if (this.isFocusName) {
        this.isFocusName = false;
      } else {
        this.isFocusName = true;
      }
    },

    focusPhone() {
      if (this.isFocusPhone) {
        this.isFocusPhone = false;
      } else {
        this.isFocusPhone = true;
      }
    },

    focusEmail() {
      if (this.isFocusEmail) {
        this.isFocusEmail = false;
      } else {
        this.isFocusEmail = true;
      }
    },

    focusMessage() {
      if (this.isFocusMessage) {
        this.isFocusMessage = false;
      } else {
        this.isFocusMessage = true;
      }
    }
  }
};
</script>

<style scoped>
.text-black input {
  color: green !important;
}
</style>