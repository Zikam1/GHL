<template>
  <section id="testimonials" class="relative py-28 bg-white overflow-hidden">

    <!-- Background Glow -->
    <div class="absolute top-0 left-0 w-96 h-96 bg-green-100 blur-[120px] rounded-full"></div>
    <div class="absolute bottom-0 right-0 w-96 h-96 bg-emerald-100 blur-[120px] rounded-full"></div>

    <div class="relative max-w-7xl mx-auto px-6">

      <!-- Heading -->
      <div class="text-center mb-20">
        <span
          class="inline-flex items-center px-4 py-2 rounded-full border border-green-200 bg-green-50 text-green-700 text-sm font-medium">
          ⭐ Trusted By Growing Businesses
        </span>

        <h2 class="mt-6 text-3xl font-bold text-gray-900">
          Real Results. Real Businesses.
        </h2>

        <p class="mt-5 text-gray-600 text-sm max-w-3xl mx-auto">
          Businesses are leveraging GoHighLevel automation, CRM systems, and funnels
          to save time, generate more leads, and increase revenue.
        </p>
      </div>

      <!-- Testimonials -->
      <div class="grid lg:grid-cols-3 md:grid-cols-2 gap-8">

        <div
          v-for="(item, index) in testimonials"
          :key="index"
          :class="item.featured
            ? 'rounded-3xl p-[1px] bg-gradient-to-r from-green-400 to-emerald-500'
            : 'group bg-white border border-gray-200 rounded-3xl p-8 shadow-sm hover:shadow-xl transition-all duration-300 hover:-translate-y-2'">

          <div
            :class="item.featured
              ? 'bg-white rounded-3xl p-8 h-full shadow-xl'
              : ''">

            <div
              v-if="item.featured"
              class="inline-flex px-3 py-1 rounded-full bg-green-50 text-green-700 text-xs mb-6">
              ⭐ MOST IMPACTFUL RESULT
            </div>

            <div class="text-green-500 text-4xl mb-6">
              ❝
            </div>

            <p
              :class="item.featured
                ? 'text-gray-700 text-lg leading-relaxed'
                : 'text-gray-600 leading-relaxed'">
              {{ item.text }}
            </p>

            <div class="mt-8 flex items-center gap-4">

              <div
                class="w-14 h-14 rounded-full bg-green-100 flex items-center justify-center font-bold text-green-700">
                {{ item.initials }}
              </div>

              <div>
                <h4 class="font-semibold text-gray-900">
                  {{ item.name }}
                </h4>

                <p class="text-sm text-gray-500">
                  {{ item.role }}
                </p>
              </div>

            </div>

          </div>

        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    initials: "SJ",
    name: "Sarah Johnson",
    role: "Real Estate Consultant",
    text: "The automation workflows eliminated hours of manual follow-up every week. We now close more leads without adding more staff."
  },
  {
    initials: "MT",
    name: "Michael Thompson",
    role: "Marketing Agency Owner",
    text: "Within 5 days, our appointment bookings doubled after implementing our funnel and CRM automation. Everything now runs on autopilot.",
    featured: true
  },
  {
    initials: "DW",
    name: "David Williams",
    role: "Fitness Business Owner",
    text: "The SMS and email automation campaigns continue nurturing leads around the clock, helping us increase conversions consistently."
  },
  {
    initials: "ER",
    name: "Emily Roberts",
    role: "Beauty Salon Owner",
    text: "Automated booking reminders reduced no-shows and helped us keep our calendar full every week."
  },
  {
    initials: "JC",
    name: "James Carter",
    role: "Dental Clinic",
    text: "Our team now spends less time chasing patients because every follow-up is handled automatically."
  },
  {
    initials: "LB",
    name: "Lisa Brown",
    role: "Business Coach",
    text: "The CRM keeps every lead organized, while the sales funnels generate appointments every day."
  },
  {
    initials: "RN",
    name: "Robert Nelson",
    role: "Roofing Company",
    text: "We respond to new leads in minutes instead of hours, which has significantly increased our closing rate."
  },
  {
    initials: "AG",
    name: "Amanda Green",
    role: "Medical Spa Owner",
    text: "Our email and SMS campaigns consistently bring inactive clients back, increasing monthly revenue."
  },
  {
    initials: "PH",
    name: "Peter Harris",
    role: "Cleaning Service Owner",
    text: "From lead capture to appointment booking, everything runs automatically, allowing us to focus on serving clients."
  }
];
</script>