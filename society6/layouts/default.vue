<template>
  <header>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/">HOME</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/victory">終戦記念日</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/map">地図</NuxtLink>
        </li>
        <!-- <li class="li">HOME</li> -->
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
