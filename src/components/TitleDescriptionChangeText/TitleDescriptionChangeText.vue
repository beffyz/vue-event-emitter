<template>
  <div class="title-desc">
    <h2>{{ currentTitle }}</h2>
    <h2>{{ currentDescription }}</h2>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "TitleDescriptionClickChangeText",
  props: {
    currentTitle: String,
    currentDescription: String,
  },
});
</script>

<style scoped>
.title-desc {
  display: flex;
  flex-direction: column;
}
</style>
