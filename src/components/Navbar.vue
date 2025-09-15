<template>
  <nav
    class="fixed w-[calc(100%-64px)] rounded-xl flex justify-between items-center top-8 left-8 right-8 m-8 z-50 shadow-lg p-4 backdrop-blur-lg bg-green-smoke-100/80 text-green-smoke-950"
  >
    <div class="flex items-center text-center gap-8">
      <RouterLink to="/">
        <span>Home</span>
      </RouterLink>
      <RouterLink to="/vehicles">
        <span>Vehicles</span>
      </RouterLink>
      <RouterLink to="/about">
        <span>About</span>
      </RouterLink>
    </div>
    <RouterLink to="/" class="pr-20">
      <img src="@/assets/logo.svg" alt="Logo" class="h-8 w-8" />
    </RouterLink>
    <a
      href="https://turo.com"
      target="_blank"
      class="flex justify-self-end items-center gap-2 bg-green-smoke-950 text-green-smoke-50 px-4 py-2 rounded-md hover:bg-green-smoke-50 hover:text-green-smoke-950 transition-colors"
    >
      <span>Rent Now </span> <ExternalLinkIcon size="16" />
    </a>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { ExternalLinkIcon } from 'lucide-vue-next'

const isMobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}

const closeMobileMenu = () => {
  isMobileMenuOpen.value = false
}
</script>
