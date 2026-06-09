<template>
  <section class="relative py-28 bg-gradient-to-b from-black via-[#050505] to-black text-white overflow-hidden">

    <!-- glow background -->
    <div class="absolute inset-0">
      <div class="absolute w-[600px] h-[600px] bg-green-500/10 blur-[140px] rounded-full top-[-200px] left-[-200px]"></div>
    </div>

    <div class="relative max-w-4xl mx-auto px-6">

      <h2 class="text-4xl font-bold mb-20">
        Simple 3-Step Process
      </h2>

      <!-- left timeline line -->
      <div class="absolute left-6 top-40 bottom-0 w-[2px] bg-white/10"></div>

      <!-- animated progress line -->
      <div
        class="absolute left-6 top-40 w-[2px] bg-green-500 transition-all duration-700"
        :style="{ height: progressHeight + '%' }"
      ></div>

      <div class="space-y-20">

        <div
          v-for="(step, index) in steps"
          :key="index"
          class="relative pl-16"
        >

          <!-- dot -->
          <div class="absolute left-6 top-2 -translate-x-1/2">
            <div class="w-5 h-5 rounded-full bg-green-500 shadow-[0_0_25px_#22c55e] animate-pulse"></div>
          </div>

          <!-- number -->
          <div class="text-green-400 text-3xl font-bold mb-2">
            {{ displayNumbers[index] }}
          </div>

          <!-- text card -->
          <div class="bg-white/5 border border-white/10 rounded-xl p-6 backdrop-blur-md">
            <p class="text-gray-300 text-lg leading-relaxed">
              {{ step.text }}
            </p>
          </div>

        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const steps = [
  { number: 1, text: 'We analyze your business and goals' },
  { number: 2, text: 'I build your funnel & automation system' },
  { number: 3, text: 'You start getting consistent clients' }
]

const displayNumbers = ref([])
const progressHeight = ref(0)

let intervals = []
let loop = null

const format = (n) => String(n).padStart(2, '0')

const runAnimation = () => {
  displayNumbers.value = steps.map(s => s.number + 20)
  progressHeight.value = 0

  setTimeout(() => {
    progressHeight.value = 100
  }, 200)

  steps.forEach((step, i) => {
    let current = step.number + 50
    const target = step.number

    intervals[i] = setInterval(() => {
      current--
      displayNumbers.value[i] = format(current)

      if (current <= target) {
        displayNumbers.value[i] = format(target)
        clearInterval(intervals[i])
      }
    }, 40)
  })
}

onMounted(() => {
  runAnimation()
  loop = setInterval(runAnimation, 6000)
})

onBeforeUnmount(() => {
  intervals.forEach(clearInterval)
  clearInterval(loop)
})
</script>