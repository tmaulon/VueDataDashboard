<template>
  <div class="VddApp_Header_Date">
    <i class="fas fa-calendar-alt"></i>
    <p>{{ localeDate() }}</p>
  </div>
</template>
<script>
export default {
  name: "DateTime",
  methods: {
    localeDate: function() {
      var o = {
        weekday: "long",
        year: "numeric",
        month: "long",
        day: "numeric"
      };
      let d = new Date();
      let l = window.navigator.language;
      let res = d.toLocaleDateString(l, o);
      return res;
    }
  }
};
</script>
