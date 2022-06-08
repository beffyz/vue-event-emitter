<template>
  <div>
    <form @submit.prevent @submit="titleSubmitHandler">
      <input v-model="titleValue" placeholder="Update title..." type="text" />
      <button type="submit">Change</button>
    </form>
    <form @submit.prevent @submit="descriptionSubmitHandler">
      <input
        v-model="descriptionValue"
        placeholder="Update description..."
        type="text"
      />
      <button type="submit">Change</button>
    </form>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TitleDescriptionClickChangeForm",
  data: () => ({
    titleValue: "",
    descriptionValue: "",
  }),
  methods: {
    titleSubmitHandler() {
      console.log(this.titleValue);
      this.$emit("changeTitle", this.titleValue);
      this.titleValue = "";
    },
    descriptionSubmitHandler() {
      console.log(this.descriptionValue);
      this.$emit("changeDescription", this.descriptionValue);
      this.descriptionValue = "";
    },
  },
});
</script>

<style scoped></style>
