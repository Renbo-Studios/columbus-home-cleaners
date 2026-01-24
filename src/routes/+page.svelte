<script>
  import { Zap, Shield, Globe, Phone, Clock, CheckCircle, ArrowRight, Star, AlertTriangle } from 'lucide-svelte';

  const config = {
    slug: "emergency-cleaning-services-columbus-ohio",
    description: "Need urgent cleaning in Columbus, Ohio? Get 24/7 emergency deep cleaning for homes and businesses. Fast and reliable. Book your same-day service now!",
    heroTitle: "Emergency Cleaning in Columbus: Fast, Professional, Same-Day Results",
    heroSubtitle: "Don't wait for the mess to get worse. Our expert Columbus cleaning crews are on standby to restore your property immediately. Request your quote now!",
    features: [
      {
        title: "24/7 Rapid Response",
        description: "We are ready around the clock. Our Columbus teams arrive within hours to handle your cleaning emergencies.",
        icon: Zap
      },
      {
        title: "Industrial-Grade Clean",
        description: "From deep sanitization to move-out emergencies, we use high-power equipment for a spotless finish.",
        icon: Shield
      },
      {
        title: "Trusted Local Experts",
        description: "Serving the entire Columbus metro area with reliable, top-rated professional cleaning services.",
        icon: Globe
      }
    ]
  };

  const services = [
    "Biohazard & Sanitization",
    "Post-Construction Cleanup",
    "Emergency Move-Out Cleaning",
    "Flood & Water Mess Restoration",
    "Last-Minute Commercial Cleaning",
    "Industrial Spill Cleanup"
  ];
</script>

<svelte:head>
  <title>{config.heroTitle}</title>
  <meta name="description" content={config.description} />
</svelte:head>

<main class="min-h-screen bg-white text-zinc-900 font-sans">
  <!-- Top Urgency Bar -->
  <div class="bg-amber-600 text-white py-2 px-4 text-center text-sm font-bold uppercase tracking-widest flex items-center justify-center gap-2">
    <AlertTriangle size={16} />
    24/7 Emergency Dispatch Available in Columbus
    <AlertTriangle size={16} />
  </div>

  <!-- Header -->
  <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-sm border-b border-zinc-200">
    <div class="max-w-7xl mx-auto px-4 h-20 flex items-center justify-between">
      <div class="flex items-center gap-2">
        <div class="bg-amber-500 p-2 rounded-lg">
          <Zap class="text-white" size={24} fill="currentColor" />
        </div>
        <span class="text-xl font-black tracking-tighter uppercase text-zinc-900">Columbus<span class="text-amber-600">Rapid</span>Clean</span>
      </div>
      <a href="#contact" class="hidden md:flex items-center gap-2 bg-zinc-900 text-white px-6 py-3 rounded-full font-bold hover:bg-amber-600 transition-colors">
        <Phone size={18} />
        Call Now
      </a>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="relative overflow-hidden bg-zinc-950 text-white py-20 lg:py-32">
    <div class="absolute inset-0 opacity-20">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-amber-500 via-transparent to-transparent"></div>
    </div>
    
    <div class="max-w-7xl mx-auto px-4 relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <div class="inline-flex items-center gap-2 bg-amber-500/10 border border-amber-500/50 text-amber-500 px-4 py-1 rounded-full text-sm font-bold mb-6">
            <Clock size={14} /> Same-Day Service Available
          </div>
          <h1 class="text-5xl lg:text-7xl font-black leading-tight mb-6">
            {config.heroTitle}
          </h1>
          <p class="text-xl text-zinc-400 mb-8 max-w-xl">
            {config.heroSubtitle}
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#contact" class="bg-amber-500 hover:bg-amber-400 text-zinc-950 font-black text-center px-8 py-4 rounded-xl text-lg flex items-center justify-center gap-2 transition-all transform hover:scale-105">
              GET AN EMERGENCY QUOTE <ArrowRight size={20} />
            </a>
            <div class="flex items-center gap-4 px-4 py-2 border border-zinc-800 rounded-xl bg-zinc-900/50">
              <div class="flex -space-x-2">
                {#each [1,2,3] as i}
                  <div class="w-8 h-8 rounded-full border-2 border-zinc-900 bg-zinc-700 flex items-center justify-center text-[10px] font-bold">C{i}</div>
                {/each}
              </div>
              <div class="text-xs">
                <p class="font-bold">4.9/5 Rating</p>
                <p class="text-zinc-500">200+ Columbus Clients</p>
              </div>
            </div>
          </div>
        </div>
        <div class="relative hidden lg:block">
          <div class="aspect-square bg-gradient-to-br from-amber-500 to-amber-700 rounded-3xl rotate-3 flex items-center justify-center p-8">
            <div class="bg-zinc-900 w-full h-full rounded-2xl -rotate-3 p-8 flex flex-col justify-between">
              <div class="space-y-4">
                <div class="h-4 w-2/3 bg-zinc-800 rounded"></div>
                <div class="h-4 w-full bg-zinc-800 rounded"></div>
                <div class="h-4 w-1/2 bg-zinc-800 rounded"></div>
              </div>
              <div class="bg-amber-500/20 border border-amber-500/50 p-4 rounded-xl">
                <p class="text-amber-500 font-bold mb-1">Status: High Priority</p>
                <p class="text-sm text-zinc-400">Dispatching cleaning unit to Columbus Metro Area...</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Features Section -->
  <section class="py-24 bg-zinc-50">
    <div class="max-w-7xl mx-auto px-4">
      <div class="text-center mb-16">
        <h2 class="text-3xl md:text-5xl font-black text-zinc-900 mb-4">Why Columbus Trusts Our Rapid Teams</h2>
        <div class="w-20 h-2 bg-amber-500 mx-auto"></div>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        {#each config.features as feature}
          <article class="bg-white p-8 rounded-2xl shadow-xl shadow-zinc-200/50 border border-zinc-100 hover:border-amber-500 transition-colors">
            <div class="bg-amber-100 text-amber-600 w-16 h-16 rounded-xl flex items-center justify-center mb-6">
              <svelte:component this={feature.icon} size={32} />
            </div>
            <h3 class="text-2xl font-bold mb-4">{feature.title}</h3>
            <p class="text-zinc-600 leading-relaxed">{feature.description}</p>
          </article>
        {/each}
      </div>
    </div>
  </section>

  <!-- Services / About -->
  <section class="py-24 border-t border-zinc-100">
    <div class="max-w-7xl mx-auto px-4">
      <div class="grid lg:grid-cols-2 gap-16 items-center">
        <div>
          <h2 class="text-4xl font-black mb-6">Expert Cleaning for Critical Situations</h2>
          <p class="text-lg text-zinc-600 mb-8 italic">
            "When things go wrong, we make them right. Fast."
          </p>
          <div class="grid sm:grid-cols-2 gap-4">
            {#each services as service}
              <div class="flex items-center gap-3 p-4 bg-zinc-100 rounded-lg">
                <CheckCircle class="text-amber-600" size={20} />
                <span class="font-bold text-sm text-zinc-700">{service}</span>
              </div>
            {/each}
          </div>
        </div>
        <div class="bg-zinc-900 text-white p-10 rounded-3xl relative overflow-hidden">
          <div class="relative z-10">
            <h3 class="text-2xl font-bold mb-4">Serving Columbus Metro</h3>
            <p class="text-zinc-400 mb-6">We cover everything from Downtown and the Short North to Westerville, Dublin, and Upper Arlington. No location is too far when time is of the essence.</p>
            <div class="flex items-center gap-4 mb-6">
              <div class="text-amber-500">
                <Star fill="currentColor" size={20} />
              </div>
              <span class="text-lg font-bold">5-Star Response Rating</span>
            </div>
            <div class="border-t border-zinc-800 pt-6">
              <p class="text-sm font-bold uppercase tracking-wider text-amber-500 mb-2">Next available slot:</p>
              <p class="text-3xl font-black">Within 2 Hours</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- FAQ / Testimonial Section -->
  <section class="py-24 bg-zinc-900 text-white">
    <div class="max-w-4xl mx-auto px-4 text-center">
      <h2 class="text-3xl md:text-4xl font-black mb-12">Frequently Asked Questions</h2>
      <div class="space-y-6 text-left">
        <div class="bg-zinc-800/50 p-6 rounded-xl border border-zinc-700">
          <h4 class="font-bold text-lg mb-2 text-amber-500">How quickly can you be here?</h4>
          <p class="text-zinc-400">Our average response time for emergency calls in Columbus is 60-90 minutes depending on your specific location.</p>
        </div>
        <div class="bg-zinc-800/50 p-6 rounded-xl border border-zinc-700">
          <h4 class="font-bold text-lg mb-2 text-amber-500">Do you handle commercial properties?</h4>
          <p class="text-zinc-400">Yes. We specialize in high-stakes commercial cleaning including retail, offices, and medical facilities that need immediate remediation.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4">
      <div class="bg-amber-500 rounded-3xl overflow-hidden shadow-2xl flex flex-col lg:flex-row">
        <div class="p-10 lg:p-16 flex-1 text-zinc-950">
          <h2 class="text-4xl lg:text-5xl font-black mb-6">Request Emergency Response</h2>
          <p class="text-xl font-medium mb-8 opacity-90">
            Fill out the form below for an instant callback and priority scheduling.
          </p>
          
          <form action="/api/leads" method="POST" class="space-y-4">
            <div class="grid md:grid-cols-2 gap-4">
              <input 
                type="text" 
                name="name" 
                placeholder="Your Full Name" 
                required
                class="w-full px-6 py-4 rounded-xl bg-white/20 border-2 border-zinc-950/10 placeholder:text-zinc-800 focus:outline-none focus:border-zinc-950 transition-colors"
              />
              <input 
                type="tel" 
                name="phone" 
                placeholder="Phone Number" 
                required
                class="w-full px-6 py-4 rounded-xl bg-white/20 border-2 border-zinc-950/10 placeholder:text-zinc-800 focus:outline-none focus:border-zinc-950 transition-colors"
              />
            </div>
            <select 
              name="service" 
              class="w-full px-6 py-4 rounded-xl bg-white/20 border-2 border-zinc-950/10 text-zinc-800 focus:outline-none focus:border-zinc-950 transition-colors"
            >
              <option value="emergency-residential">Emergency Residential Cleaning</option>
              <option value="emergency-commercial">Emergency Commercial Cleaning</option>
              <option value="sanitization">Deep Sanitization / Biohazard</option>
              <option value="other">Other Emergency Needs</option>
            </select>
            <textarea 
              name="message" 
              rows="4" 
              placeholder="Tell us about the emergency..."
              class="w-full px-6 py-4 rounded-xl bg-white/20 border-2 border-zinc-950/10 placeholder:text-zinc-800 focus:outline-none focus:border-zinc-950 transition-colors"
            ></textarea>
            
            <button type="submit" class="w-full bg-zinc-950 text-white font-black py-5 rounded-xl text-xl hover:bg-zinc-800 transition-all flex items-center justify-center gap-3 group">
              SUBMIT URGENT REQUEST
              <Zap class="group-hover:text-amber-500 transition-colors" size={24} fill="currentColor" />
            </button>
          </form>
        </div>
        
        <div class="bg-zinc-950 p-10 lg:p-16 text-white lg:w-1/3 flex flex-col justify-center border-l border-white/10">
          <div class="space-y-10">
            <div>
              <p class="text-amber-500 font-bold text-sm uppercase mb-2">Direct Emergency Line</p>
              <p class="text-3xl font-black">(614) 555-0199</p>
            </div>
            <div>
              <p class="text-amber-500 font-bold text-sm uppercase mb-2">Service Area</p>
              <p class="text-xl font-bold">Columbus, OH + 30 Mile Radius</p>
            </div>
            <div class="flex gap-4">
              <div class="bg-zinc-800 p-3 rounded-full"><Clock size={20}/></div>
              <div class="bg-zinc-800 p-3 rounded-full"><Shield size={20}/></div>
              <div class="bg-zinc-800 p-3 rounded-full"><Globe size={20}/></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer class="py-12 bg-zinc-50 border-t border-zinc-200">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <div class="flex items-center justify-center gap-2 mb-6">
        <Zap class="text-amber-500" size={20} fill="currentColor" />
        <span class="text-lg font-black tracking-tighter uppercase text-zinc-900">Columbus<span class="text-amber-600">Rapid</span>Clean</span>
      </div>
      <p class="text-zinc-500 text-sm">
        &copy; {new Date().getFullYear()} Columbus Rapid Cleaning Services. Licensed, Bonded, and Insured.
        <br />
        Immediate dispatch available for Franklin, Delaware, and Fairfield counties.
      </p>
    </div>
  </footer>
</main>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }
</style>