<script setup></script>

<template>
  <section
    class="max-w-6xl mx-auto px-6 py-16 grid md:grid-cols-2 gap-16 items-center"
  >
    <div class="relative w-full max-w-sm h-80 mx-auto">
      <!-- decorative arcs -->
      <div
        class="absolute -top-6 -left-6 w-40 h-40 rounded-full border-[10px] border-t-[#7d838f] border-r-[#7d838f] border-b-transparent border-l-transparent opacity-70"
      ></div>
      <div
        class="absolute -top-2 right-0 w-28 h-28 rounded-full border-[8px] border-t-[#f2a72e] border-l-[#f2a72e] border-r-transparent border-b-transparent"
      ></div>
      <div
        class="absolute bottom-0 right-6 w-36 h-36 rounded-full border-[8px] border-b-[#2fd0f0] border-r-[#2fd0f0] border-t-transparent border-l-transparent"
      ></div>

      <!-- photo collage: har birini o'z rasmingizga almashtiring -->
      <div
        class="absolute top-6 left-6 w-28 h-32 rounded-lg overflow-hidden shadow-xl border border-white/10"
      >
        <img
          src="/public/imgs/images.jfif"
          alt=""
          class="w-full h-full object-cover"
        />
      </div>
      <div
        class="absolute top-24 right-2 w-32 h-36 rounded-lg overflow-hidden shadow-xl border border-white/10"
      >
        <img
          src="/public/imgs/images.jfif"
          alt=""
          class="w-full h-full object-cover"
        />
      </div>
      <div
        class="absolute bottom-2 left-12 w-28 h-24 rounded-lg overflow-hidden shadow-xl border border-white/10"
      >
        <img
          src="/public/imgs/images.jfif"
          alt=""
          class="w-full h-full object-cover"
        />
      </div>
    </div>

    <div>
      <h2 class="text-2xl font-bold mb-4 text-white">About me</h2>
      <p class="text-[#9aa0ac] leading-relaxed">
        Hi! I'm a product and UI/UX designer with a few years of experience
        turning ideas into clean, usable interfaces. I care about the small
        details — spacing, color, motion — as much as the big picture, because
        that's what makes a product feel effortless. Outside of design work, I
        like traveling and taking photos, which is where a lot of my color and
        composition instincts come from.
      </p>
    </div>
  </section>
</template>
