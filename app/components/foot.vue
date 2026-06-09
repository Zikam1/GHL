<template>
  <footer class="bg-white border-t border-gray-100">
    <div class="max-w-6xl mx-auto px-6 py-20">

      <!-- CTA BLOCK -->
      <div class="bg-gradient-to-r from-green-50 to-white border border-green-100 rounded-3xl p-10 text-center shadow-sm">

        <h2 class="text-3xl md:text-4xl font-semibold text-gray-900">
          Ready to get more clients consistently
          
        </h2>

        <p class="mt-4 text-gray-600 max-w-xl mx-auto">
          Let’s build a system that brings you leads and closes clients on autopilot using GoHighLevel.
        </p>

        <!-- MAIN CTA (FIVERR) -->
        <a 
          href="https://www.fiverr.com/zikam10/design-and-build-websites-funnels-and-landing-pages-using-gohighlevel?context_referrer=tailored_homepage_perseus&source=recently_viewed_gigs&ref_ctx_id=a43f2d01823a4be88112d5969f445f72&context=recommendation&pckg_id=1&pos=1&context_alg=recently_viewed&seller_online=true&imp_id=8c55f3e5-2967-404e-9202-dd29db0f3b66"
          target="_blank"
          class="inline-block mt-6 bg-green-600 text-white px-8 py-4 rounded-xl font-medium hover:scale-105 transition"
        >
          Start Your Project
        </a>

      </div>

      <!-- MAIN FOOTER -->
      <div class="mt-16 grid md:grid-cols-3 gap-10 text-sm">

        <!-- BRAND -->
        <div>
          <h3 class="text-xl font-semibold text-gray-900">
            Aku Isaac
          </h3>

          <p class="mt-3 text-gray-600 leading-relaxed">
            I design high-converting funnels, automation systems, and CRM setups that help businesses scale faster with less manual work.
          </p>

          <p class="mt-4 text-green-600 font-medium text-sm">
            GoHighLevel Funnel & Automation Expert
          </p>
        </div>

        <!-- SERVICES -->
        <div>
          <h4 class="font-semibold text-gray-900 mb-4">
            What You Get
          </h4>

          <ul class="space-y-3 text-gray-600">
            <li>✔ High-converting funnels</li>
            <li>✔ Automated follow-ups</li>
            <li>✔ CRM pipeline setup</li>
            <li>✔ Lead tracking system</li>
          </ul>
        </div>

        <!-- CONTACT -->
        <div>
          <h4 class="font-semibold text-gray-900 mb-4">
            Contact
          </h4>

          <div class="space-y-3 text-gray-600">

            <!-- WHATSAPP NUMBER -->
            <a
  href="https://wa.me/2348104233630"
  target="_blank"
  class="inline-flex items-center justify-center px-4 py-3 rounded-xl bg-green-100 text-green-700 font-semibold border border-green-200 hover:bg-green-200 transition"
>
  Send a Message on WhatsApp
</a>

            <p>
              <a 
                href="mailto:isaacaku67@gmail.com" 
                class="hover:text-green-600 transition"
              >
                isaacaku67@gmail.com
              </a>
            </p>

            <p>
              <a 
                href="https://www.linkedin.com/in/isaac-aku-57a711177" 
                target="_blank"
                class="hover:text-green-600 transition"
              >
                LinkedIn Profile
              </a>
            </p>

            <!-- SECOND CTA -->
            <a 
              href="https://www.fiverr.com/zikam10/design-and-build-websites-funnels-and-landing-pages-using-gohighlevel?context_referrer=tailored_homepage_perseus&source=recently_viewed_gigs&ref_ctx_id=a43f2d01823a4be88112d5969f445f72&context=recommendation&pckg_id=1&pos=1&context_alg=recently_viewed&seller_online=true&imp_id=8c55f3e5-2967-404e-9202-dd29db0f3b66"
              target="_blank"
              class="inline-block mt-3 text-green-600 font-medium hover:underline"
            >
              Available for new projects →
            </a>

          </div>
        </div>

      </div>

      <!-- BOTTOM -->
      <div class="mt-16 pt-6 border-t text-center text-xs text-gray-400">
        © {{ year }} Aku Isaac. Built for results.
      </div>

    </div>
  </footer>
</template>

<script setup>
const year = new Date().getFullYear()
</script>