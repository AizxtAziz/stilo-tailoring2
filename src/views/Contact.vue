<template>
  <section id="contact" class="contact-section py-16 px-6 md:px-12 bg-gray-50">
    <div class="container mx-auto text-center mb-12">
      <h2 class="text-3xl sm:text-4xl font-extrabold text-gray-800 mb-6">
        Contact Us
      </h2>
      <p class="text-lg sm:text-xl text-gray-600">
        Have any questions or need assistance? Reach out to us, and we will get back to you as soon as possible!
      </p>
    </div>

    <!-- Contact Section Layout: Form and Branch Location -->
    <div class="flex flex-col md:flex-row items-center md:items-start justify-center gap-12">
      
      <!-- Contact Form -->
      <div class="contact-form bg-white p-8 rounded-lg shadow-lg w-full md:w-1/2">
        <form @submit.prevent="handleSubmit">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
            <!-- Name Field -->
            <div>
              <label for="name" class="block text-gray-700 text-sm font-medium mb-2">Your Name</label>
              <input v-model="form.name" type="text" id="name" class="w-full p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500" required />
            </div>

            <!-- Email Field -->
            <div>
              <label for="email" class="block text-gray-700 text-sm font-medium mb-2">Your Email</label>
              <input v-model="form.email" type="email" id="email" class="w-full p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500" required />
            </div>
          </div>

          <!-- Message Field -->
          <div class="mt-6">
            <label for="message" class="block text-gray-700 text-sm font-medium mb-2">Your Message</label>
            <textarea v-model="form.message" id="message" rows="5" class="w-full p-3 border border-gray-300 rounded-lg shadow-sm focus:outline-none focus:ring-2 focus:ring-blue-500" required></textarea>
          </div>

          <!-- Submit Button -->
          <div class="mt-6 flex justify-center">
            <button type="submit" class="bg-blue-500 text-white hover:bg-blue-600 py-3 px-8 rounded-lg shadow-md transition duration-300 transform hover:scale-105">
              Send Message
            </button>
          </div>
        </form>
      </div>

      <!-- Branch Location Information -->
      <div class="branch-info text-center md:text-left w-full md:w-1/2">
        <h3 class="text-xl font-semibold text-gray-800 mb-4">Our Branch Location</h3>
        <p class="text-lg text-gray-600">
          1234 Main Street, Suite 567 <br />
          Cityville, ST 12345 <br />
          <a href="mailto:info@company.com" class="text-blue-500 hover:underline">info@company.com</a>
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    };
  },
  methods: {
    handleSubmit() {
      // Here, you would usually send the form data to an API or email service
      alert(`Message sent successfully!
      Name: ${this.form.name}
      Email: ${this.form.email}
      Message: ${this.form.message}`);
      // Reset the form fields
      this.form.name = '';
      this.form.email = '';
      this.form.message = '';
    }
  }
};
</script>

<style scoped>
/* Smart CSS for Contact Section */
.contact-section {
  background-color: #f9f9f9;
}

@media (min-width: 768px) {
  .contact-section {
    padding-top: 8rem;
    padding-bottom: 8rem;
  }
}

@media (max-width: 767px) {
  .contact-section {
    padding-top: 4rem;
    padding-bottom: 4rem;
  }
}
</style>
