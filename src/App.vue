<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import { KinesisContainer } from 'vue-kinesis'
</script>

<template>
  <header>
    <Navbar />
  </header>

  <kinesis-container event="scroll">
    <RouterView />
  </kinesis-container>
</template>
