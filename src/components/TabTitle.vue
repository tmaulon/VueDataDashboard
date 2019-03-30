<template>
  <h2>{{ tabTitle }}</h2>
</template>

<script>
export default {
  name: "TabTitle",
  props: {
    tabTitle: {
      required: true,
      type: String
    }
  }
};
</script>

