<script>
    import { slide } from 'svelte/transition';
  
    let faqs = [
      { q: "Is it Nippy or Nippyy?", a: "We get this a lot of times, but it is actually spelt as NIPPYY with double Ys." },
      { q: "What is Nippyy?", a: "Nippyy is a revolutionary digital payment platform that allows users to send and receive money instantly and affordable across borders — all from one secure app." },
      { q: "How do I open a Nippyy account?", a: "Download the Nippyy app, sign up with your phone number or email, verify your identity, and you’re good to go. It only takes a few minutes." },
      { q: "What currencies does Nippyy support?", a: "We currently support multiple major currencies, including NGN, USD, GBP, and EUR, with more being added regularly." },
      { q: "Can I send money internationally?", a: "Yes! Nippyy lets you send and receive money across borders instantly, at competitive rates, with no hidden charges." },
      { q: "How secure is Nippyy?", a: "We use bank-grade, blockchain-level encryption, advanced fraud monitoring, and multifactor authentication to keep your money and personal information safe at all times." },
      { q: "How does currency conversion work?", a: "Simply select the currencies you want to convert between, enter the amount, and Nippyy instantly gives you the best market rate available." },
      { q: "What is the multi-wallet feature?", a: "Multi-wallets let you hold, manage, and spend in different currencies without converting unnecessarily — perfect for travelers, freelancers, and global businesses." },
      { q: "Does Nippyy offer loans?", a: "No! We do not offer loans and credits for now." },
      { q: "Are there any hidden fees?", a: "No hidden fees ever. You see all charges upfront before you confirm any transaction." },
      { q: "How can I contact support?", a: "You can reach us via WhatsApp chat, email, or social media channels. No Bots or AI, Our team is available 24/7 to help." },
      { q: "How fast are Nippyy transfers?", a: "Nippyy transfers are nearly instant! Transactions are completed in just a few seconds, with the money reaching the recipient immediately." }
    ];
  
    /**
	 * @type {number | null}
	 */
    let openIndex = null;
  
    /**
	 * @param {number | null} index
	 */
    function toggle(index) {
      openIndex = openIndex === index ? null : index;
    }
  </script>
  
  <section class="py-24 px-6 bg-white relative overflow-hidden">
    <div class="max-w-3xl mx-auto text-center mb-16 relative z-10">
      <span class="bg-[#CFF0FB] text-[#00AEEF] px-6 py-1.5 rounded-full text-xs font-bold uppercase tracking-wider">
        FAQs
      </span>
      <h2 class="text-4xl md:text-5xl font-extrabold text-[#0A0E27] mt-6 mb-4">
        Frequently Asked Questions
      </h2>
      <p class="text-slate-600 font-medium italic">
        “Your Questions, answered clearly and quickly!”
      </p>
    </div>
  
    <div class="max-w-4xl mx-auto relative">
      <img 
        src="/nippyy-icon.png" 
        alt="" 
        class="absolute -bottom-20 -right-20 w-80 h-80 opacity-10 pointer-events-none transform rotate-12 z-0"
      />
  
      <div class="bg-[#E9F3FF] rounded-[2rem] p-4 md:p-8 relative z-10 shadow-sm">
        <div class="space-y-2">
          {#each faqs as faq, i}
            <div class="border-b border-blue-200/50 last:border-0">
              <button 
                on:click={() => toggle(i)}
                class="w-full py-5 flex items-center justify-between text-left group"
              >
                <span class="text-[#0A0E27] font-bold text-base md:text-lg transition-colors group-hover:text-[#00AEEF]">
                  {faq.q}
                </span>
                <span class="text-2xl text-slate-400 font-light ml-4">
                  {openIndex === i ? '−' : '+'}
                </span>
              </button>
              
              {#if openIndex === i}
                <div transition:slide={{ duration: 300 }} class="pb-6 pr-10">
                  <p class="text-slate-600 leading-relaxed">
                    {faq.a}
                  </p>
                </div>
              {/if}
            </div>
          {/each}
        </div>
      </div>
  
      <div class="mt-8 bg-[#E9F3FF] rounded-[1.5rem] p-6 md:p-10 flex flex-col md:flex-row items-center justify-between relative z-10 shadow-sm">
        <div class="text-center md:text-left mb-6 md:mb-0">
          <h3 class="text-2xl font-bold text-[#0A0E27]">Have any other Questions?</h3>
          <p class="text-slate-600 font-medium">Don't hesitate to reach us!</p>
        </div>
        
        <div class="flex gap-4">
          <a href="mailto:support@nippyy.com" class="w-12 h-12 bg-white rounded-xl shadow-md flex items-center justify-center hover:scale-110 transition-transform">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#00AEEF]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </a>
          <a href="#" class="w-12 h-12 bg-white rounded-xl shadow-md flex items-center justify-center hover:scale-110 transition-transform">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#25D366]" fill="currentColor" viewBox="0 0 24 24">
              <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
            </svg>
          </a>
          <a href="#" class="w-12 h-12 bg-white rounded-xl shadow-md flex items-center justify-center hover:scale-110 transition-transform">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-[#00AEEF]" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </section>