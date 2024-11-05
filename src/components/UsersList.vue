<script setup lang="ts">
const users = []
</script>

<template>
  <div class="users-list">
    <div v-if="users.length" class="table" role="table">
      <div class="row heading" role="row">
        <span>Name</span>
        <span>UserName</span>
        <span>Email</span>
        <span>City</span>
        <span>Phone</span>
      </div>
      <div class="row items" role="row" v-for="user in users" :key="user.id">
        <span>{{ user.name }}</span>
        <span>{{ user.username }}</span>
        <span>{{ user.email }}</span>
        <span>{{ user.address.city }}</span>
        <span>{{ user.phone }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.table {
  border: 1px solid var(--color-grey-200);
  font-size: 1.4rem;
  background-color: var(--color-grey-0);
  border-radius: 7px;
}
.row {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  column-gap: 2.4rem;
  -webkit-box-align: center;
  align-items: center;
  transition: none;
}
.heading {
  padding: 1.6rem 2.4rem;
  background-color: var(--color-grey-50);
  border-bottom: 1px solid var(--color-grey-100);
  text-transform: uppercase;
  letter-spacing: 0.4px;
  font-weight: 600;
  color: var(--color-grey-600);
}
.items {
  padding: 0.8rem 2.4rem;
}
.items:not(:last-child) {
  border-bottom: 1px solid var(--color-grey-100);
}
.items span {
  word-break: break-all;
}
</style>
