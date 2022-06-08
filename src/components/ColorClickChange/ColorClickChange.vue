<template>
  <form @submit.prevent @submit="handleChange">
    <input type="text" placeholder="Aqua" v-model="inputValue" />
    <button type="submit">Change</button>
  </form>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ColorClickChange",
  data: () => ({
    inputValue: "",
  }),
  methods: {
    handleChange() {
      this.$emit("inputColorValue", this.inputValue);
      this.inputValue = "";
    },
  },
});
</script>

<style scoped></style>
