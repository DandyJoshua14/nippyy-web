<script>
    // Import your Navbar and Footer components here
    import Navbar from '$lib/components/Navbar.svelte';
    import Footer from '$lib/components/Footer.svelte';
  </script>
  
  <svelte:head>
    <title>About Us — Nippyy (Coming Soon)</title>
    <meta name="description" content="Learn more about Nippyy's mission to simplify global payments. Our story is coming soon." />
  </svelte:head>
  <Navbar/>
  <main class="relative min-h-screen flex items-center justify-center bg-white overflow-hidden">
    
    <div class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-[0.03] z-0">
      <img src="/nippyy-icon.png" alt="" class="w-[500px] h-[500px] rotate-12" />
    </div>
  
    <div class="relative z-10 text-center px-6">
      <div class="inline-flex items-center gap-2 bg-[#E0F2FE] text-[#00AEEF] px-5 py-2 rounded-full text-xs font-bold uppercase tracking-widest mb-8 border border-blue-100 shadow-sm">
        Our Mission
      </div>
  
      <h1 class="text-5xl md:text-7xl lg:text-8xl font-extrabold text-[#05051F] tracking-tighter leading-none">
        Coming <span class="text-[#00AEEF]">Soon</span>.
      </h1>
  
      <p class="mt-8 text-lg md:text-xl text-slate-500 max-w-lg mx-auto font-medium leading-relaxed">
        We're currently crafting the story of how Nippyy is redefining global financial freedom. Stay tuned for our official debut.
      </p>
  
      <div class="mt-12 flex justify-center gap-2">
        <div class="w-3 h-3 bg-[#00D27F] rounded-full animate-bounce"></div>
        <div class="w-3 h-3 bg-[#00AEEF] rounded-full animate-bounce [animation-delay:-0.15s]"></div>
        <div class="w-3 h-3 bg-[#05051F] rounded-full animate-bounce [animation-delay:-0.3s]"></div>
      </div>
    </div>
  </main>

  <Footer/>