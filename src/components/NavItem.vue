<template>
  <li>
    <a href="#" :title="lien.text">
      <i :class="lien.classIcon"></i>
      <font-awesome-icon icon="coffee"/>
      <span class="link__label">{{ lien.text }}</span>
    </a>
  </li>
</template>

<script>
export default {
  name: "NavItem",
  props: {
    lien: {
      type: Object,
      text: {
        type: String,
        required: true
      },
      classIcon: {
        type: String,
        required: true
      }
    }
  }
};
</script>