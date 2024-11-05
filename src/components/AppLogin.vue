<script setup lang="ts">
function login() {
  console.log('Login')
}
</script>

<template>
  <div class="login">
    <input type="text" placeholder="Enter your name..." />
    <button @click="login">Log in</button>
  </div>
</template>

<style scoped>
.login {
  display: flex;
  align-items: center;
  gap: 2rem;
}
</style>
