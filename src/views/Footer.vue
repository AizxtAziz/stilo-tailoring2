<template>
  <footer class="bg-gray-800 text-white py-8">
    <div class="container mx-auto px-6 md:px-12">
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- About Section -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold mb-4">About Us</h4>
          <p class="text-gray-400">
            We are a company that provides excellent services to help you with all your needs. Learn more about us and how we can assist you in achieving your goals.
          </p>
        </div>

        <!-- Quick Links -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
          <ul>
            <li><a href="/about" class="text-gray-400 hover:text-white">About Us</a></li>
            <li><a href="/privacy" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
            <li><a href="/terms" class="text-gray-400 hover:text-white">Terms of Service</a></li>
            <li><a href="/contact" class="text-gray-400 hover:text-white">Contact</a></li>
          </ul>
        </div>

        <!-- Social Media Links -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold mb-4">Follow Us</h4>
          <div class="flex space-x-4">
            <a href="https://facebook.com" target="_blank" class="text-gray-400 hover:text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path d="M12 2C6.48 2 2 6.48 2 12c0 4.99 3.65 9.13 8.44 9.88V15h-2.5v-3h2.5v-2.25c0-2.4 1.47-3.75 3.7-3.75 1.08 0 2.17.08 2.47.12v2.87h-1.5c-1.17 0-1.42.56-1.42 1.43V12h3l-1.12 3h-1.88v6.88C18.35 21.13 22 16.99 22 12c0-5.52-4.48-10-10-10z"/>
              </svg>
            </a>
            <a href="https://twitter.com" target="_blank" class="text-gray-400 hover:text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path d="M23 3a10.93 10.93 0 0 1-3.1.86A5.44 5.44 0 0 0 22.4 1.2a10.81 10.81 0 0 1-3.42 1.31A5.42 5.42 0 0 0 16.5 4.7a5.42 5.42 0 0 0-9.1 4.92C7.03 9.04 4.7 7.29 3 4.3a5.42 5.42 0 0 0-.7 2.72A5.42 5.42 0 0 0 5.1 10.7a5.37 5.37 0 0 1-2.4-.66v.06a5.42 5.42 0 0 0 4.34 5.3 5.44 5.44 0 0 1-2.4.09c.68 2.12 2.67 3.66 5.02 3.7a10.91 10.91 0 0 1-6.77 2.33C6.29 20.46 11 23 16.5 23c9.94 0 15.5-8.14 15.5-15.5v-.71A10.83 10.83 0 0 0 23 3z"/>
              </svg>
            </a>
            <a href="https://instagram.com" target="_blank" class="text-gray-400 hover:text-white">
              <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                <path d="M12 2.16c3.25 0 3.64.01 4.91.07 1.16.06 2.01.22 2.68.49a5.1 5.1 0 0 1 1.87 1.87c.27.67.43 1.51.49 2.68.06 1.27.07 1.66.07 4.91 0 3.25-.01 3.64-.07 4.91-.06 1.16-.22 2.01-.49 2.68a5.1 5.1 0 0 1-1.87 1.87c-.67.27-1.51.43-2.68.49-1.27.06-1.66.07-4.91.07-3.25 0-3.64-.01-4.91-.07-1.16-.06-2.01-.22-2.68-.49a5.1 5.1 0 0 1-1.87-1.87c-.27-.67-.43-1.51-.49-2.68-.06-1.27-.07-1.66-.07-4.91 0-3.25.01-3.64.07-4.91.06-1.16.22-2.01.49-2.68a5.1 5.1 0 0 1 1.87-1.87c.67-.27 1.51-.43 2.68-.49 1.27-.06 1.66-.07 4.91-.07zM12 0C8.74 0 8.32.01 7.04.07a5.82 5.82 0 0 0-3.06.75A7.14 7.14 0 0 0 .75 5.98a5.82 5.82 0 0 0-.75 3.06C.01 8.32 0 8.74 0 12c0 3.26.01 3.68.07 4.96.06 1.16.22 2.01.49 2.68a5.1 5.1 0 0 0 1.87 1.87c.67.27 1.51.43 2.68.49 1.28.06 1.66.07 4.91.07s3.63-.01 4.91-.07c1.16-.06 2.01-.22 2.68-.49a5.1 5.1 0 0 0 1.87-1.87c.27-.67.43-1.51.49-2.68.06-1.28.07-1.7.07-4.96 0-3.26-.01-3.68-.07-4.96-.06-1.17-.22-2.01-.49-2.68a5.1 5.1 0 0 0-1.87-1.87c-.67-.27-1.51-.43-2.68-.49C15.63.01 15.26 0 12 0z"/>
              </svg>
            </a>
          </div>
        </div>

        <!-- Newsletter Section -->
        <div class="footer-section">
          <h4 class="text-lg font-semibold mb-4">Subscribe to Our Newsletter</h4>
          <form @submit.prevent="subscribeToNewsletter">
            <input v-model="email" type="email" placeholder="Your email address" class="w-full p-3 mb-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500" required />
            <button type="submit" class="w-full bg-blue-500 text-white py-3 rounded-lg hover:bg-blue-600 focus:ring-2 focus:ring-blue-500">Subscribe</button>
          </form>
        </div>
      </div>

      <!-- Footer Bottom -->
      <div class="mt-8 text-center text-sm text-gray-400">
        <p>&copy; 2024 Your Company. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      email: ""
    };
  },
  methods: {
    subscribeToNewsletter() {
      alert(`Subscribed with: ${this.email}`);
      this.email = ""; // Reset the input field
    }
  }
};
</script>

<style scoped>
/* Additional custom styles for the footer if needed */
</style>
