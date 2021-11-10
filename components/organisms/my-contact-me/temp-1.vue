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
            <span class="ml-2 title">Cebu City, Philippines</span>
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
            <a href="https://www.linkedin.com/in/rangie-laurente-486600195/" target="_blank" class="text-decoration-none">
              <v-icon color="my_primary" size="28" class="mt-n1 pointer-event">
                mdi-linkedin
              </v-icon>
            </a>
          </div>
        </v-col>
        <v-col cols="12" md="7">
          <!-- <form action="https://www.actionforms.io/e/r/rangie-laurente1-test">
            <label for="fname">First name:</label><br>
            <input type="text" id="fname" name="fname" value="John"><br>
            <label for="lname">Last name:</label><br>
            <input type="text" id="lname" name="lname" value="Doe"><br><br>
            <input type="submit" value="Submit">
            <v-hover v-slot="{ hover }">
                  <v-btn
                    type="submit"
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
          </form> -->

          <form action="https://www.actionforms.io/e/r/rangie-laurente1-test" @submit="submitForm">
            <v-row>
              <v-col cols="12">
                <label class="white--text title">Name</label>
                <v-text-field
                  v-model="name"
                  id="name" 
                  type="text" 
                  name="name"
                  height="65"
                  class="mt-2 my-text-style"
                  color="my_primary"
                  :dark="isFocusName"
                  :solo="!isFocusName"
                  @focus="focusName"
                  @blur="focusName"
                  :rules="[rules.required]"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <label class="white--text title">Phone Number</label>
                <v-text-field
                  v-model="phone"
                  id="phonenumber"
                  type="number" 
                  name="phonenumber"
                  color="my_primary"
                  :dark="isFocusPhone"
                  :solo="!isFocusPhone"
                  @focus="focusPhone"
                  @blur="focusPhone"
                  height="65"
                  class="mt-2"
                  :rules="[rules.required]"
                ></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <label class="white--text title">Email</label>
                <v-text-field
                  v-model="email"
                  id="email"
                  type="email"
                  name="email"
                  color="my_primary"
                  :dark="isFocusEmail"
                  :solo="!isFocusEmail"
                  @focus="focusEmail"
                  @blur="focusEmail"
                  height="65"
                  class="mt-2"
                  :rules="[rules.required, rules.emailRules]"
                ></v-text-field>
              </v-col>
              <v-col cols="12">
                <label class="white--text title">Your Message</label>
                <v-textarea
                  v-model="message"
                  id="message"
                  type="text"
                  name="message"
                  color="my_primary"
                  :dark="isFocusMessage"
                  :solo="!isFocusMessage"
                  @focus="focusMessage"
                  @blur="focusMessage"
                  class="mt-2"
                  :rules="[rules.required]"
                ></v-textarea>
              </v-col>
              <v-col cols="12">
                <v-hover v-slot="{ hover }">
                  <v-btn
                    type="submit"
                    width="30%"
                    :loading="isLoading"
                    :disabled="disabledBtn"
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
          </form>
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
      isFocusMessage: false,
      isLoading: false,
      rules: {
        required: value => !!value || "Required.",
        emailRules :  v => /^\w+([.-]?\w+)*@\w+([.-]?\w+)*(\.\w{2,3})+$/.test(v) || 'E-mail must be valid'
      },
      name: '',
      email: '',
      phone: '',
      message: '',
      formArr: [],
      isEmailValid: false,
      disabledBtn: true
    };
  },

  watch: {

    formArr: function(val){
      if(val){
        let newArr = [...new Set(val)]
        if(newArr.length === 4){
          this.disabledBtn = false
        }else {
          this.disabledBtn = true
        }
      }
    },

    name: function(val){
      if(val){
        this.formArr.push('name')
      }else {
        this.formArr = this.formArr.filter(e => e !== 'name')
      }
    },

    phone: function(val){
      if(val){
        this.formArr.push('phone')
      }else {
        this.formArr = this.formArr.filter(e => e !== 'phone')
      }
    },

    email: function(val){
      if(val){
        this.validateEmail(val)
        if(this.isEmailValid){
          this.formArr.push('email')
        }else {
          this.formArr = this.formArr.filter(e => e !== 'email')
        }
      }else {
        this.formArr = this.formArr.filter(e => e !== 'email')
      }
    },

    message: function(val){
      if(val){
        this.formArr.push('message')
      }else {
        this.formArr = this.formArr.filter(e => e !== 'message')
      }
    }
  },

  methods: {

     validateEmail(value) {
        if (value) {
            const reg = /\S+@{1}[a-zA-Z]+\.[a-zA-Z]+/.test(value)
            if(reg){
              this.isEmailValid = true
            }else {
              this.isEmailValid = false
            }
        }
    },

    submitForm(){
      this.isLoading = true
    },

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
.pointer-event{
  cursor: pointer;
}

 .my-text-style >>> .v-text-field__slot hint {
    color: yellow
  }
</style>