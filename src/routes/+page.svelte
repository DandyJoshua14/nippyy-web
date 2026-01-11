<script>
	import Footer from "$lib/components/Footer.svelte";
	import Hero from "$lib/components/home/Hero.svelte";
	import InclusiveMission from "$lib/components/home/InclusiveMission.svelte";
	import JoinNippyCTA from "$lib/components/home/JoinNippyCTA.svelte";
import Navbar from "$lib/components/Navbar.svelte";
	import PerfectPartner from "$lib/components/home/PerfectPartner.svelte";
	import WePutLess from "$lib/components/home/WePutLess.svelte";
    
  </script>
      <Navbar/>
  <Hero/>
  <div class="min-h-screen font-sans text-slate-900 bg-white overflow-x-hidden">
    
    
    <main class="relative z-10 bg-white">
      <WePutLess/>
  <PerfectPartner/>
      
    </main>
  <InclusiveMission/>
  <JoinNippyCTA/>
    <Footer/>
  </div>
  
  <style>
    :global(html) {
      scroll-behavior: smooth;
    }
  </style>