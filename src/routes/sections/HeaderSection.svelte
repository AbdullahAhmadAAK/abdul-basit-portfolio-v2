<script>
  let dropdown1 = false;
  let dropdown2 = false;
</script>

<header class="bg-gray-800 text-white">
  <div class="container mx-auto flex justify-between items-center py-4 px-32">
    <!-- Logo -->
    <div class="mb-6 md:mb-0 bg-gray-800">
      <img src="/abdul-basit-logo.jpg" alt="Logo of Abdul Basit Pawar, math tutor and entrepreneur" class="h-24 w-auto" />
    </div>
    <!-- Navigation -->
    <nav class="flex space-x-8">
      <!-- Regular Link -->
      <a href="#home" class="hover:text-gray-300 font-extrabold">Home</a>
      <a href="#about" class="hover:text-gray-300 font-extrabold">About</a>
      <a href="#qualification" class="hover:text-gray-300 font-extrabold"
        >Qualifications</a
      >
      <a href="#study-plans" class="hover:text-gray-300 font-extrabold"
        >Study Plans</a
      >
      <!-- Dropdown 1 -->
      <!-- <div class="relative">
           <button on:mouseover={() => (dropdown1 = true)} on:mouseleave={() => (dropdown1 = false)} class="hover:text-gray-300">
              Sections
           </button>
           {#if dropdown1}
              <ul class="absolute bg-white text-black mt-2 p-2 rounded shadow-lg" on:mouseover={() => (dropdown1 = true)} on:mouseleave={() => (dropdown1 = false)}>
                 <li><a href="#" class="block px-4 py-2 hover:bg-gray-200">Dropdown Item 1</a></li>
                 <li><a href="#" class="block px-4 py-2 hover:bg-gray-200">Dropdown Item 2</a></li>
              </ul>
           {/if}
        </div> -->

      <!-- Dropdown 2 -->
      <!-- <div class="relative">
           <button on:mouseover={() => (dropdown2 = true)} on:mouseleave={() => (dropdown2 = false)} class="hover:text-gray-300">
              More
           </button>
           {#if dropdown2}
              <ul class="absolute bg-white text-black mt-2 p-2 rounded shadow-lg" on:mouseover={() => (dropdown2 = true)} on:mouseleave={() => (dropdown2 = false)}>
                 <li><a href="#" class="block px-4 py-2 hover:bg-gray-200">Dropdown Item 1</a></li>
                 <li><a href="#" class="block px-4 py-2 hover:bg-gray-200">Dropdown Item 2</a></li>
              </ul>
           {/if}
        </div> -->

      <!-- Regular Link -->
      <!-- <a href="#" class="hover:text-gray-300">Link 2</a> -->
    </nav>
  </div>
</header>
