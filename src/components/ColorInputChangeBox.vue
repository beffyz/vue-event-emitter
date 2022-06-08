<template>
  <div>
    <ColorInputChange v-model="inputValue" />
    <ColorBox :color="inputValue" />
  </div>
</template>

<script>
import { defineComponent } from "vue";

import ColorBox from "@/components/ColorBox/ColorBox";
import ColorInputChange from "@/components/ColorInputChange/ColorInputChange";

export default defineComponent({
  name: "ColorInputChangeBox",
  data: () => ({
    inputValue: "Aqua",
  }),
  components: { ColorInputChange, ColorBox },
});
</script>

<style scoped></style>
