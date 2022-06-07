<template>
  <div>
    <h1>{{ currentTitle }}</h1>
    <TitleBtnClickChange
      placeholder="Update title..."
      @titleBtnClickChange="titleBtnClickChange"
      text="Change"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import TitleBtnClickChange from "@/components/TitleBtnClickChange/TitleBtnClickChange.vue";
export default defineComponent({
  name: "TitleBtnClickChangeBox",
  data: () => ({
    currentTitle: "Title",
  }),
  components: { TitleBtnClickChange },
  methods: {
    titleBtnClickChange(title: string) {
      this.currentTitle = title;
    },
  },
});
</script>

<style scoped></style>
