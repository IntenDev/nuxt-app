<script setup lang="ts">
definePageMeta({layout: 'users'})
const {user_id} = useRoute().params
const {data} = await useFetch(`https://dummyjson.com/users/${user_id}`)
</script>

<template>
  <div>
    <h1>ID of user: {{ user_id }}</h1>
    <div class="card shadow-lg">
      <div class="row g-0">
        <!-- Profile Image -->
        <div class="col-md-4">
          <img :src="data.image" alt="User Image" class="img-fluid rounded-start h-100">
        </div>
        <!-- User Information-->
        <div class="col-md-8">
          <div class="card-body">
            <h2 class="card-title">{{ data.firstName }} {{ data.lastName }}</h2>
            <p class="card-text text-muted">ID: {{ user_id }} | Age: {{ data.age }}</p>
            <ul class="list-group list-group-flush">
              <li class="list-group-item"><strong>Email:</strong> {{ data.email }}</li>
              <li class="list-group-item"><strong>Phone:</strong> {{ data.phone }}</li>
              <li class="list-group-item"><strong>Address:</strong> {{ data.address.address }} {{ data.address.city }}
                {{ data.address.state }} {{ data.address.stateCode }} {{ data.address.postalCode }}
                {{ data.address.country }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>


  </div>

</template>

<style scoped>

</style>