<template>
  <div
    class="w-full h-full bg-cover bg-white bg-center flex justify-center relative items-center bg-gray-100"
  >
    <div class="w-full py-6 bg-white text-black text-center">
      <h1 class="text-2xl font-bold mb-4">
        Leading Real Estate Companies of The World® & Luxury Portfolio International
      </h1>
      <div class="w-full max-w-3xl mx-auto space-y-4" id="accordion-collapse">
        <div v-for="(item, index) in items" :key="index">
          <!-- Accordion Header -->
          <h2 :id="`accordion-collapse-heading-${index}`">
            <button
              type="button"
              class="flex items-center justify-between w-full p-5 font-medium text-gray-500 border border-b-0 rounded-t-xl focus:ring-4 focus:ring-gray-200 hover:bg-gray-100 gap-3"
              @click="toggleItem(index)"
              :aria-expanded="activeIndex === index ? 'true' : 'false'"
              :aria-controls="`accordion-collapse-body-${index}`"
              tabindex="0"
            >
              <span>{{ item.title }}</span>
              <svg
                :class="{ 'rotate-180': activeIndex === index }"
                class="w-3 h-3 transition-transform"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 10 6"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 5 5 1 1 5"
                />
              </svg>
            </button>
          </h2>
          <!-- Accordion Content -->
          <div
            :id="`accordion-collapse-body-${index}`"
            :aria-labelledby="`accordion-collapse-heading-${index}`"
            v-show="activeIndex === index"
            class="p-5 border border-t-0 border-gray-200 bg-gray-50"
          >
            <!-- Text Content -->
            <p v-html="item.content" class="text-gray-600"></p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Accordion",
  props: {
    items: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      activeIndex: null,
    };
  },
  methods: {
    toggleItem(index) {
      this.activeIndex = this.activeIndex === index ? null : index;
    },
  },
};
</script>

<style scoped>
.rotate-180 {
  transform: rotate(180deg);
}
</style>
