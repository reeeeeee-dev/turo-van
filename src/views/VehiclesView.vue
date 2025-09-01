<template>
  <div class="py-8 min-h-screen bg-gradient-to-br from-gray-50 to-blue-100">
    <div class="max-w-7xl mx-auto px-4">
      <h1 class="text-center text-gray-800 mb-2 text-4xl font-bold md:text-5xl">
        Our Vehicles
      </h1>
      <p class="text-center text-gray-600 mb-12 text-lg">
        Discover our fleet of premium vehicles available for rent.
      </p>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mt-8">
        <div class="bg-white rounded-2xl overflow-hidden shadow-lg hover:-translate-y-2 hover:shadow-2xl transition-all duration-300">
          <div class="h-48 bg-gradient-to-r from-indigo-500 to-purple-600 flex items-center justify-center">
            <div class="text-6xl">🚐</div>
          </div>
          <div class="p-6">
            <h3 class="text-gray-800 mb-2 text-xl font-semibold">Camper Van</h3>
            <p class="text-gray-600 mb-4">Perfect for road trips and camping adventures</p>
            <div class="flex gap-2 mb-6 flex-wrap">
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Sleeps 4
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Kitchen
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Bathroom
              </span>
            </div>
            <button class="w-full bg-gradient-to-r from-red-400 to-orange-500 text-white font-semibold py-3 px-6 rounded-full hover:-translate-y-1 hover:shadow-lg transition-all duration-300">
              Rent Now
            </button>
          </div>
        </div>

        <div class="bg-white rounded-2xl overflow-hidden shadow-lg hover:-translate-y-2 hover:shadow-2xl transition-all duration-300">
          <div class="h-48 bg-gradient-to-r from-indigo-500 to-purple-600 flex items-center justify-center">
            <div class="text-6xl">🚙</div>
          </div>
          <div class="p-6">
            <h3 class="text-gray-800 mb-2 text-xl font-semibold">SUV</h3>
            <p class="text-gray-600 mb-4">Comfortable and spacious for family trips</p>
            <div class="flex gap-2 mb-6 flex-wrap">
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                7 Seats
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                AWD
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Luggage Space
              </span>
            </div>
            <button class="w-full bg-gradient-to-r from-red-400 to-orange-500 text-white font-semibold py-3 px-6 rounded-full hover:-translate-y-1 hover:shadow-lg transition-all duration-300">
              Rent Now
            </button>
          </div>
        </div>

        <div class="bg-white rounded-2xl overflow-hidden shadow-lg hover:-translate-y-2 hover:shadow-2xl transition-all duration-300">
          <div class="h-48 bg-gradient-to-r from-indigo-500 to-purple-600 flex items-center justify-center">
            <div class="text-6xl">🏎️</div>
          </div>
          <div class="p-6">
            <h3 class="text-gray-800 mb-2 text-xl font-semibold">Sports Car</h3>
            <p class="text-gray-600 mb-4">Experience the thrill of high-performance driving</p>
            <div class="flex gap-2 mb-6 flex-wrap">
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                2 Seats
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Convertible
              </span>
              <span class="bg-blue-50 text-blue-600 px-3 py-1 rounded-full text-sm font-medium">
                Premium
              </span>
            </div>
            <button class="w-full bg-gradient-to-r from-red-400 to-orange-500 text-white font-semibold py-3 px-6 rounded-full hover:-translate-y-1 hover:shadow-lg transition-all duration-300">
              Rent Now
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
