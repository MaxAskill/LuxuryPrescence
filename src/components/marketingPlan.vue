<template>
  <div class="w-full py-9 bg-white text-black text-center">
    <h1 class="text-black text-5xl font-bold mb-6 drop-shadow-lg">
      Comprehensive Marketing Plan
    </h1>
  </div>
  <div class="w-full py-6 bg-white text-black text-center">
    <div class="grid grid-cols-4 gap-12 max-w-5xl mx-auto">
      <div v-for="(card, index) in cards" :key="index" class="flex flex-col items-center">
        <a
          class="flex flex-col items-center w-64 h-80 p-6 bg-white border border-gray-200 rounded-lg shadow-lg hover:bg-gray-100 dark:bg-gray-800 dark:border-gray-700 dark:hover:bg-gray-700"
        >
          <img
            :src="card.icon"
            :alt="card.title"
            class="w-24 h-24 object-cover mx-auto"
          />
          <h5
            class="mt-4 mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white"
          >
            {{ card.title }}
          </h5>
          <p class="font-normal text-gray-700 dark:text-gray-400 text-center">
            {{ card.description }}
          </p>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import envelopeIcon from "@/assets/envelope.svg";
import syndication from "@/assets/syndication.svg";
import map from "@/assets/map.svg";
import photo from "@/assets/photo.svg";

export default {
  data() {
    return {
      cards: [
        {
          icon: envelopeIcon,
          title: "Responsive",
          description:
            "I am always available via phone, text, or email to answer your questions in a timely manner.",
        },
        {
          icon: syndication,
          title: "Syndication",
          description: "I market your property locally, nationally, and internationally",
        },
        {
          icon: map,
          title: "Virtual Tour",
          description: "Let's make your home stand out with a high quality virtual tour.",
        },
        {
          icon: photo,
          title: "Photography",
          description:
            "Beatiful, high-end photography is a central part of our marketing plan for your property.",
        },
      ],
    };
  },
};
</script>
