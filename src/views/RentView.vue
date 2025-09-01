<template>
  <div class="py-8 min-h-screen bg-gradient-to-br from-gray-50 to-blue-100">
    <div class="max-w-7xl mx-auto px-4">
      <h1 class="text-center text-gray-800 mb-2 text-4xl font-bold md:text-5xl">
        Rent a Vehicle
      </h1>
      <p class="text-center text-gray-600 mb-12 text-lg">
        Book your perfect vehicle for your next adventure
      </p>

      <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mt-8">
        <div class="lg:col-span-2 bg-white p-8 rounded-2xl shadow-lg">
          <h2 class="text-gray-800 mb-6 text-2xl font-semibold">Booking Details</h2>

          <form @submit.prevent="handleSubmit" class="space-y-6">
            <div class="flex flex-col gap-2">
              <label for="vehicle-type" class="text-gray-700 font-medium text-sm">
                Vehicle Type
              </label>
              <select
                id="vehicle-type"
                v-model="booking.vehicleType"
                required
                class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
              >
                <option value="">Select a vehicle</option>
                <option value="camper-van">Camper Van</option>
                <option value="suv">SUV</option>
                <option value="sports-car">Sports Car</option>
              </select>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
              <div class="flex flex-col gap-2">
                <label for="pickup-date" class="text-gray-700 font-medium text-sm">
                  Pickup Date
                </label>
                <input
                  type="date"
                  id="pickup-date"
                  v-model="booking.pickupDate"
                  required
                  :min="today"
                  class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
                />
              </div>

              <div class="flex flex-col gap-2">
                <label for="return-date" class="text-gray-700 font-medium text-sm">
                  Return Date
                </label>
                <input
                  type="date"
                  id="return-date"
                  v-model="booking.returnDate"
                  required
                  :min="booking.pickupDate || today"
                  class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
                />
              </div>
            </div>

            <div class="flex flex-col gap-2">
              <label for="pickup-location" class="text-gray-700 font-medium text-sm">
                Pickup Location
              </label>
              <input
                type="text"
                id="pickup-location"
                v-model="booking.pickupLocation"
                placeholder="Enter pickup location"
                required
                class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
              />
            </div>

            <div class="flex flex-col gap-2">
              <label for="name" class="text-gray-700 font-medium text-sm">
                Full Name
              </label>
              <input
                type="text"
                id="name"
                v-model="booking.name"
                placeholder="Enter your full name"
                required
                class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
              />
            </div>

            <div class="flex flex-col gap-2">
              <label for="email" class="text-gray-700 font-medium text-sm">
                Email
              </label>
              <input
                type="email"
                id="email"
                v-model="booking.email"
                placeholder="Enter your email"
                required
                class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
              />
            </div>

            <div class="flex flex-col gap-2">
              <label for="phone" class="text-gray-700 font-medium text-sm">
                Phone Number
              </label>
              <input
                type="tel"
                id="phone"
                v-model="booking.phone"
                placeholder="Enter your phone number"
                required
                class="p-3 border-2 border-gray-200 rounded-lg text-base transition-colors focus:outline-none focus:border-indigo-500"
              />
            </div>

            <button
              type="submit"
              :disabled="isSubmitting"
              class="w-full bg-gradient-to-r from-red-400 to-orange-500 text-white font-semibold py-4 px-8 rounded-full text-lg transition-all duration-300 hover:-translate-y-1 hover:shadow-lg disabled:opacity-70 disabled:cursor-not-allowed"
            >
              {{ isSubmitting ? 'Processing...' : 'Book Now' }}
            </button>
          </form>
        </div>

        <div class="bg-white p-8 rounded-2xl shadow-lg h-fit lg:sticky lg:top-24">
          <h2 class="text-gray-800 mb-6 text-2xl font-semibold">Booking Summary</h2>
          <div class="bg-gray-50 p-6 rounded-xl">
            <div
              v-if="booking.vehicleType"
              class="flex justify-between items-center py-3 border-b border-gray-200"
            >
              <span class="text-gray-600 font-medium">Vehicle:</span>
              <span class="text-gray-800 font-semibold">{{ getVehicleName(booking.vehicleType) }}</span>
            </div>
            <div
              v-if="booking.pickupDate"
              class="flex justify-between items-center py-3 border-b border-gray-200"
            >
              <span class="text-gray-600 font-medium">Pickup:</span>
              <span class="text-gray-800 font-semibold">{{ formatDate(booking.pickupDate) }}</span>
            </div>
            <div
              v-if="booking.returnDate"
              class="flex justify-between items-center py-3 border-b border-gray-200"
            >
              <span class="text-gray-600 font-medium">Return:</span>
              <span class="text-gray-800 font-semibold">{{ formatDate(booking.returnDate) }}</span>
            </div>
            <div
              v-if="booking.pickupLocation"
              class="flex justify-between items-center py-3 border-b border-gray-200"
            >
              <span class="text-gray-600 font-medium">Location:</span>
              <span class="text-gray-800 font-semibold">{{ booking.pickupLocation }}</span>
            </div>

            <div
              v-if="booking.vehicleType && booking.pickupDate && booking.returnDate"
              class="mt-6 pt-6 border-t-2 border-gray-200 text-center"
            >
              <h3 class="text-gray-800 mb-2 text-lg font-semibold">Estimated Price</h3>
              <div class="text-3xl font-bold text-red-500 mb-2">${{ calculatePrice() }}</div>
              <small class="text-gray-500 text-sm">Price may vary based on availability and season</small>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'

const booking = ref({
  vehicleType: '',
  pickupDate: '',
  returnDate: '',
  pickupLocation: '',
  name: '',
  email: '',
  phone: '',
})

const isSubmitting = ref(false)

const today = computed(() => {
  const date = new Date()
  return date.toISOString().split('T')[0]
})

const vehiclePrices = {
  'camper-van': 150,
  suv: 100,
  'sports-car': 200,
}

const getVehicleName = (type) => {
  const names = {
    'camper-van': 'Camper Van',
    suv: 'SUV',
    'sports-car': 'Sports Car',
  }
  return names[type] || type
}

const formatDate = (dateString) => {
  return new Date(dateString).toLocaleDateString('en-US', {
    weekday: 'short',
    year: 'numeric',
    month: 'short',
    day: 'numeric',
  })
}

const calculatePrice = () => {
  if (!booking.value.vehicleType || !booking.value.pickupDate || !booking.value.returnDate) {
    return 0
  }

  const start = new Date(booking.value.pickupDate)
  const end = new Date(booking.value.returnDate)
  const days = Math.ceil((end - start) / (1000 * 60 * 60 * 24))

  if (days <= 0) return 0

  const basePrice = vehiclePrices[booking.value.vehicleType] || 0
  return (basePrice * days).toFixed(2)
}

const handleSubmit = async () => {
  isSubmitting.value = true

  // Simulate API call
  await new Promise((resolve) => setTimeout(resolve, 2000))

  alert('Booking submitted successfully! We will contact you shortly.')
  isSubmitting.value = false

  // Reset form
  booking.value = {
    vehicleType: '',
    pickupDate: '',
    returnDate: '',
    pickupLocation: '',
    name: '',
    email: '',
    phone: '',
  }
}
</script>
