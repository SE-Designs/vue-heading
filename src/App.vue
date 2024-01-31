<script setup lang="ts">
import Alert from './components/layout/Alert.vue'
import Banner from './components/layout/Banner.vue'
</script>
<template>
  <header>
    <Alert />
  </header>
  <Banner />
  <main>
    <!-- CONTENT HERE -->
  </main>
</template>
<style lang="scss">
// GLOBAL STYLES

html {
  scroll-behavior: smooth;
  font-family: 'Roboto', sans-serif;
}

body {
  min-height: 200vh;
  // or 200dvh
}

header {
  height: 108px;
}

span {
  color: #d7a830;
  font-weight: 700;
}

button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 0;
  outline: 0;
  font-family: inherit;
  cursor: pointer;
  height: 38px;

  transition: opacity 0.2s;

  &:hover {
    opacity: 0.9;
  }

  &.btn-primary {
    background-color: #fff;
    color: #000;
    border-radius: 14px;
    padding: 10px 14px;

    font-weight: 500;
  }

  &.btn-secondary {
    background-color: rgba(255, 255, 255, 0.1);
    opacity: 0.9;
    color: #fff;
    border-radius: 14px;
    padding: 12px 24px;

    font-weight: 500;
  }

  &.btn-ghost {
    background-color: transparent;
    color: #fff;
    opacity: 0.5;
    padding: 10px;
  }
}
</style>
