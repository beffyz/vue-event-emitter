<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <TitleBtnClickChangeBox class="title__box" />
          <TitleInputChangeBox class="title__box" />
          <ColorClickChangeBox class="color__box" />
          <ColorInputChangeBox class="color__box" />
        </div>

        <div class="col-md-6">
          <TitleDescriptionClickChangeBox />
          <TitleDescriptionInputChangeBox />
          <ToggleColorBox />
          <CheckboxToggleColorBox />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import TitleBtnClickChangeBox from "@/components/TitleBtnClickChangeBox.vue";
import TitleInputChangeBox from "@/components/TitleInputChangeBox.vue";
import ColorClickChangeBox from "@/components/ColorClickChangeBox.vue";
import ColorInputChangeBox from "@/components/ColorInputChangeBox.vue";
import TitleDescriptionClickChangeBox from "@/components/TitleDescriptionClickChangeBox.vue";
import TitleDescriptionInputChangeBox from "@/components/TitleDescriptionInputChangeBox.vue";
import ToggleColorBox from "@/components/ToggleColorBox.vue";
import CheckboxToggleColorBox from "@/components/CheckboxToggleColorBox.vue";

export default defineComponent({
  name: "App",
  components: {
    CheckboxToggleColorBox,
    ToggleColorBox,
    TitleDescriptionInputChangeBox,
    TitleDescriptionClickChangeBox,
    ColorInputChangeBox,
    ColorClickChangeBox,
    TitleInputChangeBox,
    TitleBtnClickChangeBox,
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

.title__box {
  max-width: 450px;
  width: 100%;
  margin-top: 20px;
  border: 1px solid black;
  padding: 20px;
  margin-bottom: 10px;
}

.color__box {
  display: flex;
  gap: 20px;
  max-width: 450px;
  width: 100%;
  margin-top: 20px;
  border: 1px solid black;
  padding: 20px;
  margin-bottom: 10px;
}
</style>
