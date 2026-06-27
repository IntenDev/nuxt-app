<template>
  <div>
    <header class="bg-dark p-3 container">
      <ul class="nav container">
        <li class="nav-item">
          <NuxtLink to="/" class="nav-link text-white">Главная</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/contact" class="nav-link text-white">Контакты</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/users" class="nav-link text-white">Пользователи</NuxtLink>
        </li>
      </ul>
    </header>
    <div class="container py-5">
      <slot />
    </div>

    <footer class="bg-dark p-3 container">
      <p class="text-white">All rights reserved &copy;</p>
    </footer>
  </div>
</template>

<style>

</style>
<script setup lang="ts">
</script>