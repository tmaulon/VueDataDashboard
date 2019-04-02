<template>
  <ul v-if="navigation.length">
    <NavItem
      class="VddApp_NavBar_List_Item"
      v-for="(lien, key) in navigation"
      :key="key"
      :lien="lien"
    />
  </ul>
  <p v-else class="VddApp_ErrorMsg">Il n'y a aucun lien de navigation.</p>
</template>


<script>
import NavItem from "./NavItem.vue";

export default {
  name: "NavList",
  components: {
    NavItem
  },
  data() {
    return {
      navigation: [
        {
          text: "Formulaire",
          classIcon: "fas fa-pencil-alt"
        },
        {
          text: "Interventions",
          classIcon: "fas fa-list-ul"
        },
        {
          text: "Interventions à traiter",
          classIcon: "fas fa-clipboard-list"
        },
        {
          text: "Interventions prioritaires",
          classIcon: "fas fa-star"
        },
        {
          text: "Interventions traitées",
          classIcon: "fas fa-clipboard-check"
        },
        {
          text: "Paramètres",
          classIcon: "fas fa-cog"
        }
      ]
    };
  }
};
</script>

