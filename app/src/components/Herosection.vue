<template>
  <div class="font-['Poppins']">
    <!-- <nav class="fixed top-0 left-0 right-0 z-50 bg-transparent">
      <div class="max-w-8xl mx-auto px-6 py-4">
        <div class="flex items-center justify-between">
          <a href="#" class="flex items-center space-x-3">
            <img
              src="https://ai-public.creatie.ai/gen_page/logo_placeholder.png"
              alt="Logo"
              class="h-10"
            />
            <span class="text-white font-semibold text-xl">Brand</span>
          </a>
          <div class="hidden md:flex items-center space-x-8">
            <a href="#" class="text-white hover:text-gray-200">Home</a>
            <a href="#" class="text-white hover:text-gray-200">About</a>
            <a href="#" class="text-white hover:text-gray-200">Services</a>
            <a href="#" class="text-white hover:text-gray-200">Contact</a>
            <button
              class="!rounded-button bg-white text-custom px-6 py-2 font-medium"
            >
              Get Started
            </button>
          </div>
        </div>
      </div>
    </nav> -->

    <div class="glide h-screen relative">
      <div class="glide__track h-full" data-glide-el="track">
        <ul class="glide__slides h-full">
          <li class="glide__slide">
            <div class="h-full relative">
              <img
                src="../assets/IMG/blog-image-10.jpg"
                class="w-full h-full object-cover"
                alt="Slide 1"
              />
              <div class="absolute inset-0 bg-black bg-opacity-40"></div>
            </div>
          </li>
          <li class="glide__slide">
            <div class="h-full relative">
              <img
                src="../assets/IMG/blog-image-10.jpg"
                class="w-full h-full object-cover"
                alt="Slide 2"
              />
              <div class="absolute inset-0 bg-black bg-opacity-40"></div>
            </div>
          </li>
          <li class="glide__slide">
            <div class="h-full relative">
              <img
                src="../assets/IMG/blog-image-10.jpg"
                class="w-full h-full object-cover"
                alt="Slide 3"
              />
              <div class="absolute inset-0 bg-black bg-opacity-40"></div>
            </div>
          </li>
        </ul>
      </div>

      <div
        class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-center z-10 w-full max-w-4xl px-6"
      >
        <div
          id="typed-text"
          class="text-white text-5xl font-bold mb-8 h-20"
        ></div>
        <p class="text-white text-xl mb-12 opacity-90">
          Discover innovative solutions for your business needs with our
          cutting-edge technology and expert team.
        </p>
        <div class="flex items-center justify-center space-x-6">
          <button
            class="!rounded-button bg-custom text-white px-8 py-3 font-semibold text-lg hover:bg-opacity-90 transition-all"
          >
            Get Started Now
          </button>
          <button
            class="!rounded-button border-2 border-white text-white px-8 py-3 font-semibold text-lg hover:bg-white hover:text-custom transition-all"
          >
            Learn More
          </button>
        </div>
      </div>

      <div
        class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-20"
        data-glide-el="controls[nav]"
      >
        <div class="flex space-x-3">
          <button
            class="w-3 h-3 rounded-full bg-white bg-opacity-50 focus:outline-none"
            data-glide-dir="=0"
          ></button>
          <button
            class="w-3 h-3 rounded-full bg-white bg-opacity-50 focus:outline-none"
            data-glide-dir="=1"
          ></button>
          <button
            class="w-3 h-3 rounded-full bg-white bg-opacity-50 focus:outline-none"
            data-glide-dir="=2"
          ></button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";
import Typed from "typed.js";
import Glide from "@glidejs/glide";


let glideInstance = null;

const typedElement = ref(null);
let typedInstance = null;

onMounted(() => {
  glideInstance = new Glide(".glide", {
    type: "carousel",
    autoplay: 5000,
    animationDuration: 1000,
    gap: 0,
    perView: 1,
  });

  glideInstance.mount();
});

onUnmounted(() => {
  if (glideInstance) {
    glideInstance.destroy(); // Cleanup when component unmounts
  }
});

onMounted(() => {
  typedInstance = new Typed(typedElement.value, {
    strings: [
      "Transform Your Business",
      "Innovate with Confidence",
      "Build the Future Today",
    ],
    typeSpeed: 50,
    backSpeed: 30,
    backDelay: 2000,
    loop: true,
  });
});

onUnmounted(() => {
  if (typedInstance) {
    typedInstance.destroy(); // Clean up when component unmounts
  }
});
// new Glide(".glide", {
//   type: "carousel",
//   autoplay: 5000,
//   animationDuration: 1000,
//   gap: 0,
//   perView: 1,
// }).mount();

// new Typed("#typed-text", {
//   strings: [
//     "Transform Your Business",
//     "Innovate with Confidence",
//     "Build the Future Today",
//   ],
//   typeSpeed: 50,
//   backSpeed: 30,
//   backDelay: 2000,
//   loop: true,
// });
</script>

<style lang="scss" scoped></style>
