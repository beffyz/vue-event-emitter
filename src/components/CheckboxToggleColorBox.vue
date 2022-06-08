<template>
  <div class="cont">
    <CheckboxToggleColor @click="toggleVisibility" />
    <ColorBox v-if="currentVisibility" :color="currentColor" />
  </div>
</template>

<script>
import ColorBox from "@/components/ColorBox/ColorBox";
import CheckboxToggleColor from "@/components/CheckboxToggleColor/CheckboxToggleColor";
export default {
  name: "CheckboxToggleColorBox",
  components: { CheckboxToggleColor, ColorBox },
  data: () => ({
    currentColor: "Orange",
    currentVisibility: true,
  }),
  methods: {
    toggleVisibility() {
      this.currentVisibility = !this.currentVisibility;
    },
  },
};
</script>

<style scoped>
.cont {
  display: flex;
  border: 1px solid black;
  max-width: 500px;
  width: 100%;
  padding: 15px;
  margin: 20px 0 20px 0;
  gap: 60px;
}
</style>
