<template>
  <section id="home" class="home-section bg-gradient-to-r from-purple-600 to-blue-500 py-16 px-6 md:px-12">
    <div class="container mx-auto text-center">
      <h1 class="text-white text-4xl sm:text-5xl font-extrabold leading-tight mb-6">
        Welcome to Your New Home
      </h1>
      <p class="text-white text-lg sm:text-xl mb-8">
        Discover the perfect place to call home, with modern amenities and sleek design.
      </p>
      <div class="cta-btns flex justify-center space-x-4">
        <button class="bg-white text-purple-600 hover:bg-purple-100 py-2 px-6 rounded-lg shadow-lg transition duration-300 transform hover:scale-105">
          Get Started
        </button>
        <button class="bg-transparent border-2 border-white text-white hover:bg-white hover:text-purple-600 py-2 px-6 rounded-lg shadow-lg transition duration-300 transform hover:scale-105">
          Learn More
        </button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HomeView',
};
</script>

<style scoped>
/* Custom Smart CSS for Home Section */
.home-section {
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

@media (min-width: 640px) {
  .home-section {
    padding-top: 8rem;
    padding-bottom: 8rem;
  }
}

@media (max-width: 639px) {
  .home-section {
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
}
</style>

