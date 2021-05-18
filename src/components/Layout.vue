<template>
  <body>
    <Header :isMenuOpen="isMenuOpen" @toggleIsMenuOpen="toggleIsMenuOpen" />
    <slot/>
    <footer>
      Enjoy
    </footer>
  </body>
</template>

<script lang="ts">
import { ref, provide } from 'vue'
import Header from './Header.vue';

export default {
  components: { Header },

  setup() {
    const isMenuOpen = ref(false);
    const toggleIsMenuOpen = (): void => {
      console.log('yetp')
      isMenuOpen.value = !isMenuOpen.value
    }

    provide('isMenuOpen', isMenuOpen)

    return {
      isMenuOpen,
      toggleIsMenuOpen
    }
  }
}
</script>
