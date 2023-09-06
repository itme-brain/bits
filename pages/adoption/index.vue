<template>
  <header class="heading">
    Tracking Bits Adoption
  </header>
  <div class="text">
    Email for addition or suggestions<br>
    <a href="mailto:hi@bits.name" class="email">
      hi@bits.name
    </a>
  </div>
  <div class="table">
    <Table />
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
  .heading {
    @apply text-center text-3xl font-bold mt-24
  }

  .table {
    @apply justify-center flex mt-10
  }

  .text {
    @apply text-center mt-10
  }

  .email {
    @apply text-blue-900 underline
  }
</style>
