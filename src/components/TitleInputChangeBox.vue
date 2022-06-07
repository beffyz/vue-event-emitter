<template>
  <div>
    <h1>{{ currentTitle }}</h1>
    <TitleInputChange v-model="currentTitle" placeholder="Update title..." />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TitleInputChange from "@/components/TitleInputChange/TitleInputChange.vue";

export default defineComponent({
  name: "TitleInputChangeBox",
  components: { TitleInputChange },
  data: () => ({
    currentTitle: "Title",
  }),
});
</script>

<style scoped></style>
