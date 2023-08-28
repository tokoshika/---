<template>
  <header>
    <nav>
      <ul>
        <li class="li">HOME</li>
        <li class="li">HOME</li>
        <li class="li">HOME</li>
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
