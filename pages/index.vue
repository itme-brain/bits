<template>
  <div class="main">
    <div class="symbol">
      <Symbol />
    </div>
  </div>
  <div class="satsConversion">
    1 <i class="icon-Bits-Symbol"></i> = 100<i class="fak fa-regular"></i>
  </div>
  <!--<div class="bitcoinConversion">
    1 ₿ = 1,000,000 <i class="icon-Bits-Symbol"></i>
  </div> -->
  <div class="body">
    <div class="kits">
      👇️ Free and Open Source 👇️
    </div>
    <div class="buttons">
      <Buttons />
    </div>
      <div class="license">
        <CC0 />
      </div>
    <div>
      <NuxtLink to="/adoption" class="supporters">
        Adoption
      </NuxtLink>
    </div>
  </div>
  <footer>
    <div class="info">
      Questions or Suggestions?<br>
      Please reach out 🙂 <br>
      <a href="mailto:hi@bits.name" class="email">
        hi@bits.name
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
      satsSymbol.defer = true;

      bitsSymbol.src = '/bitsSymbol.js';
      bitsSymbol.defer = true;

      document.head.appendChild(satsSymbol);
      document.head.appendChild(bitsSymbol);
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

  .satsConversion {
    @apply text-center text-3xl font-bold mt-0 select-none;
    opacity: 0;
    animation: fadeIn ease 5s;
    animation-delay: 5s;
    animation-fill-mode: forwards
  }

 /* .bitcoinConversion {
    @apply text-center text-3xl font-bold mt-0 mb-0 select-none;
    opacity: 0;
    animation: fadeIn ease 5s;
    animation-delay: 8s;
    animation-fill-mode: forwards
  } */

  .body {
    @apply mt-0;
    opacity: 0;
    animation: fadeIn ease 5s;
    animation-delay: 10s;
    animation-fill-mode: forwards
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
    animation: slideUp 5s ease, fadeIn 3s ease forwards;
    animation-delay: 15s;
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
