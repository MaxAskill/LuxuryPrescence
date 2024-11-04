<script>
import Navbar from "./Navbar.vue";
import marketingPlan from "./marketingPlan.vue";
import Process from "./Process.vue";
import Experience from "./Experience.vue";
import MarketingStrategy from "./MarketingStrategy.vue";
import About from "./About.vue";
import ContactUs from "./ContactUs.vue";
import Footer from "./Footer.vue";

export default {
  components: {
    Navbar,
    marketingPlan,
    Process,
    Experience,
    MarketingStrategy,
    About,
    ContactUs,
    Footer,
  },
  data() {
    return {
      accordionItems: [
        {
          title: "What is JRockcliff's affiliation with Luxury Portfolio International?",
          content:
            "JRockcliff is a founding member of Luxury Portfolio International®, the luxury division of Leading Real Estate Companies of the World®. With more than 500 member firms around the world, our luxury listings are exposed to a vast global audience and reach potential buyers and investors in over 50 countries.",
        },
        {
          title: "What is Who’s Who in Luxury Real Estate?",
          content:
            "Who’s Who in Luxury Real Estate is a global collection of luxury real estate brokers.",
        },
        {
          title: "How does JRockcliff leverage international affiliations?",
          content:
            "Through our international affiliations, we have a strong presence in over 50 countries. Our luxury listings are sent to prominent international real estate sites, reaching over 70 million potential buyers and investors worldwide through our relationships with various partners.",
        },
        {
          title: "What markets do you serve in China?",
          content:
            "We have several well-positioned affiliate offices in China, providing our clients with access to buyers in Hong Kong, Shanghai, and Beijing.",
        },
        {
          title: "How does your international presence benefit clients?",
          content:
            "Through our international affiliations, we have a strong presence in over 50 countries. Our luxury listings are sent to prominent international real estate sites, reaching over 70 million potential buyers and investors worldwide.",
        },
      ],
    };
  },
};
</script>

<template>
  <Navbar />
  <div
    class="w-screen h-screen bg-cover bg-center bg-white flex flex-col items-center"
    style="background-image: url('/assets/moderninteriordesign.jpg')"
  >
    <h1
      class="text-white text-4xl md:text-5xl font-bold mb-6 drop-shadow-lg pt-32 md:pt-64"
    >
      Services
    </h1>

    <form class="max-w-sm md:max-w-md mx-auto w-full px-4 md:px-0">
      <label
        for="default-search"
        class="mb-2 text-sm font-medium text-gray-900 sr-only dark:text-white"
      >
        Search
      </label>
      <div class="relative w-full">
        <div
          class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none"
        ></div>
        <input
          type="search"
          id="default-search"
          class="block w-full p-3 md:p-4 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg bg-gray-5 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          placeholder="Search by Address or Area"
          required
        />
        <button
          type="submit"
          class="text-white absolute end-2.5 bottom-2.5 bg-white hover:bg-white focus:ring-4 focus:outline-none focus:ring-white font-medium rounded-lg text-sm px-3 py-2 md:px-4 md:py-2 dark:bg-white dark:hover:bg-white dark:focus:ring-white"
        >
          <p class="text-gray-800">Search</p>
        </button>
      </div>
    </form>
  </div>

  <marketingPlan />
  <Process />
  <Experience />
  <MarketingStrategy />

  <div class="w-full md:w-3/4 lg:w-1/2 items-center px-4 md:px-0 mx-auto">
    <About :items="accordionItems" />
  </div>
  <ContactUs />
  <Footer />
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@500;700&display=swap");

h1,
h5 {
  font-family: "Poppins", sans-serif;
  font-weight: 700; /* Bold */
}

h3 {
  font-family: "Poppins", sans-serif;
  font-weight: 500; /* Medium */
}

p,
.list {
  font-family: "Poppins", sans-serif;
  font-weight: 500; /* Medium */
}

@media (max-width: 720px) {
  h1 {
    font-size: 2.5rem;
  }
  form {
    padding: 0 16px;
  }
  .bg-image {
    background-size: cover;
  }
}

@media (min-width: 1080px) {
  h1 {
    font-size: 3rem;
  }
  form {
    max-width: 640px;
  }
}
</style>
