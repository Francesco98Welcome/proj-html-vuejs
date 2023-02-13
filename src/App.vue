<script>
//import { store } from './store.js';
import AppHeader from './components/Header/AppHeader.vue';
import AppMain from './components/Main/AppMain.vue';
import AppFooter from './components/Footer/AppFooter.vue';
//import Introduction from './components/Header/Introduction.vue';


export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter,

  },
  data() {
    return {
      headerMenuItems: [
        { text: "Home" },
        { text: "About" },
        { text: "Blog" },
        { text: "Contact" },
        { text: "Shop by Brand" }
      ],
      /*footerMenuItems: [
        { text: "icon" },
        { text: "icon" },
        { text: "Support" }
      ]*/
    }
  }
}
</script>

<template>
  <div>
    <AppHeader :menuItems="headerMenuItems" />
    <AppMain />
    <!--<AppFooter :menuItems="footerMenuItems" />-->
  </div>
</template>

<style lang="scss">
@import './styles/main.scss';
</style>
