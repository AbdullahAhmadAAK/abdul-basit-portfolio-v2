<script>
  import {sectionHorizontalPadding} from '../../lib/styles'
  let dropdown1 = false;
  let dropdown2 = false;
</script>

<header class="bg-gray-800 text-white">
  <div class="container mx-auto {sectionHorizontalPadding} py-4 flex items-center justify-between">
    <!-- Logo -->
    <div class="mb-4 md:mb-0">
      <img src="/abdul-basit-logo.jpg" alt="Logo of Abdul Basit Pawar, math tutor and entrepreneur" class="h-16 w-auto md:h-24" />
    </div>
    <!-- Navigation -->
    <nav class="md:w-auto flex flex-col md:flex-row md:space-x-8 items-center">
      <!-- Mobile Menu Button -->
      <button class="md:hidden text-white focus:outline-none" onclick="document.getElementById('mobile-menu').classList.toggle('hidden')">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path>
        </svg>
      </button>

      <!-- Desktop Links -->
      <div class="hidden md:flex md:space-x-8">
        <a href="#home" class="hover:text-gray-300 font-extrabold">Home</a>
        <a href="#about" class="hover:text-gray-300 font-extrabold">About</a>
        <a href="#qualification" class="hover:text-gray-300 font-extrabold">Qualifications</a>
        <a href="#study-plans" class="hover:text-gray-300 font-extrabold">Study Plans</a>
      </div>

      <!-- Mobile Menu -->
      <div id="mobile-menu" class="absolute top-24 left-0 w-full text-center bg-gray-800 text-white hidden md:hidden">
        <a href="#home" class="block px-4 py-2 hover:bg-gray-700">Home</a>
        <a href="#about" class="block px-4 py-2 hover:bg-gray-700">About</a>
        <a href="#qualification" class="block px-4 py-2 hover:bg-gray-700">Qualifications</a>
        <a href="#study-plans" class="block px-4 py-2 hover:bg-gray-700">Study Plans</a>
      </div>
    </nav>
  </div>
</header>
