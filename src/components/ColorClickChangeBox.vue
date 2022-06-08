<template>
  <div>
    <ColorClickChange
      :v-model="inputValue"
      @inputColorValue="colorClickChange"
    />
    <ColorBox :color="boxColor" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ColorClickChange from "@/components/ColorClickChange/ColorClickChange.vue";
import ColorBox from "@/components/ColorBox/ColorBox.vue";

export default defineComponent({
  name: "ColorClickChangeBox",
  components: { ColorBox, ColorClickChange },
  data: () => ({
    boxColor: "aqua",
    inputValue: "",
  }),
  methods: {
    colorClickChange(color: string) {
      this.boxColor = color;
      this.inputValue = "";
    },
  },
});
</script>

<style scoped></style>
