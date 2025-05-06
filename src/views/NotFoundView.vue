<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section
    class="min-h-screen flex flex-col justify-center items-center bg-gradient-to-b from-gray-50 to-gray-100 p-4"
  >
    <div class="text-center max-w-2xl mx-auto">
      <!-- Animated 404 text -->
      <div class="relative">
        <h1 class="text-9xl font-bold text-gray-200 mb-4 animate-pulse">404</h1>
        <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">
          <i class="pi pi-exclamation-triangle text-yellow-400 text-7xl mb-4 animate-bounce"></i>
        </div>
      </div>

      <!-- Main message -->
      <h2 class="text-4xl font-bold text-gray-800 mb-4">Oops! Page Not Found</h2>
      <p class="text-xl text-gray-600 mb-8">
        The page you're looking for seems to have vanished into the digital void.
      </p>

      <!-- Action buttons -->
      <div class="flex flex-col sm:flex-row gap-4 justify-center">
        <RouterLink
          to="/"
          class="px-6 py-3 bg-green-600 hover:bg-green-700 text-white rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 flex items-center justify-center gap-2"
        >
          <i class="pi pi-home"></i>
          Back to Home
        </RouterLink>
        <button
          @click="$router.back()"
          class="px-6 py-3 bg-gray-200 hover:bg-gray-300 text-gray-800 rounded-lg shadow-lg hover:shadow-xl transition-all duration-300 transform hover:scale-105 flex items-center justify-center gap-2"
        >
          <i class="pi pi-arrow-left"></i>
          Go Back
        </button>
      </div>

      <!-- Fun message -->
      <p class="text-sm text-gray-500 mt-8">
        Don't worry, even the best explorers sometimes take wrong turns!
      </p>
    </div>
  </section>
</template>

<style scoped>
.animate-pulse {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.animate-bounce {
  animation: bounce 1s infinite;
}

@keyframes pulse {
  0%,
  100% {
    opacity: 1;
  }
  50% {
    opacity: 0.5;
  }
}

@keyframes bounce {
  0%,
  100% {
    transform: translateY(-25%);
    animation-timing-function: cubic-bezier(0.8, 0, 1, 1);
  }
  50% {
    transform: translateY(0);
    animation-timing-function: cubic-bezier(0, 0, 0.2, 1);
  }
}
</style>
