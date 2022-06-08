<template>
  <div class="color-box" :style="{ backgroundColor: color }" />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ColorBox",
  props: { color: String },
});
</script>

<style scoped>
.color-box {
  border: 1px solid black;
  width: 100px;
  height: 70px;
}
</style>
