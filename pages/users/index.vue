<script setup lang="ts">
definePageMeta({layout: 'users'})
/*const users = ref([
    {id: 1, name: 'Alex'},
        {id: 2, name: 'Bob'},
        {id: 3, name: 'John'},
    ]
)*/
const { data } = await useFetch('https://dummyjson.com/users')
const users = ref(data.value.users)
</script>

<template>
  <div>
    <h1>Users</h1>
    <ul class="d-flex flex-wrap list-unstyled gap-3">
      <li v-for="user in users" :key="user.id">
        <NuxtLink :to="`/users/user-${ user.id }`" class="btn btn-primary">{{ user.firstName }} {{ user.lastName }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>

<style scoped>

</style>