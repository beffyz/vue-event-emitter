<template>
  <input v-model="inputValue" placeholder="Aqua" class="input" type="text" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ColorInputChange",
  data: () => ({
    inputValue: "",
  }),
});
</script>

<style scoped>
.input {
  height: 30px;
  margin-right: 70px;
}
</style>
