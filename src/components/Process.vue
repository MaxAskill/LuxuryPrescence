<template>
  <div
    class="w-screen h-screen bg-cover bg-center flex flex-col justify-center relative mt-10"
  >
    <div
      class="absolute inset-0 bg-cover bg-center"
      style="
        background-image: url('/assets/meeting.png');
        filter: blur(8px);
        z-index: 0;
        background-color: rgba(31, 41, 55, 0.5);
        background-blend-mode: multiply;
      "
    ></div>
    <div class="relative z-10">
      <div class="grid grid-cols-2 gap-8 max-w-7xl mx-auto">
        <!-- Selling Process Section -->
        <div class="flex flex-col items-start">
          <h1 class="text-white text-6xl font-bold mb-6 drop-shadow-lg">
            Selling Process
          </h1>
          <ol class="relative border-l border-gray-200 dark:border-gray-700">
            <li class="mb-10 ms-6">
              <ProcessStep title="INITIAL CONSULTATION & PLANNING" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="DEVISE & EXECUTE MARKETING PLAN" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="REVIEW OFFERS & REACH AGREEMENT WITH BUYER" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="COMPLETE TRANSACTION PROCESS" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="AFTER-SALE SERVICE" />
            </li>
          </ol>
        </div>

        <!-- Buying Process Section -->
        <div class="flex flex-col items-center">
          <h1 class="text-white text-6xl font-bold mb-6 drop-shadow-lg">
            Buying Process
          </h1>
          <ol class="relative border-l border-gray-200 dark:border-gray-700">
            <li class="mb-10 ms-6">
              <ProcessStep title="INITIAL CONSULTATION & PLANNING" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="SEARCH FOR PROPERTIES & VISITS" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="ANALYZE & CHOOSE PROPERTIES" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="NEGOTIATE & PRESENT OFFERS" />
            </li>
            <li class="mb-10 ms-6">
              <ProcessStep title="COMPLETE TRANSACTION PROCESS" />
            </li>
          </ol>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProcessStep from "./ProcessStep.vue"; // Assuming you create a separate component

export default {
  components: {
    ProcessStep,
  },
};
</script>

<style scoped>
/* Add any scoped styles if necessary */
</style>
