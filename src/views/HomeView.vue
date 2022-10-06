<template>
  <main>
    <div class="greetings">
      <h1 class="green">VIZ-I</h1>
    </div>
    <IndiaMap />
  </main>
</template>
<script setup>
import IndiaMap from "../components/IndiaMap.vue";
</script>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}
</style>
