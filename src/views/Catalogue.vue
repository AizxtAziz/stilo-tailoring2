<template>
  <section id="catalogue" class="catalogue-section py-16 px-6 md:px-12 bg-gray-50">
    <div class="container mx-auto text-center mb-12">
      <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-800 mb-6">
        Our Catalogue
      </h2>
      <p class="text-lg sm:text-xl text-gray-600">
        Explore our curated selection of products and services. Find what suits you best!
      </p>
    </div>

    <!-- Catalogue Grid -->
    <div class="catalogue-grid grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-8">
      <div class="catalogue-item bg-white rounded-lg shadow-lg overflow-hidden">
        <img src="https://via.placeholder.com/400x300" alt="Product 1" class="w-full h-48 object-cover"/>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800 mb-2">Product 1</h3>
          <p class="text-gray-600 mb-4">
            A brief description of the product goes here. It's a high-quality product designed for your needs.
          </p>
          <button class="bg-blue-500 text-white hover:bg-blue-600 py-2 px-6 rounded-lg shadow-md transition duration-300 transform hover:scale-105">
            View More
          </button>
        </div>
      </div>

      <div class="catalogue-item bg-white rounded-lg shadow-lg overflow-hidden">
        <img src="https://via.placeholder.com/400x300" alt="Product 2" class="w-full h-48 object-cover"/>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800 mb-2">Product 2</h3>
          <p class="text-gray-600 mb-4">
            This is another great product. It's built with the latest technology and offers amazing performance.
          </p>
          <button class="bg-blue-500 text-white hover:bg-blue-600 py-2 px-6 rounded-lg shadow-md transition duration-300 transform hover:scale-105">
            View More
          </button>
        </div>
      </div>

      <div class="catalogue-item bg-white rounded-lg shadow-lg overflow-hidden">
        <img src="https://via.placeholder.com/400x300" alt="Product 3" class="w-full h-48 object-cover"/>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800 mb-2">Product 3</h3>
          <p class="text-gray-600 mb-4">
            A premium product designed with attention to detail. Perfect for everyday use or special occasions.
          </p>
          <button class="bg-blue-500 text-white hover:bg-blue-600 py-2 px-6 rounded-lg shadow-md transition duration-300 transform hover:scale-105">
            View More
          </button>
        </div>
      </div>

      <!-- Add more items as needed -->
      <!-- Example of dynamic items: -->
      <div v-for="item in catalogueItems" :key="item.id" class="catalogue-item bg-white rounded-lg shadow-lg overflow-hidden">
        <img :src="item.image" :alt="item.title" class="w-full h-48 object-cover"/>
        <div class="p-6">
          <h3 class="text-xl font-semibold text-gray-800 mb-2">{{ item.title }}</h3>
          <p class="text-gray-600 mb-4">{{ item.description }}</p>
          <button class="bg-blue-500 text-white hover:bg-blue-600 py-2 px-6 rounded-lg shadow-md transition duration-300 transform hover:scale-105">
            View More
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CatalogueSection',
  data() {
    return {
      // Example static data
      catalogueItems: [
        {
          id: 1,
          title: 'Product 4',
          description: 'This product is a blend of high-tech innovation and sleek design.',
          image: 'https://via.placeholder.com/400x300',
        },
        {
          id: 2,
          title: 'Product 5',
          description: 'An amazing product for those who value quality and functionality.',
          image: 'https://via.placeholder.com/400x300',
        },
        {
          id: 3,
          title: 'Product 6',
          description: 'Perfect for all your needs, combining elegance with power.',
          image: 'https://via.placeholder.com/400x300',
        },
        // Add more items as needed
      ]
    }
  }
};
</script>

<style scoped>
/* Smart CSS for Catalogue Section */
.catalogue-section {
  background-color: #658ac2;
}

.catalogue-item img {
  transition: transform 0.3s ease;
}

.catalogue-item:hover img {
  transform: scale(1.05);
}

@media (min-width: 768px) {
  .catalogue-section {
    padding-top: 8rem;
    padding-bottom: 8rem;
  }
}

@media (max-width: 767px) {
  .catalogue-section {
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
}
</style>
