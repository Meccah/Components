<template>
  <div class="font-[Poppins]">
    <div class="bg-teal-500 relative">
      <div class="max-w-8xl mx-auto">
        <div
          class="flex justify-between items-center py-2 px-6 text-sm text-gray-600 border-b border-gray-100"
        >
          <div class="flex  items-center space-x-4 bg-teal-500">
            <div class="flex items-center">
              <img src="../assets/logo.svg" class="h-6" alt="" />
              <span>New York, NY</span>
            </div>
            <div class="flex items-center">
              <i class="fas fa-phone mr-2"></i>
              <span>+1 (555) 123-4567</span>
            </div>
          </div> 
          <div class="flex justify-end items-center space-x-3">
          <a href="https://www.youtube.com" target="_blank"
            ><img src="../assets/icons8-youtube.svg" class="h-6" alt=""
          /></a>
          <a href="https://twitter.com" target="_blank"
            ><img src="../assets/icons8-twitter.svg" class="h-6" alt=""
          /></a>
          <a href="https://www.linkedin.com" target="_blank"
            ><img src="../assets/icons8-linked-in.svg" class="h-6" alt=""
          /></a>
        </div>
        </div>
       
      </div>
    </div>
    <nav class="relative bg-gray-50 mb-5">
      <div class="max-w-8xl mx-auto px-6">
        <div class="flex items-center justify-between py-6">
          <div class="w-48">
            <img
              src="https://ai-public.creatie.ai/gen_page/logo_placeholder.png"
              alt="Logo"
              class="w-full"
            />
          </div>

          <div class="flex flex-col items-start space-y-4">
            <a
              href="#"
              class="text-gray-800 hover:text-custom transition-colors"
              >Home</a
            >
            <a
              href="#"
              class="text-gray-800 hover:text-custom transition-colors"
              >Products</a
            >
            <a
              href="#"
              class="text-gray-800 hover:text-custom transition-colors"
              >Contact</a
            >
          </div>
          <div class="flex items-center space-x-4">
            <button
              class="!rounded-button px-6 py-2 border border-custom bg-custom hover:text-white transition-colors"
            >
              Log In
            </button>
            <button
              class="!rounded-button px-6 py-2 border border-custom bg-custom hover:bg-opacity-90 transition-colors"
            >
              Sign Up
            </button>
          </div>
        </div>
      </div>

      <!-- <div class="absolute bottom-0 left-0 w-full overflow-hidden -mb-1">
          <svg viewBox="0 0 1440 120" fill="none" xmlns="http://www.w3.org/2000/svg" class="w-full h-16">
              <path fill="#f9fafb" d="M0,0 C240,95 480,120 720,120 C960,120 1200,95 1440,0 L1440,120 L0,120 Z" style="fill: white"></path>
          </svg>
      </div> -->
    </nav>
    <main class="bg-gray-900 h-2"></main>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped></style>
