<template>
  <header class="header-container">
    <h1>to<span>do</span></h1>
  </header>
</template>

<script lang="ts">
export default {
  name: 'HeaderView'
}
</script>

<style scoped>
.header-container {
  background: var(--gray-700);
  height: 28rem;

  display: flex;
  align-items: center;
  justify-content: center;

  font-weight: 900;
  font-size: 1.6rem;
}

.header-container h1 {
  color: var(--blue);
}

.header-container h1 span {
  color: var(--purple-dark);
}
</style>
