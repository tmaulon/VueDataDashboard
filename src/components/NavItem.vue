<template>
  <li>
    <a href="#" :title="lien.text" class="VddApp_NavBar_List_Item_Link">
      <i class="VddApp_NavBar_List_Item_Link_Icon" :class="lien.classIcon"></i>
      <span class="VddApp_NavBar_List_Item_Link_Label">{{ lien.text }}</span>
    </a>
  </li>
</template>

<script>
export default {
  name: "NavItem",
  props: {
    lien: {
      type: Object,
      required: true,
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