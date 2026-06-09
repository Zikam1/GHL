<script setup>
import { ref } from "vue"

// current date
const currentDate = ref(new Date())

// month + day labels
const monthNames = [
  "January","February","March","April","May","June",
  "July","August","September","October","November","December"
]

const days = ["Su","Mo","Tu","We","Th","Fr","Sa"]

// generate calendar days
const getDaysInMonth = (date) => {
  const year = date.getFullYear()
  const month = date.getMonth()

  const firstDay = new Date(year, month, 1).getDay()
  const totalDays = new Date(year, month + 1, 0).getDate()

  let calendar = []

  // empty spaces
  for (let i = 0; i < firstDay; i++) {
    calendar.push(null)
  }

  // actual days
  for (let i = 1; i <= totalDays; i++) {
    calendar.push(i)
  }

  return calendar
}

// navigation
const nextMonth = () => {
  currentDate.value = new Date(
    currentDate.value.getFullYear(),
    currentDate.value.getMonth() + 1,
    1
  )
}

const prevMonth = () => {
  currentDate.value = new Date(
    currentDate.value.getFullYear(),
    currentDate.value.getMonth() - 1,
    1
  )
}

// redirect
const bookNow = () => {
  window.open(
    "https://www.fiverr.com/zikam10/design-and-build-websites-funnels-and-landing-pages-using-gohighlevel",
    "_blank"
  )
}
</script>

<template>
  <section id="booking" class="py-32 px-6 bg-white">
    <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-16 items-center">

      <!-- LEFT SIDE -->
      <div>
        <p class="text-gray-500 font-semibold uppercase tracking-widest mb-4">
          Free Strategy Session
        </p>

        <h2 class="text-5xl font-bold mb-6 leading-tight text-green-900">
          Let’s Build You a System That 
          <span class="text-black">Generates Clients Daily</span>
        </h2>

        <p class="text-gray-600 text-lg mb-10">
          In this free call, we’ll map out a clear funnel and automation strategy tailored to your business  so you can start attracting and closing clients consistently.
        </p>

        <!-- BULLETS -->
        <div class="space-y-5 mb-10">

          <div class="flex items-start gap-4">
            <div class="w-6 h-6 bg-black text-white flex items-center justify-center rounded-full text-sm">✓</div>
            <p class="text-gray-700">Identify where you're losing leads & revenue</p>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-6 h-6 bg-black text-white flex items-center justify-center rounded-full text-sm">✓</div>
            <p class="text-gray-700">Get a custom funnel & automation plan</p>
          </div>

          <div class="flex items-start gap-4">
            <div class="w-6 h-6 bg-black text-white flex items-center justify-center rounded-full text-sm">✓</div>
            <p class="text-gray-700">Learn how to turn traffic into paying clients</p>
          </div>

        </div>

        <!-- URGENCY -->
        <div class="bg-gray-50 border border-gray-200 rounded-xl p-6">
          <p class="text-sm text-gray-600">
            ⚠️ Limited slots available each week — only serious business owners.
          </p>
        </div>
      </div>

      <!-- RIGHT SIDE -->
      <div class="bg-white rounded-3xl shadow-2xl border border-gray-200 p-6 md:p-8">

        <h3 class="text-2xl font-semibold mb-4 text-center text-gray-900">
          Schedule Your Call
        </h3>

        <p class="text-gray-500 text-center mb-6 text-sm">
          Takes less than 30 seconds to book
        </p>

        <!-- CALENDAR -->
        <div class="border border-gray-200 rounded-2xl p-6 w-full max-w-md mx-auto">

          <!-- Header -->
          <div class="flex items-center justify-between mb-4">
            <h3 class="font-semibold text-gray-900">
              {{ monthNames[currentDate.getMonth()] }} {{ currentDate.getFullYear() }}
            </h3>

            <div class="flex gap-3 text-gray-500">
              <button @click="prevMonth" class="hover:text-black transition">←</button>
              <button @click="nextMonth" class="hover:text-black transition">→</button>
            </div>
          </div>

          <!-- Days -->
          <div class="grid grid-cols-7 text-xs text-gray-500 mb-2">
            <span v-for="day in days" :key="day">{{ day }}</span>
          </div>

          <!-- Dates -->
          <div class="grid grid-cols-7 gap-2 text-sm">
            <template v-for="(day, index) in getDaysInMonth(currentDate)" :key="index">
              <span v-if="day === null"></span>

              <button
                v-else
                @click="bookNow"
                class="py-2 rounded-lg hover:bg-black hover:text-white transition"
              >
                {{ day }}
              </button>
            </template>
          </div>

          <!-- CTA -->
          <button 
            @click="bookNow"
            class="block w-full mt-6 text-center bg-green-700 text-white py-3 rounded-xl hover:scale-105 transition"
          >
            Book a Time
          </button>

        </div>

        <!-- TRUST -->
        <p class="text-xs text-gray-400 text-center mt-4">
          Your information is secure and will never be shared.
        </p>

      </div>

    </div>
  </section>
</template>