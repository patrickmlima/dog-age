<script setup lang="ts">
  import AgeForm from './components/AgeForm.vue';
</script>

<template>
  <header>
    <h1>Here you can check your dog age human equivalence</h1>
  </header>

  <main>
    <AgeForm />
  </main>

  <footer>
    <p>&copy; Patrick Lima, 2024</p>
  </footer>
</template>

<style scoped>
  header {
    position: relative;
    top: 0;
    display: block;
    background-color: #1ba62f;
    width: 100%;
    padding: 0.5rem 1rem;
    color: whitesmoke;

    h1 {
      font-size: 1.7rem;
    }
  }
  
  main {
    position: relative;
    display: block;
    margin-bottom: 2.5rem;
  }

  footer {
    position: fixed;
    bottom: 0;
    height: 2.5rem;
    padding-left: 2rem;
    background-color: #1ba62f;
    color: whitesmoke;
    width: 100%;
    font-size: small;
  }
</style>
