<template>
  <transition appear name="menu-slide">
    <form submit.prevent v-if="isMenuOpen">
      Hey it's me the sidebar!
    </form>
  </transition>
</template>

<script setup lang="ts">
import { inject } from 'vue'

const isMenuOpen = inject<Boolean>('isMenuOpen', false)
</script>

<style>
form {
  position: absolute;
  top: calc(var(--block) * 5);
  right: 0;
  background: var(--yellow);
  min-height: calc(100vh - (var(--block) * 5));
  padding: var(--block);
  display: block;
  overflow: auto;
  width: 100%;
  max-width: 24rem;
}
</style>
