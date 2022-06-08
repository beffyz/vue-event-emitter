<template>
  <div class="cont">
    <ToggleColorBoxBtn @click="toggleVisibility" />
    <ColorBox v-if="currentVisibility" :color="currentColor" />
  </div>
</template>

<script>
import { defineComponent } from "vue";

import ToggleColorBoxBtn from "@/components/ToggleColorBoxBtn/ToggleColorBoxBtn";
import ColorBox from "@/components/ColorBox/ColorBox";
export default defineComponent({
  name: "ToggleColorBox",
  components: { ColorBox, ToggleColorBoxBtn },
  data: () => ({
    currentColor: "Orange",
    currentVisibility: true,
  }),
  methods: {
    toggleVisibility() {
      this.currentVisibility = !this.currentVisibility;
    },
  },
});
</script>

<style scoped>
.cont {
  display: flex;
  border: 1px solid black;
  max-width: 500px;
  width: 100%;
  padding: 15px;
  margin: 20px 0 20px 0;
  gap: 80px;
}
</style>
