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
      // link header

      headerMenuItems: [
        { text: "Home", subMenu: true },
        { text: "About", subMenu: true },
        { text: "Blog" },
        { text: "Contact" },
        { text: "Shop by Brand", subMenu: true }
      ],


      // prima sezione link footer

      footerMenuItems: [
        { titleShop: 'Shop by Brand' },
        { item: 'Bed' },
        { item: 'Food' },
        { item: 'Toys' },
        { item: 'Transport' },
      ],
      footerMenuItemsTwo: [
        // seconda sezione link footer
        { titleUseful: 'Useful links' },
        { linkUseful: 'My account' },
        { linkUseful: 'Orders' },
        { linkUseful: 'Checkout' },
        { linkUseful: 'Cart' },
      ],
      footerMenuItemsThree: [
        // ultimi links per footer
        { lastLinks: 'Home' },
        { lastLinks: 'About' },
        { lastLinks: 'Blog' },
        { lastLinks: 'Contact' },
        { lastLinks: 'Shop' }
      ]
    }
  }
}
</script>

<template>
  <div>
    <AppHeader :menuItems="headerMenuItems" />
    <AppMain />
    <AppFooter :menuItems="footerMenuItems" :menuItemsTwo="footerMenuItemsTwo" :menuItemsThree="footerMenuItemsThree" />
  </div>
</template>

<style lang="scss">
@import './styles/main.scss';
</style>
