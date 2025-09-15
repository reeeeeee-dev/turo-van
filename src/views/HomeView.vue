<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const parallaxContainer = ref(null)
const parallaxImage = ref(null)

const handleScroll = () => {
  if (parallaxImage.value) {
    const scrolled = window.pageYOffset
    const rate = scrolled * -0.5 // Adjust this value to control parallax speed
    parallaxImage.value.style.transform = `translateY(${rate}px)`
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <div class="bg-green-smoke-50 min-h-screen h-[5000px]">
    <div ref="parallaxContainer" class="relative h-screen overflow-hidden">
      <!-- Parallax background image -->
      <div class="absolute inset-0">
        <img
          ref="parallaxImage"
          src="@/assets/cars.jpg"
          alt="Van Hero"
          class="w-full h-screen object-cover"
        />
      </div>

      <!-- Overlay -->
      <div class="absolute inset-0">
        <!-- Content -->
        <div class="h-full flex items-center justify-center">
          <div class="text-center gap-4 flex flex-col items-center">
            <h1 class="text-green-smoke-50 text-4xl font-bold md:text-5xl lg:text-6xl">
              Luxury transportation rentals
            </h1>
            <div class="text-green-smoke-300 text-lg">
              The best way to explore Northwest Arkansas and beyond
            </div>
            <button
              class="bg-green-smoke-50 text-green-smoke-950 px-4 py-2 w-max rounded-md text-xl"
            >
              Rent Now
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Ensure smooth parallax movement */
img {
  will-change: transform;
  transform: translateY(0);
}
</style>
