<template>
  <section id="about-us" class="about-section py-16 px-6 md:px-12">
    <div class="container mx-auto flex flex-col md:flex-row items-center space-y-8 md:space-y-0 md:space-x-12">
      <!-- Text Section -->
      <div class="text-section flex-1">
        <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-800 mb-4">
          About Us
        </h2>
        <p class="text-lg sm:text-xl text-gray-600 mb-6">
          We are a passionate team committed to providing innovative solutions that transform the way people live and work.
          Our goal is to create a lasting impact on the communities we serve with exceptional products and services.
        </p>
        <div class="cta-btns flex space-x-4">
          <button class="bg-blue-500 text-white hover:bg-blue-600 py-2 px-6 rounded-lg shadow-lg transition duration-300 transform hover:scale-105">
            Contact Us
          </button>
          <button class="bg-transparent border-2 border-gray-800 text-gray-800 hover:bg-gray-800 hover:text-white py-2 px-6 rounded-lg shadow-lg transition duration-300 transform hover:scale-105">
            Learn More
          </button>
        </div>
      </div>

      <!-- Image Section -->
      <div class="image-section flex-1">
        <img src="https://via.placeholder.com/600x400" alt="About Us" class="w-full h-auto rounded-lg shadow-xl object-cover"/>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
};
</script>

<style scoped>
/* Smart CSS for About Section */
.about-section {
  background-color: #f9f9f9;
}

@media (min-width: 768px) {
  .about-section {
    padding-top: 8rem;
    padding-bottom: 8rem;
  }
}

@media (max-width: 767px) {
  .about-section {
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
}
</style>
