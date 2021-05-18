<template>
  <Layout>
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Hello Vue 3.0 + Vite" />
  </Layout>
</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import Layout from './components/Layout.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Layout
  },
}
</script>
