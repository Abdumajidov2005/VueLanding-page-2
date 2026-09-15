<script setup>
const navItems = ['Home', 'About me', 'Portfolio', 'Contact']
</script>

<template>
  <header class="sticky top-0 z-40 bg-[#15171d]/90 backdrop-blur border-b border-white/5">
    <div class="max-w-6xl mx-auto flex items-center justify-between px-6 py-4">
      <div class="flex items-center gap-2 font-bold text-lg text-white">
        <svg width="22" height="22" viewBox="0 0 24 24" fill="none">
          <path d="M4 7a2 2 0 012-2h4l2 2h6a2 2 0 012 2v8a2 2 0 01-2 2H6a2 2 0 01-2-2V7z" stroke="#2fd0f0" stroke-width="1.8" />
        </svg>
        <span>Portfolio</span>
      </div>

      <nav class="hidden md:flex items-center gap-8 text-sm text-[#9aa0ac]">
        <a v-for="item in navItems" :key="item" href="#" class="hover:text-white transition-colors">
          {{ item }}
        </a>
      </nav>
    </div>
  </header>
</template>
