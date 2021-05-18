<template>
  <header>
    Welcome to Vue 3 Scoreboard!

    <button @click="handleToggle" :aria-pressed="String(isMenuOpen)">
      Menu {{ String(isMenuOpen) }}
    </button>

    <Menu :isMenuOpen="isMenuOpen" />
  </header>
</template>

<script lang="ts" setup>
import Menu from './Menu.vue'
import { inject, defineEmit } from 'vue'

const emit = defineEmit(['toggleIsMenuOpen'])
const isMenuOpen = inject<Boolean>('isMenuOpen', false)

const handleToggle = (): void => emit('toggleIsMenuOpen')
</script>

<style scoped>
header {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: var(--block);
  background-color: var(--yellow);
  height: calc(var(--block) * 5);
}

header button {
  color: white;
}
</style>
