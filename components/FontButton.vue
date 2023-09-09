<template>
  <div class="button">
    <a href="/FontKit.zip">
      .Zip
    </a>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.button {
  @apply flex max-w-sm mx-auto rounded-lg mt-10 select-none justify-center items-center
         bg-purple-600 h-10 text-white text-lg font-bold
}

.button:hover {
  @apply bg-orange-500
}
</style>
