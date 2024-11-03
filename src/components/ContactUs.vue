<template>
  <div
    class="mx-auto w-screen h-screen bg-cover bg-center bg-white flex flex-col items-center"
    style="background-image: url('../../src/assets/bed.png')"
  >
    <h1 class="text-white text-5xl font-bold mb-6 drop-shadow-lg pt-[10%]">
      Work With Us
    </h1>
    <p class="block mb-3 px-4 max-w-lg font-normal text-black dark:text-white mx-auto">
      With decades of experience in luxurious Tri Valley real estate, our team is here to
      ensure that your dreams are a reality. Let us guide you through your home buying
      journey, contact us today!
    </p>

    <!-- Modal toggle -->
    <button
      @click="openModal"
      class="block text-white hover:text-black border border-white hover:bg-white focus:ring-4 focus:outline-none focus:ring-black font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-white dark:text-white dark:hover:text-white dark:hover:bg-black dark:focus:ring-black"
      type="button"
    >
      Contact Us
    </button>

    <!-- Main modal -->
    <div
      v-if="isModalOpen"
      id="authentication-modal"
      tabindex="-1"
      aria-hidden="true"
      role="dialog"
      class="fixed top-0 right-0 left-0 z-50 flex justify-center items-center w-full h-full bg-black bg-opacity-50"
    >
      <div class="relative p-4 w-full max-w-2xl max-h-[90vh] overflow-y-auto">
        <!-- Modal content -->
        <div class="relative bg-white rounded-lg shadow dark:bg-gray-700">
          <!-- Modal header -->
          <div
            class="flex items-center justify-between p-4 md:p-5 border-b rounded-t dark:border-gray-600"
          >
            <h3 class="text-xl font-semibold text-gray-900 dark:text-white">
              Contact Us
            </h3>
            <button
              type="button"
              @click="closeModal"
              class="end-2.5 text-gray-400 bg-transparent hover:bg-gray-200 hover:text-gray-900 rounded-lg text-sm w-8 h-8 ms-auto inline-flex justify-center items-center dark:hover:bg-gray-600 dark:hover:text-white"
            >
              <svg
                class="w-3 h-3"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 14 14"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"
                />
              </svg>
              <span class="sr-only">Close modal</span>
            </button>
          </div>
          <!-- Modal body -->
          <div class="p-4 md:p-5">
            <form @submit.prevent="submitForm" class="space-y-4">
              <div>
                <label
                  for="name"
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
                  >Your Name</label
                >
                <input
                  type="text"
                  v-model="form.name"
                  id="name"
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
                  placeholder="Name"
                  required
                />
              </div>
              <div>
                <label
                  for="number"
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
                  >Your Phone Number</label
                >
                <input
                  type="text"
                  v-model="form.number"
                  id="number"
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
                  placeholder="(925) 553-6707"
                  required
                />
              </div>
              <div>
                <label
                  for="email"
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
                  >Your Email</label
                >
                <input
                  type="email"
                  v-model="form.email"
                  id="email"
                  class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
                  placeholder="name@company.com"
                  required
                />
              </div>
              <div>
                <label
                  for="message"
                  class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
                  >Your Message</label
                >
                <textarea
                  id="message"
                  rows="4"
                  v-model="form.message"
                  class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
                  placeholder="Your message..."
                  required
                ></textarea>
              </div>

              <div class="flex justify-between">
                <div class="flex items-start">
                  <div class="flex items-center h-5">
                    <input
                      id="remember"
                      type="checkbox"
                      v-model="form.remember"
                      class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 dark:bg-gray-600 dark:border-gray-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800"
                    />
                  </div>
                  <label
                    for="remember"
                    class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
                  >
                    By providing Julie Hansen Partnership your contact information, you
                    acknowledge and agree to our Privacy Policy and consent to receiving
                    marketing communications, including through automated calls, texts,
                    and emails, some of which may use artificial or prerecorded voices.
                    This consent isn’t necessary for purchasing any products or services
                    and you may opt out at any time. To opt out from texts, you can reply,
                    ‘stop’ at any time. To opt out from emails, you can click on the
                    unsubscribe link in the emails. Message and data rates may apply.
                  </label>
                </div>
              </div>
              <button
                type="submit"
                class="w-full text-gray-900 hover:text-white border border-gray-800 hover:bg-gray-900 focus:ring-4 focus:outline-none focus:ring-gray-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center me-2 mb-2 dark:border-gray-600 dark:text-gray-400 dark:hover:text-white dark:hover:bg-gray-600 dark:focus:ring-gray-800"
              >
                Submit
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false,
      form: {
        name: "",
        number: "",
        email: "",
        message: "",
        remember: false,
      },
    };
  },
  methods: {
    openModal() {
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
    },
    submitForm() {
      // Handle form submission logic here
      console.log("Form submitted:", this.form);
      this.closeModal(); // Close the modal after submission
      // Here you can add further logic, e.g., API calls to handle the form submission
    },
  },
};
</script>

<style scoped>
/* Add any additional styles if needed */
</style>
