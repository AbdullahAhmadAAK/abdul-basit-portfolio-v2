<script>
  let dropdown1 = false;
  let dropdown2 = false;
</script>

<header class="bg-gray-800 text-white">
  <div class="container mx-auto flex justify-between items-center py-4 px-32">
     <!-- Logo -->
     <div class="logo text-xl font-bold">
        <a href="/" class="hover:text-gray-300">Logo</a>
     </div>

     <!-- Navigation -->
     <nav class="flex space-x-8">
        <!-- Regular Link -->
        <a href="#" class="hover:text-gray-300">Home</a>
        <a href="#" class="hover:text-gray-300">About</a>
        <a href="#" class="hover:text-gray-300">Services</a>
        <a href="#" class="hover:text-gray-300">Study Plans</a>
        <a href="#" class="hover:text-gray-300">Contact</a>
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
