<template>
  <Header :isMenuOpen="isMenuOpen" @toggleIsMenuOpen="toggleIsMenuOpen" />
  <main>
    <slot/>
  </main>
  <footer>
    Enjoy
  </footer>
</template>

<script lang="ts" setup>
import { ref, provide } from 'vue'
import Header from './Header.vue';

const isMenuOpen = ref<Boolean>(false);
const toggleIsMenuOpen = (): void => {
  isMenuOpen.value = !isMenuOpen.value
}

provide('isMenuOpen', isMenuOpen)
</script>
