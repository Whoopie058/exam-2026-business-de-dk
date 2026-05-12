<template>
  <header class="flex w-full items-center justify-between gap-4 bg-[#0E1B29] px-6 py-4">
    <div class="flex shrink-0 items-center">
      <div class="flex items-center">
        <img src="/Logo-Tekst.png" alt="Logo" class="h-20 w-auto" />
      </div>
    </div>

    <div class="flex flex-1 items-center justify-end gap-3">
      <div class="flex items-center gap-2">
        <div
          v-for="menu in menus"
          :key="menu.name"
          class="relative"
          @mouseleave="closeMenu"
        >
          <button
            type="button"
            class="rounded-full border border-white/10 bg-white/5 px-4 py-2 text-sm font-medium text-white transition hover:bg-white/10 focus:outline-none focus:ring-2 focus:ring-cyan-200/30"
            @click="toggleMenu(menu.name)"
          >
            {{ menu.name }}
          </button>

          <div
            v-show="activeMenu === menu.name"
            class="absolute left-1/2 top-full z-20 mt-3 w-44 -translate-x-1/2 rounded-2xl border border-white/10 bg-[#132638] p-2 shadow-xl shadow-slate-950/30"
          >
            <a
              v-for="item in menu.items"
              :key="item"
              href="#"
              class="block rounded-xl px-3 py-2 text-sm text-slate-100 transition hover:bg-white/10"
            >
              {{ item }}
            </a>
          </div>
        </div>
      </div>

      <input
        v-model="searchQuery"
        type="text"
        placeholder="Search..."
        class="w-full max-w-sm rounded-full border border-color-white bg-transparent px-4 py-2 text-sm text-white outline-none"
        @input="handleSearch"
      />
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'

const searchQuery = ref('')
const activeMenu = ref('')

const menus = [
  {
    name: 'menu1',
    items: ['menu1 option 1', 'menu1 option 2', 'menu1 option 3'],
  },
  {
    name: 'menu2',
    items: ['menu2 option 1', 'menu2 option 2', 'menu2 option 3'],
  },
  {
    name: 'menu3',
    items: ['menu3 option 1', 'menu3 option 2', 'menu3 option 3'],
  },
  {
    name: 'menu4',
    items: ['menu4 option 1', 'menu4 option 2', 'menu4 option 3'],
  },
]

const toggleMenu = (name) => {
  activeMenu.value = activeMenu.value === name ? '' : name
}

const closeMenu = () => {
  activeMenu.value = ''
}


const handleSearch = () => {
  console.log('Search query:', searchQuery.value)
}
</script>
