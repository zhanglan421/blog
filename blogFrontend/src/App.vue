<template>
  <vue-particles id="tsparticles" :options="tsparticlesConfig" />

  <starBackground />

  <RouterView />
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'

import starBackground from '@/components/starBackground/index.vue'

import {tsparticlesConfig} from '@/config/tsparticles.config'
</script>

<style lang="scss"></style>
