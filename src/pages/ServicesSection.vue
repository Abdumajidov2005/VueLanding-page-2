<script setup>
const servicesRowOne = [
  { label: 'Product Design', icon: 'M12 2l2 5 5 .5-4 3.5 1 5-4-2.5L8 16l1-5-4-3.5L10 7z' },
  { label: 'UX/UI Design', icon: 'M4 4h16v16H4z M8 9h8 M8 13h5' },
  { label: 'Icon Design', icon: 'M4 5h6v6H4z M14 5h6v6h-6z M4 13h6v6H4z M14 13h6v6h-6z' },
  { label: 'Logo Design', icon: 'M9 9a4 4 0 100-8 4 4 0 000 8z M13 13h7v7h-7z' },
]

const servicesRowTwo = [
  { label: 'Redesign', icon: 'M8 7L4 12l4 5 M16 7l4 5-4 5' },
  { label: 'Flatdesign', icon: 'M3 5h18v12H3z M8 20h8' },
  { label: 'Motion', icon: 'M4 4h12v12H4z M8 8h12v12H8z' },
]
</script>

<template>
  <section class="max-w-4xl mx-auto px-6 pb-20">
    <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 mb-4">
      <div
        v-for="s in servicesRowOne"
        :key="s.label"
        class="bg-[#20232c] rounded-xl p-6 flex flex-col items-center gap-3 border border-white/5 hover:border-[#2fd0f0]/40 transition"
      >
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" class="text-[#2fd0f0]">
          <path :d="s.icon" stroke="currentColor" stroke-width="1.6" />
        </svg>
        <span class="text-sm text-center text-[#9aa0ac]">{{ s.label }}</span>
      </div>
    </div>

    <div class="grid grid-cols-3 gap-4 max-w-xl mx-auto">
      <div
        v-for="s in servicesRowTwo"
        :key="s.label"
        class="bg-[#20232c] rounded-xl p-6 flex flex-col items-center gap-3 border border-white/5 hover:border-[#2fd0f0]/40 transition"
      >
        <svg width="26" height="26" viewBox="0 0 24 24" fill="none" class="text-[#2fd0f0]">
          <path :d="s.icon" stroke="currentColor" stroke-width="1.6" />
        </svg>
        <span class="text-sm text-center text-[#9aa0ac]">{{ s.label }}</span>
      </div>
    </div>
  </section>
</template>
