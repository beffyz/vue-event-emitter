<template>
  <input class="input" type="text" v-model="inputValue" />
</template>

<script>
import { defineComponent } from "vue";
export default defineComponent({
  name: "TextInput",
  data: () => ({
    inputValue: "",
  }),
});
</script>

<style scoped>
.input {
  height: 30px;
  width: 200px;
}
</style>
