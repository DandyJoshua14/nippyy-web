<script>
	import Footer from "$lib/components/Footer.svelte";
	import Hero from "$lib/components/home/Hero.svelte";
	import InclusiveMission from "$lib/components/home/InclusiveMission.svelte";
	// import JoinNippyCTA from "$lib/components/home/JoinNippyCTA.svelte";
import Navbar from "$lib/components/Navbar.svelte";
	import PerfectPartner from "$lib/components/home/PerfectPartner.svelte";
	import WePutLess from "$lib/components/home/WePutLess.svelte";
	import Step from "$lib/components/home/Step.svelte";
    
  </script>
  <svelte:head>
    <title>Nippyy — Instant Global Payments & Borderless Banking</title>
    <meta name="title" content="Nippyy — Instant Global Payments & Borderless Banking" />
    <meta name="description" content="Send and receive money instantly across borders with Nippyy. Enjoy zero-fee local transactions, multi-currency wallets, and real-time conversion at market rates." />
    <meta name="keywords" content="global payments, fintech, international money transfer, borderless banking, multi-currency wallet, Nippyy, cross-border payments" />
    <meta name="author" content="Softnext Solutions" />
  
    <meta property="og:type" content="website" />
    <meta property="og:url" content="https://nippyy-web.vercel.app/" />
    <meta property="og:title" content="Nippyy — Instant Global Payments & Borderless Banking" />
    <meta property="og:description" content="Manage, grow, and move your money globally with ease. Join thousands using Nippyy for seamless international transactions." />
    <meta property="og:image" content="https://nippyy-web.vercel.app/og-image.png" />
  
    <meta property="twitter:card" content="summary_large_image" />
    <meta property="twitter:url" content="https://nippyy-web.vercel.app/" />
    <meta property="twitter:title" content="Nippyy — Instant Global Payments & Borderless Banking" />
    <meta property="twitter:description" content="Send and receive money instantly across borders with zero stress. The future of global banking is here." />
    <meta property="twitter:image" content="https://nippyy-web.vercel.app/og-image.png" />
  
    <link rel="icon" type="image/png" href="/nippy-favicon.png" />
    
    <link rel="canonical" href="https://nippyy-web.vercel.app/" />
  
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" >
  </svelte:head>
      <Navbar/>
  <Hero/>
  <div class="min-h-screen font-sans text-slate-900 bg-white overflow-x-hidden">
    
    
    <main class="relative z-10 bg-white">
      <WePutLess/>
  <PerfectPartner/>
      <Step/>
    </main>
  <InclusiveMission/>
  
    <Footer/>
  </div>
  
  <style>
    :global(html) {
      scroll-behavior: smooth;
    }
  </style>