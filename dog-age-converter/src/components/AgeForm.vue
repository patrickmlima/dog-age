<script setup lang="ts">
import { ref, computed } from 'vue'

const age = ref(0)
const equivalentAge = computed(() => (age.value ? (Math.log(age.value) * 16 + 31).toFixed(2) : '0'));
</script>

<template lang="html">
  <form id="age">
    <label for="age">Your dog age: <input id="age" type="number" min="0" v-model="age" /></label>
  </form>
  <p>Equivalent to: {{ equivalentAge }} human years</p>

  <section id="references">
    <p>
      The calculated age is based on a 2019 study called:
      <a href="https://www.biorxiv.org/content/10.1101/829192v1.full"
        >Quantitative translation of dog-to-human aging by conserved remodeling of epigenetic
        networks</a
      >
    </p>
  </section>
</template>

<style scoped>
form,
p {
  padding: 10px;
}

#references {
  position: fixed;
  bottom: 2rem;
}
</style>
