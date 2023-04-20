<template>
  <section class="input-container">
    <label v-if="label">{{ label }} </label>
    <input
      type="text"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
      v-bind="$attrs"
    />
  </section>
</template>

<script setup>
import { defineProps } from "vue";
defineProps({
  label: {
    type: [String, Boolean],
    default: false,
  },
  modelValue: {
    type: String,
    default: "",
  },
});
</script>

<style lang="scss" scoped>
.input-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;

  input {
    font-size: 1rem;
    margin-left: 0.2rem;
    padding: 0.2rem;
  }
}
</style>