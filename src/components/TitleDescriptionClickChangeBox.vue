<template>
  <div class="cont">
    <TitleDescriptionClickChangeForm
      @changeTitle="changeTitle"
      @changeDescription="changeDescription"
    />
    <TitleDescriptionClickChangeText
      :current-title="currentTitle"
      :current-description="currentDescription"
    />
  </div>
</template>

<script>
import { defineComponent } from "vue";

import TitleDescriptionClickChangeForm from "@/components/TitleDescriptionClickChangeForm/TitleDescriptionClickChangeForm";
import TitleDescriptionClickChangeText from "@/components/TitleDescriptionChangeText/TitleDescriptionChangeText";
export default defineComponent({
  name: "TitleDescriptionClickChangeBox",
  components: {
    TitleDescriptionClickChangeText,
    TitleDescriptionClickChangeForm,
  },
  data: () => ({
    currentTitle: "Title",
    currentDescription: "Description",
    titleValue: "",
    descriptionValue: "",
  }),
  methods: {
    changeTitle(title) {
      this.currentTitle = title;

      this.titleValue = "";
    },
    changeDescription(description) {
      this.currentDescription = description;

      this.descriptionValue = "";
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
}
</style>
