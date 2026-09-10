<script setup>
import { ref } from "vue";

const mahsulot = ref({
  nomi: "iPhone 15 Pro",
  tavsif: "Titanium dizayn, A17 Pro chip, 48MP kamera tizimi",
  rasm: "https://picsum.photos/400/300?random=1",
  narx: 14500000,
  eskiNarx: 17000000,
  mavjud: true,
});

const miqdor = ref(1);

// Chegirma foizini hisoblash
const chegirma = Math.round(
  ((mahsulot.value.eskiNarx - mahsulot.value.narx) / mahsulot.value.eskiNarx) *
    100,
);

function oshir() {
  if (miqdor.value < 10) miqdor.value++;
}

function kamaytir() {
  if (miqdor.value > 1) miqdor.value--;
}
</script>

<template>
  <div class="min-h-screen bg-gray-50 p-8">
    <h1 class="text-3xl font-bold text-center text-gray-800 mb-8">
      Mahsulotlar
    </h1>

    <div
      class="max-w-sm mx-auto bg-white rounded-2xl shadow-lg overflow-hidden"
    >
      <!-- Rasm -->
      <img
        :src="mahsulot.rasm"
        :alt="mahsulot.nomi"
        class="w-full h-56 object-cover"
      />

      <!-- Ma'lumotlar -->
      <div class="p-6">
        <div class="flex items-center justify-between mb-2">
          <h2 class="text-xl font-bold text-gray-800">{{ mahsulot.nomi }}</h2>
          <span
            class="text-xs font-semibold px-3 py-1 rounded-full"
            :class="{
              'bg-green-100 text-green-700': mahsulot.mavjud,
              'bg-red-100 text-red-700': !mahsulot.mavjud,
            }"
          >
            {{ mahsulot.mavjud ? "Mavjud" : "Tugagan" }}
          </span>
        </div>

        <p class="text-gray-500 text-sm mb-4">{{ mahsulot.tavsif }}</p>

        <!-- Narx -->
        <div class="flex items-center justify-between mb-4">
          <div>
            <span
              v-if="mahsulot.eskiNarx"
              class="text-gray-400 line-through text-sm mr-2"
            >
              {{ mahsulot.eskiNarx.toLocaleString() }} so'm
            </span>
            <span class="text-2xl font-bold text-green-600">
              {{ mahsulot.narx.toLocaleString() }} so'm
            </span>
          </div>
        </div>

        <!-- Chegirma foizi -->
        <div
          v-if="mahsulot.eskiNarx"
          class="bg-yellow-50 text-yellow-700 text-sm font-medium px-3 py-2 rounded-lg mb-4 text-center"
        >
          🔥 {{ chegirma }}% chegirma!
        </div>

        <!-- Miqdor -->
        <div class="flex items-center gap-4 mb-4">
          <span class="text-gray-600 text-sm">Miqdor:</span>
          <div class="flex items-center gap-2">
            <button
              @click="kamaytir"
              :disabled="miqdor <= 1"
              class="w-8 h-8 rounded-lg bg-gray-100 text-gray-600 hover:bg-gray-200 disabled:opacity-40 disabled:cursor-not-allowed transition"
            >
              −
            </button>
            <span class="w-8 text-center font-bold">{{ miqdor }}</span>
            <button
              @click="oshir"
              :disabled="miqdor >= 10"
              class="w-8 h-8 rounded-lg bg-gray-100 text-gray-600 hover:bg-gray-200 disabled:opacity-40 disabled:cursor-not-allowed transition"
            >
              +
            </button>
          </div>
        </div>

        <!-- Jami -->
        <div class="bg-gray-50 rounded-xl p-3 mb-4 text-center">
          <span class="text-gray-500 text-sm">Jami: </span>
          <span class="text-xl font-bold text-gray-800">
            {{ (mahsulot.narx * miqdor).toLocaleString() }} so'm
          </span>
        </div>

        <!-- Tugma -->
        <button
          :disabled="!mahsulot.mavjud"
          class="w-full py-3 rounded-xl font-semibold transition active:scale-[0.98]"
          :class="{
            'bg-green-500 text-white hover:bg-green-600': mahsulot.mavjud,
            'bg-gray-200 text-gray-400 cursor-not-allowed': !mahsulot.mavjud,
          }"
        >
          {{ mahsulot.mavjud ? "🛒 Savatga qo'shish" : "Mavjud emas" }}
        </button>
      </div>
    </div>
  </div>
</template>
