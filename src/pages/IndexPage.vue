<template>
  <q-page class="q-pa-md">
    <div class="text-h5 q-mb-md">Basic Form</div>

    <q-form @submit="onSubmit" class="q-gutter-md">
      <q-input filled v-model="form.name" label="Name" />
      <q-input filled v-model="form.email" label="Email" type="email" />
      <q-input filled v-model="form.message" label="Message" type="textarea" />

      <q-btn label="Submit" type="submit" color="primary" />
    </q-form>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const form = ref({
  name: '',
  email: '',
  message: ''
})

function onSubmit () {
  alert(`Name: ${form.value.name}\nEmail: ${form.value.email}\nMessage: ${form.value.message}`)
}
</script>
