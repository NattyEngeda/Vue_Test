<script setup>
import { reactive } from "vue";
const message = "Hello World";
const state = reactive({
  seen: true,
});

function changeSeen() {
  seen = !seen;
}
console.log(seen);

var url = "https://www.facebook.com";
</script>

<template>
  <h1>{{ message.split("").reverse().join("") }}</h1>
  <button @click="changeSeen">Click Me</button>
  <br />
  <h1 v-if="seen">Seen</h1>
  <a :href="url" target="_blank">Google.com</a>
</template>

<style scoped>
#id {
  color: red;
}
</style>
