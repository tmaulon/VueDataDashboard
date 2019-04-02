<template>
  <aside>
    <nav role="navigation" class="VddApp_NavBar">
      <NavList class="VddApp_NavBar_List"/>
    </nav>
  </aside>
</template>

<script>
import NavList from "./NavList.vue";
import Logo from "./Logo.vue";

export default {
  name: "Aside",
  components: {
    NavList
  }
};
</script>



 

