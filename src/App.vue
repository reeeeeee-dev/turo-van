<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import { KinesisContainer } from 'vue-kinesis'
</script>

<template>
  <Navbar />

  <kinesis-container event="scroll">
    <RouterView v-slot="{ Component }">
      <Transition name="fade" mode="out-of-view">
        <component :is="Component" />
      </Transition>
    </RouterView>
  </kinesis-container>
</template>
