<script setup lang="ts">
const users = []

async function getUsers() {
  console.log('Getting users')
}
</script>

<template>
  <div class="users-controls">
    <button @click="getUsers">Get users</button>
    <span><b>Users count:</b> {{ users.length }}</span>
  </div>
</template>

<style scoped>
.users-controls {
  display: flex;
  align-items: center;
  gap: 2rem;
}
</style>
