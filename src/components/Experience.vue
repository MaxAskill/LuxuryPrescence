<template>
  <div class="w-full h-full bg-cover bg-center justify-center relative">
    <div class="w-full py-6 bg-white text-black text-center">
      <div class="grid gap-4 md:gap-8 max-w-6xl mx-auto">
        <!-- Card 1 -->
        <div
          class="flex flex-col items-center bg-white rounded-lg md:flex-row md:max-w-full dark:bg-gray-800"
        >
          <img
            class="object-cover w-full h-96 md:h-auto md:w-[45%] rounded-t-lg md:rounded-none md:rounded-l-lg"
            src="@/assets/resuccess.png"
            alt="Real Estate Success"
          />
          <div class="flex flex-col justify-between p-4 md:p-8 text-left">
            <h5 class="text-2xl font-bold text-gray-900 dark:text-white mb-2">
              Over 33 Years of Real Estate Success
            </h5>
            <p class="font-normal text-gray-700 dark:text-gray-400">
              We provide every one of our clients with a level of service they won’t find
              anywhere else. We give them what they need, often before they know they need
              it. In real estate, almost everything can be negotiated. When you choose
              Hansen Partners, experience is 100% nonnegotiable. And it’s an experience
              like no other.
            </p>
          </div>
        </div>

        <!-- Card 2 -->
        <div
          class="flex flex-col items-center bg-white rounded-lg md:flex-row md:max-w-full dark:bg-gray-800"
        >
          <div class="flex flex-col justify-between p-4 md:p-8 text-left">
            <h5 class="text-2xl font-bold text-gray-900 dark:text-white mb-2">
              We Want To Create An Unforgettable Experience For You...
            </h5>
            <p class="font-normal text-gray-700 dark:text-gray-400">
              We combine data gained from your home’s Comparative Market Analysis with
              local market research to create a marketing plan designed to help you meet
              your selling goals. Successfully marketing a home in today’s real estate
              environment requires a firm with experience and flexibility. Hansen Partners
              provides both.
            </p>
          </div>
          <img
            class="object-cover w-full h-96 md:h-auto md:w-[45%] rounded-t-lg md:rounded-none md:rounded-r-lg"
            src="@/assets/msummary.png"
            alt="Marketing Summary"
          />
        </div>

        <!-- Card 3 -->
        <div
          class="flex flex-col items-center bg-white rounded-lg md:flex-row md:max-w-full dark:bg-gray-800"
        >
          <img
            class="object-cover w-full h-96 md:h-auto md:w-[45%] rounded-t-lg md:rounded-none md:rounded-l-lg"
            src="@/assets/tablet.png"
            alt="Communications Tablet"
          />
          <div class="flex flex-col justify-between p-4 md:p-8 text-left">
            <h5 class="text-2xl font-bold text-gray-900 dark:text-white mb-2">
              The Hansen Partners Communications Tablet
            </h5>
            <p class="font-normal text-gray-700 dark:text-gray-400">
              We have created this as a wonderful tool so that we can communicate with you
              daily, providing updates on what is happening with your home. We are
              available with a click of your tablet.
            </p>
            <ul class="list-disc pl-5 space-y-1 text-gray-700 dark:text-gray-400">
              <li>Review all documents and sign at your convenience.</li>
              <li>Stay up-to-date on all marketing activities in real-time.</li>
              <li>Meet face-to-face using our Gotomeeting platform.</li>
              <li>Quickly send video messages for fast communication.</li>
            </ul>
          </div>
        </div>

        <!-- Card 4 -->
        <div
          class="flex flex-col items-center bg-white rounded-lg md:max-w-full dark:bg-gray-800 p-4 md:p-8"
        >
          <p class="font-normal text-gray-700 dark:text-gray-400">
            We believe that transparency and guiding you and your family through the
            process is key to a great experience. During uncertain times, it’s good to
            know you have someone with a proven track record you can count on. We’re here
            to handle your needs throughout the real estate process. Who you work with
            does matter!
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResponsiveRealEstateComponent",
};
</script>

<style scoped>
/* Additional custom styling if needed */
</style>
