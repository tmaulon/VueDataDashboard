<template>
  <img :src="logo.src" :alt="logo.alt">
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
        required: true
      },
      alt: {
        type: String,
        required: true
      }
    }
  }
};
</script>

