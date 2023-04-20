<template>
  <form class="form-container">
    <VInput
      v-model="firstName"
      type="text"
      label="Firstname: "
      placeholder="Your firstname..."
    />
    <VInput
      v-model="lastName"
      type="text"
      label="Lastname: "
      placeholder="Your lastname..."
    />
    <VInput
      v-model="email"
      type="email"
      label="Email: "
      placeholder="Your email..."
    />
  </form>
</template>

<script setup>
import VInput from "./components/VInput.vue";
import { ref } from "vue";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.form-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;
}
</style>
