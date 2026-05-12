<template>
  <header class="flex w-full items-center justify-between gap-4 bg-[#0E1B29] px-6 py-4 shadow-lg shadow-slate-950/20">
    <div class="flex min-w-0 flex-1 items-center">
      <div class="flex items-center">
        <img src="/Logo-Tekst.png" alt="Logo" class="h-20 w-auto" />
      </div>
    </div>

    <div class="flex flex-1 justify-end">
      <input
        v-model="searchQuery"
        type="text"
        placeholder="Search..."
        class="w-full max-w-sm rounded-full border border-white/20 bg-transparent px-4 py-2 text-sm text-white outline-none transition placeholder:text-white/60 focus:border-cyan-300 focus:ring-2 focus:ring-cyan-200/30"
        @input="handleSearch"
      />
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

// comment here
const searchQuery = ref('')


const handleSearch = () => {
  console.log('Search query:', searchQuery.value)
}
</script>
