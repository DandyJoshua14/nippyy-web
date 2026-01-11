<script>
    import { slide } from 'svelte/transition';
    
    let isMobileMenuOpen = false;
    /**
	 * @type {string | null}
	 */
    let activeDropdown = null; // Tracks which dropdown is open on mobile
  
    function toggleMobileMenu() {
      isMobileMenuOpen = !isMobileMenuOpen;
    }
  
    /**
	 * @param {string | null} name
	 */
    function toggleDropdown(name) {
      activeDropdown = activeDropdown === name ? null : name;
    }
  </script>
  
  <div class="relative z-50 bg-white border-b border-slate-50">
    <nav class="flex items-center justify-between px-6 py-4 max-w-7xl mx-auto">
      <div class="flex-shrink-0">
        <img src="/logo.png" alt="Nippyy Logo" class="h-8" />
      </div>
  
      <div class="hidden md:flex items-center gap-10 text-[15px] font-medium text-slate-800">
        <div class="relative group cursor-pointer">
          <div class="flex items-center gap-1 hover:text-black transition py-2">
            Company
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 opacity-70 transition-transform group-hover:rotate-180" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </div>
          <div class="absolute left-0 top-full hidden group-hover:block pt-2 w-48 transition-all">
            <div class="bg-white border border-slate-100 rounded-xl shadow-xl py-2 overflow-hidden">
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 1</a>
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 2</a>
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 3</a>
            </div>
          </div>
        </div>
  
        <div class="relative group cursor-pointer">
          <div class="flex items-center gap-1 hover:text-black transition py-2">
            Products
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 opacity-70 transition-transform group-hover:rotate-180" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
            </svg>
          </div>
          <div class="absolute left-0 top-full hidden group-hover:block pt-2 w-48 transition-all">
            <div class="bg-white border border-slate-100 rounded-xl shadow-xl py-2 overflow-hidden">
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 1</a>
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 2</a>
              <a href="#" class="block px-4 py-2 hover:bg-slate-50 hover:text-cyan-600 transition">Item 3</a>
            </div>
          </div>
        </div>
  
        <a href="#support" class="hover:text-black transition">Support</a>
      </div>
  
      <div class="hidden md:flex items-center gap-8">
        <button class="text-[15px] font-medium text-slate-800 hover:text-black transition">Log In</button>
        <button class="bg-[#000033] text-white px-5 py-2.5 rounded-md text-[15px] font-semibold hover:bg-slate-900 transition">
          Get Started
        </button>
      </div>
  
      <div class="md:hidden flex items-center">
        <button on:click={toggleMobileMenu} class="text-slate-800 focus:outline-none">
          {#if isMobileMenuOpen}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          {:else}
            <svg xmlns="http://www.w3.org/2000/svg" class="h-7 w-7" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
            </svg>
          {/if}
        </button>
      </div>
    </nav>
  
    {#if isMobileMenuOpen}
      <div transition:slide class="md:hidden bg-white border-t border-slate-50 absolute w-full left-0 shadow-2xl overflow-hidden">
        <div class="flex flex-col p-6 gap-4">
          
          <div>
            <button on:click={() => toggleDropdown('company')} class="flex items-center justify-between w-full text-lg font-semibold text-slate-800">
              Company
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 transition-transform {activeDropdown === 'company' ? 'rotate-180' : ''}" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            {#if activeDropdown === 'company'}
              <div transition:slide class="pl-4 mt-2 flex flex-col gap-3 border-l-2 border-slate-100">
                <a href="#" class="text-slate-600">Item 1</a>
                <a href="#" class="text-slate-600">Item 2</a>
                <a href="#" class="text-slate-600">Item 3</a>
              </div>
            {/if}
          </div>
  
          <div>
            <button on:click={() => toggleDropdown('products')} class="flex items-center justify-between w-full text-lg font-semibold text-slate-800">
              Products
              <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 transition-transform {activeDropdown === 'products' ? 'rotate-180' : ''}" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </button>
            {#if activeDropdown === 'products'}
              <div transition:slide class="pl-4 mt-2 flex flex-col gap-3 border-l-2 border-slate-100">
                <a href="#" class="text-slate-600">Item 1</a>
                <a href="#" class="text-slate-600">Item 2</a>
                <a href="#" class="text-slate-600">Item 3</a>
              </div>
            {/if}
          </div>
  
          <a href="#support" class="text-lg font-semibold text-slate-800">Support</a>
          
          <hr class="my-2 border-slate-100" />
          
          <button class="text-lg font-semibold text-slate-800 text-left">Log In</button>
          <button class="bg-[#000033] text-white px-5 py-3 rounded-lg text-lg font-bold hover:bg-slate-900 transition">
            Get Started
          </button>
        </div>
      </div>
    {/if}
  </div>