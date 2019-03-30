<template>
  <nav>
    <ul v-if="navigation.length">
      <NavItem
        :lien="lien"
        :text="text"
        :classIcon="classIcon"
        v-for="(lien, key) in navigation"
        :key="key"
      />
    </ul>
    <p v-else>Il n'y a aucun lien de navigation.</p>
  </nav>
</template>


<script>
import NavItem from "./NavItem.vue";

export default {
  components: {
    NavItem
  },
  name: "NavBar",
  data() {
    return {
      navigation: [
        {
          text: "Déconnexion",
          classIcon: "fas fa-power-off"
        },
        {
          text: "Formulaire",
          classIcon: "fab fa-wpforms"
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

<style scoped>
</style>
