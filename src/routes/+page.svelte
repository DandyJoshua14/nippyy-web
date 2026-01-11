<script>
	import Hero from "$lib/components/Hero.svelte";
	import InclusiveMission from "$lib/components/InclusiveMission.svelte";
	import JoinNippyCTA from "$lib/components/JoinNippyCTA.svelte";
import Navbar from "$lib/components/Navbar.svelte";
	import PerfectPartner from "$lib/components/PerfectPartner.svelte";
	import WePutLess from "$lib/components/WePutLess.svelte";

    const steps = [
      {
        id: "01",
        title: "Sign Up",
        desc: "Download the app and create an account in minutes.",
        img: "/hiw-1.jpeg",
        reverse: false
      },
      {
        id: "02",
        title: "Verify & Secure",
        desc: "Add your details and activate security features.",
        img: "/hiw-2.jpeg",
        reverse: true
      },
      {
        id: "03",
        title: "Start Transacting",
        desc: "Enjoy complete financial freedom from one platform.",
        img: "/hiw-3.jpeg",
        reverse: false
      }
    ];
  </script>
      <Navbar/>
  <Hero/>
  <div class="min-h-screen font-sans text-slate-900 bg-white overflow-x-hidden">
    
    
    <main class="relative z-10 bg-white">
      <WePutLess/>
  <PerfectPartner/>
      <section class=" bg-[#E6EDFF] w-screen">
        <div class="max-w-5xl mx-auto px-6 py-24">

        
        <h2 class="text-4xl font-extrabold text-center text-[#0A0E27] mb-24">How it Works</h2>
        
        <div class="space-y-40 ">
          {#each steps as step}
            <div class="flex flex-col {step.reverse ? 'md:flex-row-reverse' : 'md:flex-row'} items-center gap-12 lg:gap-24">
              <div class="flex-1">
                <div class="text-8xl font-black text-slate-100 select-none mb-[-2rem]">{step.id}</div>
                <div class="relative pl-4 border-l-4 border-cyan-500">
                  <h3 class="text-3xl font-bold text-[#0A0E27] mb-4">{step.title}</h3>
                  <p class="text-slate-500 text-lg leading-relaxed">{step.desc}</p>
                </div>
              </div>
              <div class="flex-1">
                <div class="relative">
                  <div class="absolute -inset-4 bg-cyan-100 rounded-full blur-3xl opacity-30"></div>
                  <img src={step.img} alt={step.title} class="relative max-h-[550px] w-auto mx-auto drop-shadow-2xl" />
                </div>
              </div>
            </div>
          {/each}
        </div>
      </div>
      </section>
    </main>
  <InclusiveMission/>
  <JoinNippyCTA/>
    <footer class="bg-[#0B0D47] text-white pt-24 pb-12 px-6">
      <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-16 mb-24">
        <div class="col-span-1">
          <img src="/logo-dark.png" alt="Logo" class="h-8 mb-8" />
          <p class="text-slate-400 leading-relaxed">
            The all-in-one platform for your borderless lifestyle. Send, spend, and save globally.
          </p>
        </div>
        <div>
          <h4 class="font-bold mb-8 text-lg">Company</h4>
          <ul class="space-y-4 text-slate-400">
            <li><a href="/" class="hover:text-white transition">About Us</a></li>
            <li><a href="/" class="hover:text-white transition">Careers</a></li>
            <li><a href="/" class="hover:text-white transition">Legal</a></li>
          </ul>
        </div>
        <div>
          <h4 class="font-bold mb-8 text-lg">Products</h4>
          <ul class="space-y-4 text-slate-400">
            <li><a href="/" class="hover:text-white transition">Nippyy Tag</a></li>
            <li><a href="/" class="hover:text-white transition">Virtual Cards</a></li>
            <li><a href="/" class="hover:text-white transition">Currency Swap</a></li>
          </ul>
        </div>
        <div>
          <h4 class="font-bold mb-8 text-lg">Help</h4>
          <ul class="space-y-4 text-slate-400">
            <li><a href="/" class="hover:text-white transition">Help Center</a></li>
            <li><a href="/" class="hover:text-white transition">Contact Support</a></li>
            <li><a href="/" class="hover:text-white transition">Twitter (X)</a></li>
          </ul>
        </div>
      </div>
      <div class="max-w-7xl mx-auto pt-8 border-t border-slate-800 text-sm text-slate-500 flex flex-col md:flex-row justify-between items-center gap-4">
        <p>© 2025 Nippyy Solutions. All rights reserved.</p>
        <div class="flex gap-6">
          <a href="/" class="hover:text-white">Privacy Policy</a>
          <a href="/" class="hover:text-white">Terms of Service</a>
        </div>
      </div>
    </footer>
  </div>
  
  <style>
    :global(html) {
      scroll-behavior: smooth;
    }
  </style>