<template>
  <div>
    <!-- Navbar with active class binding -->
    <Header :activeMenu="activeMenu" @setActiveMenu="setActiveMenu" />
    <HomeView />
    <About />
    <Catalogue />
    <Contact />
    <Footer />
  </div>
</template>

<script>
import Header from './Header.vue';
import HomeView from './HomeView.vue';
import About from './About.vue';
import Catalogue from './Catalogue.vue';
import Contact from './Contact.vue';
import Footer from './Footer.vue';

export default {
  name: 'Main',
  components: {
    Header,
    HomeView,
    About,
    Catalogue,
    Contact,
    Footer
  },
  data() {
    return {
      activeMenu: ''  // Track the active menu item
    };
  },
  methods: {
    setActiveMenu(menu) {
      this.activeMenu = menu;  // Update active menu item
    }
  }
};
</script>
