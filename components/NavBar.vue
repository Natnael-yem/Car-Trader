<template>
  <header
    class="
      sticky
      top-0
      z-50
      flex
      justify-between
      items-center
      space-x-1
      border-b
      bg-white
      p-4
      shadow-md
    "
  >
    <NuxtLink class="text-3xl font-mono" to="/">Car Trader</NuxtLink>
    <div class="hidden sm:ml-6 sm:block">
          <div class="flex space-x-4">
            <CarSearchBar />
            <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
            <NuxtLink  to="/login" class="bg-gray-900 text-white rounded-md px-3 py-2 text-sm font-medium" aria-current="page">Login</NuxtLink> 
            
            
            <NuxtLink to="/register"  class="text-gray-300 hover:bg-gray-700 hover:text-white rounded-md px-3 py-2 text-sm font-medium">Register</NuxtLink>
            
          </div>
        </div>
  </header>
</template>


