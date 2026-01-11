<script>
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