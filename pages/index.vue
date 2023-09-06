<template>
  <div class="main">
    <div class="symbol">
      <Symbol />
    </div>
  </div>
  <div class="body">
    <div class="conversion">
      1 <i class="icon-Bits-Symbol"></i> = 100<i class="fak fa-regular"></i>
    </div>
    <div class="kits">
      👇️ Free and Open Source 👇️
    </div>
    <div class="buttons">
      <Buttons />
    </div>
      <div class="license">
        <CC0 />
      </div>
    <!-- <div>
      <a class="supporters" href="/adoption">
        Adoption
      </a>
    </div> -->
  </div>
  <footer>
    <div class="info">
      Have any suggestions?<br>
      Please reach out 🙂 <br>
      <a href="mailto:hi@bits.name" class="email">
        hi@bits.name
      </a>
    </div>
    <div class="socials flex justify-center space-x-3 mt-0">
      <a href="https://github.com/itme-brain/bits.name">
        <img src="/assets/github.jpg" class="w-8 h-8 rounded-full">
      </a>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent, onMounted } from 'vue';

export default defineComponent({
  setup() {
    onMounted(() => {
      const satsSymbol = document.createElement('script');
      const bitsSymbol = document.createElement('script');

      satsSymbol.src = 'https://kit.fontawesome.com/090ca49637.js';
      satsSymbol.crossOrigin = 'anonymous';

      bitsSymbol.src = "/bitsSymbol.js";

      document.body.appendChild(satsSymbol);
      document.body.appendChild(bitsSymbol);
    });
  },
});
</script>

<style scoped>
  .main {
    opacity: 0;
    animation: fadeIn ease 10s;
    animation-fill-mode: forwards;
  }

  .symbol {
    @apply flex justify-center mt-10 mb-10;
  }

  .body {
    opacity: 0;
    animation: fadeIn ease 5s;
    animation-delay: 5s;
    animation-fill-mode: forwards
  }

  .conversion {
    @apply text-center text-3xl font-bold mt-0 select-none
  }

  .kits {
    @apply justify-center text-center items-center mt-10 mb-0
    font-semibold select-none;
  }

  .buttons {
    @apply mt-0
  }

  footer {
    @apply justify-center items-center mt-10;
    overflow-y: hidden;
    opacity: 0;
    animation: slideUp 3s ease, fadeIn 3s ease forwards;
    animation-delay: 8s;
    animation-fill-mode: forwards;
  }
  
  @keyframes fadeIn {
    0% {opacity: 0;} 
    100% {opacity: 1;}
  }

  @keyframes slideUp {
    0% { transform: translateY(100%); }
    100% { transform: translateY(0); }
  }

  .supporters {
    @apply flex justify-center mt-0 mb-5
    text-xl text-blue-900 cursor-pointer underline font-mono
  }

  .info {
    @apply justify-center text-center items-center mb-3 mt-0 font-semibold
  }
  
  .email {
    @apply underline text-blue-900 cursor-pointer
  }

  .license {
    @apply flex justify-center items-center mb-5 mt-5
  }

  .socials {
  }
</style>
