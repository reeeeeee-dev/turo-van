<template>
  <div class="bg-green-smoke-50 min-h-screen flex flex-col">
    <!-- Hero Section -->
    <section class="relative overflow-hidden" style="height: calc(66.67vh + 6rem)">
      <div class="absolute inset-0">
        <img
          src="@/assets/van_hero.jpg"
          alt="Luxury Van in Northwest Arkansas"
          class="w-full h-full object-cover"
        />
      </div>

      <!-- Overlay -->
      <div class="absolute inset-0 bg-black/40"></div>

      <!-- Content -->
      <div class="relative h-full flex items-center justify-center">
        <div class="text-center text-white max-w-4xl mx-auto px-8">
          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6">About LuxZ Rentals</h1>
          <p class="text-xl md:text-2xl mb-8 text-green-smoke-200">
            Premium luxury vehicle rentals in the heart of Northwest Arkansas
          </p>
        </div>
      </div>
    </section>

    <!-- Company Story Section -->
    <section class="py-20 px-8 flex justify-center">
      <div class="max-w-6xl">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="flex flex-col gap-8">
            <h2 class="text-4xl font-bold text-green-smoke-950">Our Story</h2>
            <p class="text-lg text-green-smoke-700">
              Founded in the beautiful landscape of Northwest Arkansas, LuxZ Rentals was born from a
              passion for providing exceptional transportation experiences. We understand that every
              journey deserves to be extraordinary, whether you're exploring the Ozark Mountains,
              attending a business meeting in Bentonville, or celebrating a special occasion in
              Fayetteville.
            </p>
            <p class="text-lg text-green-smoke-700">
              Our commitment to luxury, reliability, and personalized service has made us the
              premier choice for discerning clients throughout the region. We believe that
              transportation should be more than just getting from point A to point B – it should be
              an experience that enhances your journey.
            </p>
          </div>
          <div class="relative">
            <img
              src="@/assets/van_gradient.png"
              alt="Luxury Van"
              class="w-full h-96 object-cover rounded-lg shadow-xl"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Northwest Arkansas Focus -->
    <section class="py-20 px-8 bg-green-smoke-100 flex justify-center">
      <div class="max-w-6xl flex flex-col gap-16">
        <div class="text-center items-center flex mb-16">
          <h2 class="text-4xl font-bold text-green-smoke-950 mb-6">
            Proudly Serving Northwest Arkansas
          </h2>
          <p class="text-xl text-green-smoke-700 max-w-3xl mx-auto">
            From the bustling business district of Bentonville to the vibrant cultural scene of
            Fayetteville, we're your trusted partner for luxury transportation throughout the
            region.
          </p>
        </div>

        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div class="text-center p-6 bg-white rounded-lg shadow-lg flex flex-col gap-4">
            <h3 class="text-2xl font-bold text-green-smoke-950">Bentonville</h3>
            <p class="text-green-smoke-700">
              Corporate transportation for Fortune 500 companies, executive meetings, and business
              events in the heart of Walmart's headquarters.
            </p>
          </div>

          <div class="text-center p-6 bg-white rounded-lg shadow-lg flex flex-col gap-4">
            <h3 class="text-2xl font-bold text-green-smoke-950">Fayetteville</h3>
            <p class="text-green-smoke-700">
              University events, cultural celebrations, and special occasions in Arkansas's most
              dynamic college town.
            </p>
          </div>

          <div class="text-center p-6 bg-white rounded-lg shadow-lg flex flex-col gap-4">
            <h3 class="text-2xl font-bold text-green-smoke-950">Rogers & Springdale</h3>
            <p class="text-green-smoke-700">
              Airport transfers, wedding transportation, and luxury travel for the growing
              communities of Northwest Arkansas.
            </p>
          </div>

          <div class="text-center p-6 bg-white rounded-lg shadow-lg flex flex-col gap-4">
            <h3 class="text-2xl font-bold text-green-smoke-950">Bella Vista</h3>
            <p class="text-green-smoke-700">
              Golf course transportation, resort transfers, and luxury travel for the premier
              golfing destination of Northwest Arkansas.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Values Section -->
    <section class="py-20 px-8 flex justify-center">
      <div class="max-w-6xl flex flex-col gap-16">
        <h2 class="text-4xl font-bold text-green-smoke-950 text-center">Our Values</h2>

        <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
          <div class="text-center flex flex-col items-center gap-4">
            <div class="w-16 h-16 bg-green-smoke-950 rounded-full flex items-center justify-center">
              <span class="text-white text-2xl">⭐</span>
            </div>
            <h3 class="text-xl font-bold text-green-smoke-950">Excellence</h3>
            <p class="text-green-smoke-700">
              We maintain the highest standards in every aspect of our service, from vehicle
              maintenance to customer care.
            </p>
          </div>

          <div class="text-center flex flex-col items-center gap-4">
            <div class="w-16 h-16 bg-green-smoke-950 rounded-full flex items-center justify-center">
              <span class="text-white text-2xl">🤝</span>
            </div>
            <h3 class="text-xl font-bold text-green-smoke-950">Trust</h3>
            <p class="text-green-smoke-700">
              Building lasting relationships through reliability, transparency, and consistent
              delivery of promises.
            </p>
          </div>

          <div class="text-center flex flex-col items-center gap-4">
            <div class="w-16 h-16 bg-green-smoke-950 rounded-full flex items-center justify-center">
              <span class="text-white text-2xl">🎯</span>
            </div>
            <h3 class="text-xl font-bold text-green-smoke-950">Precision</h3>
            <p class="text-green-smoke-700">
              Attention to detail in every interaction, ensuring flawless execution of your
              transportation needs.
            </p>
          </div>

          <div class="text-center flex flex-col items-center gap-4">
            <div class="w-16 h-16 bg-green-smoke-950 rounded-full flex items-center justify-center">
              <span class="text-white text-2xl">💎</span>
            </div>
            <h3 class="text-xl font-bold text-green-smoke-950">Luxury</h3>
            <p class="text-green-smoke-700">
              Providing premium experiences that exceed expectations and create memorable moments.
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Fleet Highlights -->
    <section class="py-20 px-8 bg-green-smoke-100 flex justify-center">
      <div class="max-w-6xl flex flex-col gap-16">
        <div class="text-center flex flex-col items-center gap-6">
          <h2 class="text-4xl font-bold text-green-smoke-950">Our Commitment</h2>
          <p class="text-xl text-green-smoke-700 max-w-3xl">
            We're dedicated to providing the finest luxury vehicles and exceptional service
            throughout Northwest Arkansas and beyond.
          </p>
        </div>

        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="flex flex-col gap-6">
            <h3 class="text-3xl font-bold text-green-smoke-950">Premium Fleet</h3>
            <ul class="flex flex-col gap-4 text-lg text-green-smoke-700">
              <li class="flex items-center gap-2">
                <span class="w-2 h-2 bg-green-smoke-950 rounded-full"></span>
                Latest model luxury vehicles maintained to perfection
              </li>
              <li class="flex items-center gap-2">
                <span class="w-2 h-2 bg-green-smoke-950 rounded-full"></span>
                Professional chauffeurs with extensive local knowledge
              </li>
              <li class="flex items-center gap-2">
                <span class="w-2 h-2 bg-green-smoke-950 rounded-full"></span>
                24/7 customer support and emergency assistance
              </li>
              <li class="flex items-center gap-2">
                <span class="w-2 h-2 bg-green-smoke-950 rounded-full"></span>
                Flexible booking options for any occasion
              </li>
            </ul>
          </div>

          <div class="relative">
            <img
              src="@/assets/cars.jpg"
              alt="Luxury Fleet"
              class="w-full h-96 object-cover rounded-lg shadow-xl"
            />
          </div>
        </div>
      </div>
    </section>

    <!-- Contact CTA -->
    <section class="py-20 px-8 flex justify-center">
      <div class="max-w-4xl text-center flex flex-col items-center gap-8">
        <h2 class="text-4xl font-bold text-green-smoke-950">Ready to Experience Luxury?</h2>
        <p class="text-xl text-green-smoke-700">
          Contact us today to book your premium transportation experience in Northwest Arkansas.
        </p>
        <div class="flex flex-col sm:flex-row gap-4 justify-center">
          <a
            href="https://turo.com"
            target="_blank"
            class="bg-green-smoke-950 text-green-smoke-50 px-8 py-4 rounded-lg text-lg font-semibold hover:bg-green-smoke-800 transition-colors"
          >
            Book Now
          </a>
          <a
            href="/vehicles"
            class="border-2 border-green-smoke-950 text-green-smoke-950 px-8 py-4 rounded-lg text-lg font-semibold hover:bg-green-smoke-950 hover:text-green-smoke-50 transition-colors"
          >
            View Fleet
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup>
// Component logic can be added here if needed
</script>

<style scoped>
/* Custom styles can be added here if needed */
</style>
