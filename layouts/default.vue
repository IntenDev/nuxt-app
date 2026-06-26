<template>
  <div>
    <header class="bg-dark p-3">
      <ul class="nav">
        <li class="nav-item">
          <NuxtLink to="/" class="nav-link text-white">Главная</NuxtLink>
        </li>
        <li>
          <NuxtLink to="contact" class="nav-link text-white">Контакты</NuxtLink>
        </li>
        <li>
          <NuxtLink to="users" class="nav-link text-white">Пользователи</NuxtLink>
        </li>
      </ul>
    </header>
    <slot />
  </div>
</template>

<style>
header a:not(.router-link-exact-active):hover {
  text-decoration: underline;
}
header a.route-link-exact-active {
  color: #ffb636 !important;
  font-weight: 500;
}
h1 {color: red}
</style>