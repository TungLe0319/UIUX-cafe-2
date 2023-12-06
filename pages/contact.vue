<script setup >
import IconDivider from "~/components/Globals/IconDivider.vue";

import { ref } from 'vue';
import PageHeader from "~/components/Globals/PageHeader.vue";


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
  <main class="    ">
    <PageHeader title="Contact Us" content="  Lorem ipsum dolor, sit amet consectetur adipisicing elit." />
    <section class="lg:flex  items-start justify-center mt-32 w-full  ">
      <div v-motion-slide-visible-left class="lg:w-1/3 flex flex-col items-center justify-center">
        <h1 class="text-2xl font-bold  text-amber-400 font-serif">Lorem Ipsum Café</h1>
        <div class="w-full my-10">
          <IconDivider />
        </div>
        <div class=" text-start flex flex-col items-start space-y-5">
          <p class="text-center ">Monday - Friday: 9am - 5pm</p>
          <p class="text-center ">Saturday - Sunday: 10am - 4pm</p>
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
      <div v-motion-slide-visible-right class="lg:w-2/3 ">
        <div v-motion-pop-visible class="lg:hidden block text-center font-serif  mt-10 lg:mt-0 ">
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
    <section class=" my-24 ">
       <div class="flex flex-col items-center  justify-center  my-10 lg:my-20">
      
          <div v-motion-pop-visible class="text-4xl font-serif text-center"> Find us! </div>
          <div v-motion-pop-visible class="w-full pt-8">
            <IconDivider />
          </div>
          <div v-motion-pop-visible class="w-2/3 text-center my-8 text-gray-500">
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Amet, iure optio rem nihil placeat laboriosam id
              tempora aliquid quam, maxime eligendi dolorem eum quisquam eius!</p>
          </div>
        
        </div>
        <div v-motion-slide-visible-bottom class="lg:flex  items-center justify-center gap-10">
     <Icon  name="uil:facebook" class="text-8xl text-amber-400 " />
          <Icon  name="uil:instagram" class="text-8xl text-amber-400 " />
          <Icon  name="uil:youtube" class="text-8xl text-amber-400 " />
          <Icon  name="fa6-brands:x-twitter" class="text-8xl text-amber-400 " />
     
        </div>
     
    </section>
  </main>
</template>

<style scoped>
.form {
  @apply rounded-md p-2 ring-2 ring-amber-400 focus:ring bg-[var(--night)];
}
</style>
