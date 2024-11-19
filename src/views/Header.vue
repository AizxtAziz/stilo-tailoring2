<template>
  <header class="bg-white text-black shadow-md sticky top-0 z-50">
    <div class="container mx-auto px-4 py-3">
      <div class="flex items-center justify-between">
        <!-- Logo (adjusted size) -->
        <div class="text-4xl font-bold">
          <span
            ><img src="../assets/logo.png" class="w-20 h-16" alt="Logo"
          /></span>
        </div>

        <!-- Navbar -->
        <nav class="hidden md:flex space-x-8">
          <a
            class="hover:text-gray-300 transition duration-300"
            :class="{ 'text-blue-400': isActive('home') }"
            @click.prevent="scrollToSection('home')"
            >Home</a
          >
          <a
            class="hover:text-gray-300 transition duration-300"
            :class="{ 'text-blue-400': isActive('about-us') }"
            @click.prevent="scrollToSection('about-us')"
            >About</a
          >
          <a
            class="hover:text-gray-300 transition duration-300"
            :class="{ 'text-blue-400': isActive('catalogue') }"
            @click.prevent="scrollToSection('catalogue')"
            >Catalogue</a
          >
          <a
            class="hover:text-gray-300 transition duration-300"
            :class="{ 'text-blue-400': isActive('contact') }"
            @click.prevent="scrollToSection('contact')"
            >Contact</a
          >
        </nav>

        <!-- Mobile Menu Button -->
        <div class="md:hidden">
          <button @click="toggleMenu" class="text-white">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              ></path>
            </svg>
          </button>
        </div>
      </div>

      <!-- Mobile Dropdown Menu -->
      <div v-if="isMenuOpen" class="md:hidden mt-4 space-y-4">
        <a
          @click="closeMenu"
          class="block text-white hover:text-gray-300"
          :class="{ 'text-blue-400': isActive('home') }"
          @click.prevent="scrollToSection('home')"
          >Home</a
        >
        <a
          @click="closeMenu"
          class="block text-white hover:text-gray-300"
          :class="{ 'text-blue-400': isActive('about-us') }"
          @click.prevent="scrollToSection('about-us')"
          >About</a
        >
        <a
          @click="closeMenu"
          class="block text-white hover:text-gray-300"
          :class="{ 'text-blue-400': isActive('catalogue') }"
          @click.prevent="scrollToSection('catalogue')"
          >Catalogue</a
        >
        <a
          @click="closeMenu"
          class="block text-white hover:text-gray-300"
          :class="{ 'text-blue-400': isActive('contact') }"
          @click.prevent="scrollToSection('contact')"
          >Contact</a
        >
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
      currentSection: "home", // Default section
    };
  },
  mounted() {
    // Add scroll event listener
    window.addEventListener("scroll", this.onScroll);
  },
  beforeDestroy() {
    // Remove scroll event listener to prevent memory leaks
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    },
    isActive(route) {
      return this.currentSection === route;
    },
    scrollToSection(sectionId) {
      const section = document.getElementById(sectionId);
      if (section) {
        // Update the URL hash
        window.location.hash = `#${sectionId}`;
        const navbarHeight = document.querySelector("header").offsetHeight;
        window.scrollTo({
          top: section.offsetTop - navbarHeight,
          behavior: "smooth",
        });
        // Update currentSection without modifying the URL
        this.currentSection = sectionId;
        this.closeMenu();

        // Optionally replace the URL state without appending the hash
        window.history.replaceState(null, null, "/main");
      }
    },
    onScroll() {
      const sections = document.querySelectorAll("section"); // Assuming each section is wrapped in a <section> tag
      const navbarHeight = document.querySelector("header").offsetHeight;
      let current = "";

      // Find the section currently in view
      sections.forEach((section) => {
        const sectionTop = section.offsetTop - navbarHeight;
        const sectionHeight = section.offsetHeight;
        if (
          window.scrollY >= sectionTop &&
          window.scrollY < sectionTop + sectionHeight
        ) {
          current = section.getAttribute("id");
        }
      });

      // Update the current section
      if (current) {
        this.currentSection = current;
      }
    },
  },
};
</script>


<style scoped>
/* Add custom styles for navigation links */
a {
  cursor: pointer; /* Ensures the pointer cursor is displayed */
}

/* Optional: Customize hover styles */
a:hover {
  text-decoration: none; /* Remove underline if any */
}

/* Add active link color */
.text-blue-400 {
  color: #60a5fa; /* Customize the active link color */
  font-weight: bold; /* Make the active link more prominent */
}
</style>

