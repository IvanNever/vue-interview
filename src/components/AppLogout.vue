<script setup lang="ts">
const userName = ''
function logout() {
  console.log('logout')
}
</script>

<template>
  <div class="logout">
    <span><b>User Name:</b> {{ userName || 'No authorized' }}</span>
    <button @click="logout">Log out</button>
  </div>
</template>

<style scoped>
.logout {
  display: flex;
  align-items: center;
  gap: 2rem;
}
</style>
