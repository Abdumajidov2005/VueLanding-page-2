<script setup>
import { ref } from 'vue'

const projects = [
  {
    name: 'Learning Ice-cream',
    title: 'YOUR NEW UNIVERSE',
    gradient: 'linear-gradient(135deg,#d63b6a,#7b2ff7)',
    description:
      'A landing page concept for a creative studio — bold gradients, playful type and a single clear call to action.',
  },
  {
    name: 'Weather App UI',
    title: 'SKYLINE',
    gradient: 'linear-gradient(135deg,#1f8ef1,#0b3d91)',
    description:
      'A minimal weather app interface focused on glanceable data and calm, muted color states.',
  },
  {
    name: 'Fintech Dashboard',
    title: 'CLEARPATH',
    gradient: 'linear-gradient(135deg,#0f9b6c,#0a3d2e)',
    description:
      'A dashboard redesign for a fintech product, simplifying complex data into clear, scannable cards.',
  },
]

const current = ref(0)

const next = () => {
  current.value = (current.value + 1) % projects.length
}

const prev = () => {
  current.value = (current.value - 1 + projects.length) % projects.length
}
</script>

<template>
  <section class="max-w-5xl mx-auto px-6 py-16 text-center">
    <h2 class="text-2xl font-bold mb-10 text-white">Portfolio</h2>

    <div class="relative flex items-center justify-center gap-6">
      <button
        @click="prev"
        class="shrink-0 w-11 h-11 rounded-full bg-[#f2a72e] text-[#1b1206] flex items-center justify-center hover:brightness-110 transition"
      >
        ‹
      </button>

      <div class="bg-[#20232c] rounded-xl p-6 md:p-8 grid md:grid-cols-2 gap-8 items-center text-left w-full">
        <div class="rounded-lg overflow-hidden border border-white/10">
          <div
            class="h-48 flex items-center justify-center text-2xl font-extrabold text-white"
            :style="{ background: projects[current].gradient }"
          >
            {{ projects[current].title }}
          </div>
        </div>
        <div>
          <h3 class="text-lg font-semibold mb-3 text-white">{{ projects[current].name }}</h3>
          <p class="text-sm text-[#9aa0ac] leading-relaxed">{{ projects[current].description }}</p>
        </div>
      </div>

      <button
        @click="next"
        class="shrink-0 w-11 h-11 rounded-full bg-[#f2a72e] text-[#1b1206] flex items-center justify-center hover:brightness-110 transition"
      >
        ›
      </button>
    </div>

    <div class="flex justify-center gap-2 mt-6">
      <span
        v-for="(p, i) in projects"
        :key="p.name"
        class="w-2 h-2 rounded-full transition"
        :class="i === current ? 'bg-[#2fd0f0]' : 'bg-white/15'"
      ></span>
    </div>
  </section>
</template>
