<template>
  <div>
    <HeaderView />

    <main class="wrapper-container">
      <CreateTaskView />
    </main>
  </div>
</template>

<script lang="ts">
import HeaderView from '../components/HeaderView.vue'
import CreateTaskView from '../components/CreateTaskView.vue'

export default {
  name: 'HomeView',
  components: { HeaderView, CreateTaskView }
}
</script>

<style scoped>
  .wrapper-container {
    max-width: 73.6rem;
    margin: -2.8rem auto 10rem;
    padding: 0 1.6rem;
  }
</style>
