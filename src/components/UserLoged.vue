<template>
  <button @click="logOut()" id="sign-out-button">
    <i class="fas fa-user-circle"></i>
    {{ fullName }}
  </button>
</template>
<script>
export default {
  name: "UserLoged",
  computed: {
    fullName: {
      // getter
      getName: function() {
        return this.firstName + " " + this.lastName;
      },
      // setter
      setName: function(newValue) {
        let names = newValue.split(" ");
        this.firstName = names[0];
        this.lastName = names[names.length - 1];
      }
    }
  },
  methods: {
    logOut: function() {
      console.log("User Disconnected");
      // ToDo disconnexion function
    }
  },
  data() {
    return {
      fullName: "Thomas Maulon"
    };
  }
};
</script>

