<template>
  <input :placeholder="placeholder" v-model="inputValue" type="text" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "TitleInputChange",
  data: () => ({
    inputValue: "",
  }),
  props: {
    placeholder: String,
  },
});
</script>

<style scoped></style>
