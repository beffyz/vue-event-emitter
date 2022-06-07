<template>
  <div>
    <form @submit.prevent @submit="submitHandler">
      <input :placeholder="placeholder" type="text" v-model="inputValue" />
      <button type="submit">
        {{ text }}
      </button>
    </form>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "TitleBtnClickChange",
  data: () => ({
    inputValue: "",
  }),
  props: {
    text: String,
    placeholder: String,
  },
  methods: {
    submitHandler() {
      this.$emit("titleBtnClickChange", this.inputValue);
      this.inputValue = "";
    },
  },
});
</script>

<style scoped />
