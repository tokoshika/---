<template>
  <header>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/" style="text-decoration: none">出来事</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/victory" style="text-decoration: none"
            >終戦記念日</NuxtLink
          >
        </li>
        <li>
          <NuxtLink to="/map">地図</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/friend">お友達</NuxtLink>
        </li>
      </ul>
    </nav>
  </header>

  <slot />
</template>

<style scoped>
  ul {
    display: flex;
  }
  li {
    color: red;
    list-style: none;
    margin-left: 2rem;
  }
</style>
