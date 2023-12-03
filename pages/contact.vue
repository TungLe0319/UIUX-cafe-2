<script setup >
import IconDivider from "~/components/Globals/IconDivider.vue";
import Button from '../components/Globals/Button.vue';
import { ref } from 'vue';

const firstName = ref('');
const lastName = ref('');
const email = ref('');
const subject = ref('');
const content = ref('')
const requiredRule = (value) => value ? true : 'This field is required.';
const emailRule = (value) => /.+@.+\..+/.test(value) || 'Enter a valid email address.';

const firstNameRules = [requiredRule];
const lastNameRules = [requiredRule];
const emailRules = [requiredRule, emailRule];
const subjectRules = [requiredRule];
const contentRule = [requiredRule];
</script>

<template>
  <main class="   flex flex-col items-center justify-center px-10">
    <div class="flex flex-col items-center justify-center mt-24">
      <h1 class=" text-4xl lg:text-8xl font-bold text-center text-amber-400 font-serif">Contact Us</h1>
      <hr class=" my-5 w-full">
      <p class="text-center text-amber-400">We'd love to hear from you!</p>
    </div>
    <section class="lg:flex  items-start justify-center mt-10 w-full  ">
      <div class="lg:w-1/3 flex flex-col items-center justify-center">
        <h1 class="text-2xl font-bold  text-amber-400 font-serif">Lorem Ipsum Café</h1>
        <div class="w-full my-10">
          <IconDivider />
        </div>
        <div class=" text-start flex flex-col items-start space-y-5">
          <p class="text-center ">Monday - Friday: 9am - 5pm</p>
          <p class="text-center ">Saturday: 10am - 4pm</p>
          <p class="text-center ">Sunday: Closed</p>
        </div>
        <div class="w-full my-10">
          <IconDivider />
        </div>
        <div class=" text-start flex flex-col items-start space-y-5">
          <p class="text-center ">1234 Fake Street</p>
          <p class="text-center ">Fake City, Fake State 12345</p>
          <div class="flex items-center justify-center space-x-4">
            <Icon name="fluent:call-end-16-filled" class="text-amber-400" />
            <a href="tel:123-456-7890" class="text-amber-400">123-456-7890</a>
          </div>
          <div class="flex items-center justify-center space-x-4">
            <Icon name="uil:envelope" class="text-amber-400" />
            <a href="tel:123-456-7890" class="text-amber-400">123fake@email.com</a>
          </div>
        </div>
      </div>
      <div class="lg:w-2/3 ">
        <div class="lg:hidden block text-center font-serif  mt-10 lg:mt-0 ">
          Leave us a message!
           <IconDivider class="my-10 lg:my-0" />
        </div>
        <v-form @submit.prevent>
          <v-container>
            <v-row class="mb-4">
              <v-col cols="12" md="6">
                <v-text-field v-model="firstName" :rules="firstNameRules" label="First name"
                  color="orange-lighten-2"></v-text-field>
              </v-col>
              <v-col cols="12" md="6">
                <v-text-field v-model="lastName" label="Last name" :rules="lastNameRules"
                  color="orange-lighten-2"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field v-model="email" label="E-mail" :rules="emailRules" color="orange-lighten-2"></v-text-field>
              </v-col>
              <v-col cols="12">
                <v-text-field v-model="subject" label="Subject" :rules="subjectRules"
                  color="orange-lighten-2"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea v-model="content" :rules="contentRule" clearable label="Content"
              color="orange-lighten-2"></v-textarea>
            <v-btn type="submit" variant="outlined" block color="orange-lighten-2" class="mt-2 ">Send a message</v-btn>
          </v-container>
        </v-form>
      </div>
    </section>
  </main>
</template>

<style scoped>
.form {
  @apply rounded-md p-2 ring-2 ring-amber-400 focus:ring bg-[var(--night)];
}
</style>
