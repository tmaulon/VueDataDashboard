<template>
  <div id="app" class="VddApp">
    <UserConnexion/>
    <Aside class="VddApp_Aside"/>
    <HeaderComponent class="VddApp_Header" :appTitle="appTitle"/>
    <main class="VddApp_Main">
      <section id="dataTabAppSection" class="VddApp_Section">
        <TabWrapperComponent class="VddApp_DataTabComponent"/>
      </section>
    </main>
    <footer class="VddApp_Footer"></footer>
  </div>
</template>

<script>
import UserConnexion from "./components/UserConnexion.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import TabWrapperComponent from "./components/TabWrapperComponent.vue";
import Aside from "./components/Aside.vue";
import Logo from "./components/Logo.vue";

export default {
  name: "App",
  components: {
    UserConnexion,
    HeaderComponent,
    TabWrapperComponent,
    Aside,
    Logo
  },
  data() {
    return {
      appTitle: "Incidents Database"
    };
  }
};
</script>
<style lang="scss">
@import "./_variables.scss";
@import "./_animations.scss";
*,
*::before,
*::after {
  box-sizing: border-box;
}
body {
  margin: 0;
}
input,
button {
  -webkit-appearance: none;
  border: none;
  background: none;
  color: #000;
  text-decoration: none;
  cursor: pointer;
}
li {
  list-style-type: none;
}
a,
a:hover,
a:focus,
a:active {
  text-decoration: none;
  color: inherit;
}
.VddApp {
  margin: 0 auto;
  line-height: 1.4;
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $dark;
  display: grid;
  width: 100%;
  height: 100vh;
  grid-template-areas:
    "head head"
    "aside  main"
    "aside  foot";
  grid-template-rows: 100px 1fr 30px;
  grid-template-columns: 100px 1fr;

  &_NavBar {
    &_List {
      list-style-type: none;
      margin: 0;
      padding: 0;
      display: flex;
      flex-direction: column;
      align-items: center;

      &_Item {
        $ni: &;

        width: 100%;

        &:last-child {
          & #{$ni}_Link {
            border-bottom-color: $vue-green;
          }
        }

        &_Link {
          $nil: &;

          display: flex;
          align-items: center;
          justify-content: center;
          position: relative;
          padding: 26px 0;
          text-decoration: none;
          font-size: 1.2rem;
          color: $light;
          border: 2px solid transparent;
          border-top-color: $vue-green;
          background-color: $fire-blue;
          transition: all 0.3s $easeOutBack;

          &:hover {
            &,
            & #{$nil}_Label {
              background-color: $vue-green;
              color: $light;
            }

            #{$nil}_Label {
              @include fadeInFrom(left);
            }
          }

          &_Icon {
            font-size: 2rem;
          }

          &_Label {
            background-color: $fire-blue;
            position: absolute;
            left: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            width: auto;
            padding-right: 20px;
            opacity: 0;
            transform: translateX(-100%);
          }
        }
      }
    }
  }

  &_Logo {
    height: auto;
    display: block;
    margin: 0 auto;
    width: 100%;

    &_Wrapper {
      display: block;
      width: auto;
      max-height: 100px;
      max-width: 50px;
      margin-right: 30px;
    }
  }

  &_Aside {
    grid-area: aside;
    display: flex;
    flex-direction: column;
    width: auto;
    height: 100%;
    margin: 0;
    transform: scaleX(1);
    background-color: $fire-blue;
  }

  &_Header {
    grid-area: head;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    background-color: $fire-blue;
    color: $light;
    padding: 0 30px;

    &_Title {
      flex: 1 1 75%;
      text-align: left;
    }

    &_Date {
      text-transform: capitalize;
      display: flex;
      align-items: center;
      font-size: 0.8rem;
      font-weight: 600;
      margin-right: 20px;

      & > i {
        margin-right: 10px;
        font-size: 2rem;
      }
    }

    &_UserLogBtn {
      position: relative;
      display: flex;
      align-items: center;
      box-shadow: 0px 0px 5px 2px rgba(0, 0, 0, 0.14);
      padding: 10px 20px;
      font-size: 0.8rem;
      font-weight: 600;
      background: $light;
      color: $fire-blue;
      transform: scale(1);
      transition: all 0.6s $easeOutBack;

      &::before,
      &::after {
        content: "";
        display: block;
        position: absolute;
        width: 100%;
        height: 100%;
        border: 2px solid $vue-green;
        transform: scale(0);
        transition: all 0.6s ease-in-out;
      }

      &::before {
        top: 0;
        left: 0;
        transform-origin: top left;
        border-bottom-color: transparent;
        border-right-color: transparent;
      }

      &::after {
        bottom: 0;
        right: 0;
        transform-origin: bottom right;
        border-top-color: transparent;
        border-left-color: transparent;
      }

      &:hover {
        transform: scale(1.1);

        &::before,
        &::after {
          opacity: 1;
          transform: scale(1);
        }
      }

      & > i {
        font-size: 1.2rem;
        margin-right: 10px;
      }
    }
  }

  &_Main {
    grid-area: main;
  }

  &_Footer {
    grid-area: foot;
  }
}

h1 {
  text-align: center;
}
</style>


