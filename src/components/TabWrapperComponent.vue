<template>
  <div class="tab-wrapper">
    <TabTitle :tabTitle="tabTitle"/>
    <TabComponent/>
  </div>
</template>

<script>
import TabComponent from "./TabComponent.vue";
import TabTitle from "./TabTitle.vue";

export default {
  name: "TabWrapperComponent",
  components: {
    TabComponent,
    TabTitle
  },
  data() {
    return {
      tabTitle: "Et si on y insérait un tableau..."
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
