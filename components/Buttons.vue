<template>
  <div class="buttons">
    <a href="BitsSymbolGraphicsKit.zip" class="button-left">
      Graphics Kit
    </a>
    <NuxtLink to="/font" class="button-right">
      Font Kit
    </NuxtLink>
  </div>
</template>


<script lang="ts"></script>

<style scoped>
.buttons {
  @apply flex max-w-lg mx-auto rounded-lg mt-10 select-none
}

.button-left, .button-right {
  @apply text-white text-lg font-bold font-sans bg-purple-600
}

.button-left {
  @apply flex-1 text-center p-4 border-r border-white rounded-l-lg
}

.button-right {
  @apply flex-1 text-center p-4 rounded-r-lg
}

.button-left:hover, .button-right:hover {
  @apply bg-orange-500
}
</style>
