<template>
  <div id="app" class="VddApp">
    <Aside class="VddApp_Aside"/>
    <div class="VddApp_Content">
      <HeaderComponent msg="WTF With Vue on CodeSandBox  🤘 !"/>
      <main class="VddApp_Main">
        <section id="dataTabAppSection" class="VddApp_Section">
          <TabWrapperComponent class="VddApp_DataTabComponent"/>
        </section>
      </main>
    </div>
    <footer class="VddApp_Footer"></footer>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import TabWrapperComponent from "./components/TabWrapperComponent.vue";
import Aside from "./components/Aside.vue";
import Logo from "./components/Logo.vue";
import { library } from "@fontawesome/fontawesome-svg-core";
import { faCoffee } from "@fontawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fontawesome/vue-fontawesome";

export default {
  name: "App",
  components: {
    HeaderComponent,
    TabWrapperComponent,
    Aside,
    Logo
  }
};
</script>
<style lang="scss">
@import "./variables.scss";

*,
*::before,
*::after {
  box-sizing: border-box;
}

#app {
  margin: 0 auto;
  line-height: 1.4;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $vue-blue;
}
main {
}

h1 {
  text-align: center;
}
</style>


