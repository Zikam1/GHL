<template>
  <section id="portfolio" class="bg-black py-24">
    <div class="max-w-7xl mx-auto px-6">

      <!-- Header -->
      <div class="text-center max-w-3xl mx-auto mb-16">
        <span
          class="inline-flex items-center rounded-full border border-green-500/30 bg-green-500/10 px-4 py-1 text-sm font-medium text-green-400"
        >
          Portfolio
        </span>

        <h2 class="mt-6 text-4xl md:text-5xl font-bold text-white leading-tight">
          Building High-Converting
          <span class="text-green-500">GoHighLevel Automation Systems</span>
        </h2>

        <p class="mt-6 text-gray-400 text-lg leading-8">
          Every business is different, so every automation should be too.
          I build scalable CRM systems, AI automations, sales funnels,
          appointment booking systems, email marketing workflows, and customer
          journeys that help businesses attract more leads, close more sales,
          and deliver exceptional customer experiences.
        </p>
      </div>

      <!-- Portfolio Cards -->
     <template>
  <section id="portfolio" class="py-24 bg-[#050505]">
    <div class="max-w-7xl mx-auto px-6">

      <!-- Header -->
      <div class="text-center mb-16">
        <span
          class="inline-flex items-center rounded-full border border-green-500/20 bg-green-500/10 px-4 py-2 text-green-400"
        >
          Portfolio
        </span>

        <h2 class="mt-6 text-5xl font-bold text-white">
          Featured
          <span class="text-green-500">Projects</span>
        </h2>

        <p class="mx-auto mt-6 max-w-3xl text-lg text-gray-400 leading-8">
          A collection of CRM systems, AI automation, websites, funnels and
          digital solutions built for businesses and organizations.
        </p>
      </div>

      <!-- Projects -->
      <div class="grid gap-8 md:grid-cols-2 xl:grid-cols-3">

        <div
          v-for="project in projects"
          :key="project.title"
          class="group flex flex-col rounded-3xl border border-green-500/20 bg-neutral-900 p-8 transition-all duration-500 hover:-translate-y-2 hover:border-green-500 hover:shadow-[0_20px_50px_rgba(34,197,94,.18)]"
        >

          <!-- Top -->
          <div class="flex items-center justify-between">

            <span class="text-sm font-semibold text-green-400">
              {{ project.category }}
            </span>

            <span
              class="rounded-full bg-green-500/10 px-4 py-1 text-xs font-medium text-green-400"
            >
              {{ project.status }}
            </span>

          </div>

          <!-- Title -->
          <h3
            class="mt-6 text-2xl font-bold text-white transition group-hover:text-green-400"
          >
            {{ project.title }}
          </h3>

          <!-- Description -->
          <p class="mt-5 flex-grow leading-7 text-gray-400">
            {{ project.description }}
          </p>

          <!-- Tags -->
          <div class="mt-8 flex flex-wrap gap-2">

            <span
              v-for="tag in project.tags"
              :key="tag"
              class="rounded-full bg-green-500/10 px-3 py-2 text-sm text-green-400"
            >
              {{ tag }}
            </span>

          </div>

          <!-- Button -->
          <NuxtLink
            :to="project.link"
            class="mt-10 flex items-center justify-center rounded-xl border border-green-500 py-3 font-semibold text-green-400 transition hover:bg-green-500 hover:text-black"
          >
            View Project →
          </NuxtLink>

        </div>

      </div>

    </div>
  </section>
</template>

      <!-- Statistics -->
      <div class="mt-24 grid gap-8 md:grid-cols-4">

        <div class="text-center">
          <h3 class="text-5xl font-bold text-green-500">50+</h3>
          <p class="mt-3 text-gray-400">Funnels & Websites Built</p>
        </div>

        <div class="text-center">
          <h3 class="text-5xl font-bold text-green-500">100+</h3>
          <p class="mt-3 text-gray-400">Automation Workflows</p>
        </div>

        <div class="text-center">
          <h3 class="text-5xl font-bold text-green-500">30+</h3>
          <p class="mt-3 text-gray-400">CRM Systems Deployed</p>
        </div>

        <div class="text-center">
          <h3 class="text-5xl font-bold text-green-500">24/7</h3>
          <p class="mt-3 text-gray-400">AI Customer Engagement</p>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: "Zikam Healthcare",
    category: "Healthcare CRM",
    status: "Completed",
    description:
      "Complete healthcare CRM with appointment booking, treatment pipelines, patient follow-ups, SMS, email automation and review requests.",
    tags: ["GoHighLevel", "CRM", "SMS", "Email"],
    link: "/health",
  },
  {
    title: "BeautyBoss Academy",
    category: "Funnels & Membership",
    status: "Live",
    description:
      "Membership platform with online courses, sales funnels, booking calendar, payment integration and client onboarding automation.",
    tags: ["Funnels", "Membership", "Automation", "Payments"],
    link: "/beautyboss",
  },
  {
    title: "AI Voice Receptionist",
    category: "AI Automation",
    status: "Featured",
    description:
      "AI-powered receptionist that answers calls, qualifies leads, books appointments and synchronizes customer data with GoHighLevel.",
    tags: ["Voice AI", "Chatbot", "CRM", "Booking"],
    link: "/ai",
  },
  {
    title: "GFud & Buka",
    category: "Restaurant Platform",
    status: "Live",
    description:
      "Modern restaurant website with online ordering, menu showcase, reservations and a responsive user experience.",
    tags: ["Nuxt 3", "Tailwind", "Restaurant", "Responsive"],
    link: "/gfud",
  },
  {
    title: "Clarion Concepts",
    category: "Corporate Website",
    status: "Completed",
    description:
      "Corporate website showcasing services, completed projects, company profile and contact management with a modern responsive design.",
    tags: ["Nuxt 3", "Tailwind", "Corporate", "SEO"],
    link: "/clarion",
  },
  {
    title: "SPE DSEAT",
    category: "Petroleum Society",
    status: "Live",
    description:
      "Official website for the Society of Petroleum Engineers featuring events, membership information, resources and industry updates.",
    tags: ["Nuxt 3", "Tailwind", "Petroleum", "Society"],
    link: "/spe",
  },
];
</script>