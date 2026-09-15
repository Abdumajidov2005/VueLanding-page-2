<script setup>
const navItems = ['Home', 'About me', 'Portfolio', 'Contact']
</script>

<template>
  <footer class="border-t border-white/5 bg-[#1b1e26] mt-10">
    <div class="max-w-6xl mx-auto px-6 py-12 grid sm:grid-cols-3 gap-8 text-sm">
      <div>
        <p class="text-white font-semibold mb-3">Menu</p>
        <ul class="space-y-2 text-[#9aa0ac]">
          <li v-for="item in navItems" :key="item">{{ item }}</li>
        </ul>
      </div>

      <div>
        <p class="text-white font-semibold mb-3">Contacts</p>
        <p class="text-[#9aa0ac]">gleb.kostrubov@email.com</p>
        <p class="text-[#9aa0ac]">+1 234 56 - 78 - 90</p>
      </div>

      <div class="flex sm:justify-end items-start gap-2 text-white">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none">
          <path d="M4 7a2 2 0 012-2h4l2 2h6a2 2 0 012 2v8a2 2 0 01-2 2H6a2 2 0 01-2-2V7z" stroke="#2fd0f0" stroke-width="1.8" />
        </svg>
        <span class="font-semibold">Portfolio</span>
      </div>
    </div>

    <div class="text-center text-xs text-[#9aa0ac] pb-6">
      Copyright © 2026 Portfolio. All rights reserved.
    </div>
  </footer>
</template>
