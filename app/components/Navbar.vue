<template>
  <header class="sticky top-0 z-50 bg-white/80 backdrop-blur border-b border-gray-100">
    <div class="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">

      <!-- LEFT: BRAND + POSITIONING -->
      <div class="flex flex-col leading-tight">
        <h1 class="text-lg md:text-xl font-semibold text-green-700">
          Aku.I
        </h1>
      
      </div>

      <!-- RIGHT: TRUST + CTA -->
      <div class="flex items-center gap-4">

        <!-- Trust badge -->
        <div class="hidden md:flex items-center gap-2 text-xs text-gray-500">
          <span class="w-2 h-2 bg-green-500 rounded-full animate-pulse"></span>
          Helping businesses get clients
        </div>

        <!-- CTA -->
        <a href="#booking"
           class="bg-green-600 text-white px-5 py-2 rounded-lg text-sm font-medium shadow hover:scale-105 transition">
          Book a Call
        </a>

      </div>

    </div>
  </header>
</template>