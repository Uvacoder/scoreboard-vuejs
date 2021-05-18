<template>
  <header>
    Welcome to Vue 3 Scoreboard!

    <button @click="handleToggle">Menu {{ String(isMenuOpen) }}</button>
    <span v-if="isMenuOpen">Menu is open</span>
  </header>
</template>

<script lang="ts">
import { inject } from 'vue'

export default {
  // props: {
  //   isMenuOpen: {
  //     type: Boolean,
  //   }
  // },
  // methods: {
  //   handleToggle() {
  //     this.$emit('toggleMenuIsOpen')
  //   }
  // }

  setup(props, { emit }) {
    const isMenuOpen = inject('isMenuOpen', false)

    const handleToggle = () => {
      console.log('here')
      emit('toggleIsMenuOpen')
    }

    return {
      isMenuOpen,
      handleToggle
    }
  }
}


</script>
