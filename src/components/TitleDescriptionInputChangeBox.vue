<template>
  <div class="cont">
    <div>
      <TitleDescriptionInputChangeForm v-model="titleValue" />
      <TitleDescriptionInputChangeForm v-model="descriptionValue" />
    </div>
    <TitleDescriptionChangeText
      :current-title="titleValue"
      :current-description="descriptionValue"
    />
  </div>
</template>

<script>
import { defineComponent } from "vue";

import TitleDescriptionChangeText from "@/components/TitleDescriptionChangeText/TitleDescriptionChangeText";
import TitleDescriptionInputChangeForm from "@/components/TitleDescriptionInputChangeForm/TitleDescriptionInputChangeForm";
export default defineComponent({
  name: "TitleDescriptionInputChangeBox",
  components: { TitleDescriptionInputChangeForm, TitleDescriptionChangeText },
  data: () => ({
    titleValue: "Title",
    descriptionValue: "Description",
  }),
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
