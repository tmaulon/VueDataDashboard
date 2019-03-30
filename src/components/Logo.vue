<template>
  <img width="25%" :src="logo.src.value" :alt="logo.alt.value">
</template>

<script>
export default {
  name: "Logo",
  props: {
    logo: {
      type: Object,
      required: true,
      src: {
        type: String,
        required: true,
        value: ""
      },
      alt: {
        type: String,
        required: true,
        value: ""
      }
    }
  }
};
</script>

<style scoped>
</style>
