<template>
  <div>
    <table>
      <tr>
        <th></th>
        <th>Bits</th>
        <th>Symbol</th>
      </tr>
      <tr v-for="entry in tableData" :key="entry.project">
        <td>
          <div class="logo-container">
            <a :href="entry.link">
              <img :src="entry.logo" alt="Logo" class="logo"/>
            </a>
          </div>
        </td>
        <td>
          {{ entry.bitName ? '✅' : '❌' }}
          <span v-if="entry.differentName">
            *
          </span>
        </td>
        <td>
          {{ entry.bitSymbol ? '✅' : '❌' }}
        </td>
      </tr>
    </table>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'

interface TableEntry {
  project: string;
  logo?: string;
  logoExtension: string;
  link: string;
  bitName: boolean;
  differentName?: boolean;
  bitSymbol: boolean;
}

export default defineComponent({
  setup () {
    const tableData = ref<TableEntry[]>([
      {
        project: 'Bitcoin_Core',
        logoExtension: 'png',
        link: 'https://bitcoincore.org/',
        bitName: true,
        differentName: true,
        bitSymbol: false
      },
      {
        project: 'Blockstream_Green',
        logoExtension: 'svg',
        link: 'https://blockstream.com/green/',
        bitName: true,
        bitSymbol: false
      },
      {
        project: 'Phoenix_Wallet',
        logoExtension: 'png',
        link: 'https://phoenix.acinq.co/',
        bitName: true,
        bitSymbol: false
      },

      // ... more entries
    ]);

    const logoPath = (entry: TableEntry) => {
      return `/logos/${entry.project.toLowerCase()}.${entry.logoExtension}`
    }

    tableData.value.forEach((entry) => {
      entry.logo = logoPath(entry);
    });

    return { tableData }
  }
})
</script>

<style scoped>
  table {
    @apply text-center border-collapse select-none
  }

  th, td {
    @apply border px-4 py-2
  }
  
  .logo-container {
    @apply flex justify-center
  }

  .logo {
    @apply w-12 h-12 rounded-full object-cover cursor-pointer hover:scale-110 transition duration-300 ease-in-out
  }
</style>
