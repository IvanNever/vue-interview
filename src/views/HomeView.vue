<script setup lang="ts">
import AppLogin from '@/components/AppLogin.vue'
import AppLogout from '@/components/AppLogout.vue'
import UsersControls from '@/components/UsersControls.vue'
import UsersList from '@/components/UsersList.vue'

const userName = ''
</script>

<template>
  <div class="container">
    <header>
      <h1>Users App</h1>
      <div class="controls">
        <AppLogin />
        <AppLogout />
      </div>
    </header>
    <main>
      <span class="message" v-if="!userName">
        You need log in to get access
      </span>
      <template v-else>
        <UsersControls />
        <UsersList />
      </template>
    </main>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
header {
  padding: 2rem 4.8rem;
  display: flex;
  align-items: center;
  gap: 3rem;
  justify-content: space-between;
  border-bottom: 1px solid var(--color-grey-100);
  background-color: var(--color-grey-0);
}
.controls {
  display: flex;
  flex-wrap: wrap;
  justify-content: end;
  gap: 1rem 5rem;
}
main {
  flex: 1;
  display: flex;
  flex-direction: column;
  gap: 3rem;
  padding: 2rem 4.8rem;
  background-color: var(--color-grey-50);
}
.message {
  margin-top: 3rem;
  text-align: center;
  font-size: 2rem;
  color: var(--color-red-700);
}
</style>
