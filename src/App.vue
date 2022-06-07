<template>
  <section>
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <TitleBtnClickChangeBox class="title__box" />
          <TitleInputChangeBox class="title__box" />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import TitleBtnClickChangeBox from "@/components/TitleBtnClickChangeBox.vue";
import TitleInputChangeBox from "@/components/TitleInputChangeBox.vue";

export default defineComponent({
  name: "App",
  components: {
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
  max-width: 350px;
  width: 100%;
  margin-top: 20px;
  border: 1px solid black;
  padding: 20px;
  margin-bottom: 10px;
}
</style>
