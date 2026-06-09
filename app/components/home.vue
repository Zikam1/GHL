<template>
  <div class="bg-white text-gray-900 overflow-x-hidden">

    <!-- HERO -->
    <section class="min-h-screen flex items-center px-6 py-24">
      <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-16 items-center">

        <!-- LEFT -->
        <div>
          <p class="uppercase tracking-widest text-sm mb-6 text-green-600 font-semibold">
            Funnel Builder • Automation Expert
          </p>

          <h1 class="text-5xl md:text-7xl font-bold leading-tight mb-8">
            I Build Systems That
            <span class="text-green-600">Print Clients</span>
            For Your Business
          </h1>

          <p class="text-gray-600 text-xl mb-10 max-w-xl leading-relaxed">
            I help businesses generate consistent leads and close more deals using high-converting funnels, automation, and CRM systems powered by GoHighLevel.
          </p>

          <div class="flex flex-col sm:flex-row gap-5">
            <a href="#booking" class="bg-green-600 text-white px-10 py-5 rounded-xl text-lg font-semibold hover:bg-green-500 transition shadow-lg">
              Book Free Strategy Call
            </a>

            <a href="#services" class="border-2 border-gray-300 px-10 py-5 rounded-xl text-lg hover:border-black transition">
              See How It Works
            </a>
          </div>

          <!-- TRUST -->
          <div class="mt-10 text-sm text-gray-500">
            Funnels • Automation • CRM • Lead Generation • SMS Marketing
          </div>
        </div>

        <!-- RIGHT IMAGE -->
        <div class="flex justify-center relative">
          <div class="absolute w-72 h-72 bg-green-500/20 blur-3xl rounded-full"></div>

          <img
            src="/assets/picccture.png"
            class="relative w-[380px] md:w-[450px] rounded-2xl border border-gray-200 shadow-2xl"
          />
        </div>

      </div>
    </section>
 
    <!-- SOCIAL PROOF -->
    <section class="py-20 bg-gray-50 text-center">
      <h2 class="text-3xl font-bold mb-6">Trusted Systems That Deliver Results</h2>
      <p class="text-gray-600 max-w-2xl mx-auto text-lg">
        My systems are built to automate your growth bringing in leads, nurturing them, and converting them into paying clients without manual effort.
      </p>
    </section>
<services />
    
 <booking />
    <process />
     

<why />



  </div>
</template>


<script setup>

const year = new Date().getFullYear()

</script>