<script setup>
const badges = [
  { label: "</>", style: "top:8%; left:0%;" },
  { label: "UI", style: "top:2%; right:6%;" },
  { label: "UX", style: "top:38%; left:-8%;" },
  { label: "PS", style: "bottom:4%; left:34%;" },
];
</script>

<template>
  <section
    class="max-w-6xl mx-auto px-6 py-16 md:py-24 grid md:grid-cols-2 gap-12 items-center"
  >
    <div>
      <p class="uppercase tracking-wide text-sm text-[#9aa0ac] mb-3">Hello</p>
      <h1
        class="text-4xl md:text-5xl font-extrabold leading-tight mb-5 text-white"
      >
        I'm Gleb<br />Kostrubov
      </h1>
      <p class="text-[#9aa0ac] max-w-md mb-8 leading-relaxed">
        I create UI/UX designs, logos and icons that help products feel simple
        and clear. Every project starts with understanding the person who will
        use it.
      </p>
      <button
        class="bg-[#f2a72e] text-[#1b1206] font-semibold px-7 py-3 rounded-md hover:brightness-110 transition"
      >
        Contact me
      </button>
    </div>

    <div class="relative mx-auto w-72 h-72">
      <!-- glowing cyan ring -->
      <div
        class="absolute inset-0 rounded-full"
        style="
          background: conic-gradient(
            from 180deg,
            #2fd0f0 0deg,
            #2fd0f0 260deg,
            transparent 260deg,
            transparent 360deg
          );
          filter: drop-shadow(0 0 18px rgba(47, 208, 240, 0.45));
        "
      ></div>

      <!-- photo placeholder: almashtiring o'z rasmingizga -->
      <div
        class="absolute inset-3 rounded-full bg-[#1b1e26] overflow-hidden flex items-end justify-center"
      >
        <img
          src="/public/imgs/images.jfif"
          alt="Gleb Kostrubov"
          class="w-full h-full object-cover"
        />
      </div>

      <div
        v-for="badge in badges"
        :key="badge.label"
        class="absolute w-10 h-10 rounded-full bg-[#20232c] border border-white/10 flex items-center justify-center text-[11px] font-semibold text-white shadow-lg"
        :style="badge.style"
      >
        {{ badge.label }}
      </div>
    </div>
  </section>
</template>
