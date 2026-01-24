<script>
  import { Home, Sparkles, MapPin, Phone, CheckCircle, ArrowRight, Star, Smile } from 'lucide-svelte';

  const config = {
    slug: "columbus-home-cleaners",
    description: "Professional and reliable home cleaning services in Columbus, Ohio. Book your service today!",
    heroTitle: "A Sparkling Clean Home is a Happy Home",
    heroSubtitle: "Let us handle the cleaning while you enjoy your time. Professional, reliable, and thorough home cleaning services in Columbus.",
    features: [
      {
        title: "Experienced Professionals",
        description: "Our cleaning staff is trained, experienced, and dedicated to providing the best service.",
        icon: Smile
      },
      {
        title: "Eco-Friendly Products",
        description: "We use safe and effective cleaning products that are safe for your family and pets.",
        icon: Sparkles
      },
      {
        title: "Serving Columbus Area",
        description: "Proudly serving Columbus and the surrounding neighborhoods with top-rated cleaning services.",
        icon: MapPin
      }
    ]
  };

  const services = [
    "Standard House Cleaning",
    "Deep Cleaning Services",
    "Move-In / Move-Out Cleaning",
    "Recurring Maid Service",
    "Apartment Cleaning",
    "Custom Cleaning Plans"
  ];
</script>

<svelte:head>
  <title>Columbus Home Cleaners: Professional Home Cleaning Services</title>
  <meta name="description" content={config.description} />
</svelte:head>

<main class="min-h-screen bg-white text-zinc-900 font-sans">
  <!-- Header -->
  <header class="sticky top-0 z-50 bg-white/95 backdrop-blur-sm border-b border-zinc-200">
    <div class="max-w-7xl mx-auto px-4 h-20 flex items-center justify-between">
      <div class="flex items-center gap-2">
        <div class="bg-blue-500 p-2 rounded-lg">
          <Home class="text-white" size={24} />
        </div>
        <span class="text-xl font-black tracking-tighter uppercase text-zinc-900">Columbus<span class="text-blue-600">Home</span>Cleaners</span>
      </div>
      <a href="#contact" class="hidden md:flex items-center gap-2 bg-zinc-900 text-white px-6 py-3 rounded-full font-bold hover:bg-blue-600 transition-colors">
        <Phone size={18} />
        Get a Quote
      </a>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="relative overflow-hidden bg-zinc-950 text-white py-20 lg:py-32">
    <div class="absolute inset-0 opacity-20">
      <div class="absolute inset-0 bg-[radial-gradient(circle_at_center,_var(--tw-gradient-stops))] from-blue-500 via-transparent to-transparent"></div>
    </div>
    
    <div class="max-w-7xl mx-auto px-4 relative z-10">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <div>
          <div class="inline-flex items-center gap-2 bg-blue-500/10 border border-blue-500/50 text-blue-500 px-4 py-1 rounded-full text-sm font-bold mb-6">
            <Star size={14} /> Top-Rated Service
          </div>
          <h1 class="text-5xl lg:text-7xl font-black leading-tight mb-6">
            {config.heroTitle}
          </h1>
          <p class="text-xl text-zinc-400 mb-8 max-w-xl">
            {config.heroSubtitle}
          </p>
          <div class="flex flex-col sm:flex-row gap-4">
            <a href="#contact" class="bg-blue-500 hover:bg-blue-400 text-zinc-950 font-black text-center px-8 py-4 rounded-xl text-lg flex items-center justify-center gap-2 transition-all transform hover:scale-105">
              GET A FREE QUOTE <ArrowRight size={20} />
            </a>
          </div>
        </div>
        <div class="relative hidden lg:block">
          <div class="aspect-square bg-gradient-to-br from-blue-500 to-blue-700 rounded-3xl rotate-3 flex items-center justify-center p-8">
            <div class="bg-zinc-900 w-full h-full rounded-2xl -rotate-3 p-8 flex flex-col justify-center">
                <p class="text-lg text-zinc-400 mb-4 italic">"The best cleaning service in Columbus! My home has never looked better."</p>
                <p class="text-blue-500 font-bold text-right">- Sarah D., Columbus Resident</p>
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
        <h2 class="text-3xl md:text-5xl font-black text-zinc-900 mb-4">Why Choose Columbus Home Cleaners?</h2>
        <div class="w-20 h-2 bg-blue-500 mx-auto"></div>
      </div>

      <div class="grid md:grid-cols-3 gap-8">
        {#each config.features as feature (feature.title)}
          <article class="bg-white p-8 rounded-2xl shadow-xl shadow-zinc-200/50 border border-zinc-100 hover:border-blue-500 transition-colors">
            <div class="bg-blue-100 text-blue-600 w-16 h-16 rounded-xl flex items-center justify-center mb-6">
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
          <h2 class="text-4xl font-black mb-6">Our Commitment to a Cleaner Home</h2>
          <p class="text-lg text-zinc-600 mb-8 italic">
            "We believe a clean home is a happy home. Our mission is to provide reliable, high-quality cleaning services."
          </p>
          <div class="grid sm:grid-cols-2 gap-4">
            {#each services as service (service)}
              <div class="flex items-center gap-3 p-4 bg-zinc-100 rounded-lg">
                <CheckCircle class="text-blue-600" size={20} />
                <span class="font-bold text-sm text-zinc-700">{service}</span>
              </div>
            {/each}
          </div>
        </div>
        <div class="bg-zinc-900 text-white p-10 rounded-3xl relative overflow-hidden">
          <div class="relative z-10">
            <h3 class="text-2xl font-bold mb-4">Serving Columbus Metro</h3>
            <p class="text-zinc-400 mb-6">We cover everything from Downtown and the Short North to Westerville, Dublin, and Upper Arlington. Your satisfaction is our priority.</p>
            <div class="flex items-center gap-4 mb-6">
              <div class="text-blue-500">
                <Star fill="currentColor" size={20} />
              </div>
              <span class="text-lg font-bold">5-Star Service Rating</span>
            </div>
            <div class="border-t border-zinc-800 pt-6">
                <p class="text-sm font-bold uppercase tracking-wider text-blue-500 mb-2">Book Your Cleaning</p>
                <p class="text-3xl font-black">Flexible Scheduling</p>
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
          <h4 class="font-bold text-lg mb-2 text-blue-500">What services do you offer?</h4>
          <p class="text-zinc-400">We offer a wide range of services including standard cleaning, deep cleaning, move-in/out cleaning, and recurring maid services. We can also create custom cleaning plans.</p>
        </div>
        <div class="bg-zinc-800/50 p-6 rounded-xl border border-zinc-700">
          <h4 class="font-bold text-lg mb-2 text-blue-500">Do I need to provide cleaning supplies?</h4>
          <p class="text-zinc-400">No, we bring all the necessary equipment and eco-friendly cleaning supplies to get the job done right.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4">
      <div class="bg-blue-500 rounded-3xl overflow-hidden shadow-2xl flex flex-col lg:flex-row">
        <div class="p-10 lg:p-16 flex-1 text-zinc-950">
          <h2 class="text-4xl lg:text-5xl font-black mb-6">Get Your Free Estimate</h2>
          <p class="text-xl font-medium mb-8 opacity-90">
            Fill out the form below for a free, no-obligation quote.
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
              <option value="standard-cleaning">Standard Cleaning</option>
              <option value="deep-cleaning">Deep Cleaning</option>
              <option value="move-out-cleaning">Move-Out Cleaning</option>
              <option value="other">Other</option>
            </select>
            <textarea 
              name="message" 
              rows="4" 
              placeholder="Tell us about your cleaning needs..."
              class="w-full px-6 py-4 rounded-xl bg-white/20 border-2 border-zinc-950/10 placeholder:text-zinc-800 focus:outline-none focus:border-zinc-950 transition-colors"
            ></textarea>
            
            <button type="submit" class="w-full bg-zinc-950 text-white font-black py-5 rounded-xl text-xl hover:bg-zinc-800 transition-all flex items-center justify-center gap-3 group">
              SUBMIT REQUEST
              <Sparkles class="group-hover:text-blue-500 transition-colors" size={24} />
            </button>
          </form>
        </div>
        
        <div class="bg-zinc-950 p-10 lg:p-16 text-white lg:w-1/3 flex flex-col justify-center border-l border-white/10">
          <div class="space-y-10">
            <div>
              <p class="text-blue-500 font-bold text-sm uppercase mb-2">Call for a Quote</p>
              <p class="text-3xl font-black">(614) 555-1234</p>
            </div>
            <div>
              <p class="text-blue-500 font-bold text-sm uppercase mb-2">Service Area</p>
              <p class="text-xl font-bold">Columbus, OH & Surrounding Areas</p>
            </div>
            <div class="flex gap-4">
              <div class="bg-zinc-800 p-3 rounded-full"><Smile size={20}/></div>
              <div class="bg-zinc-800 p-3 rounded-full"><Sparkles size={20}/></div>
              <div class="bg-zinc-800 p-3 rounded-full"><MapPin size={20}/></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <footer class="py-12 bg-zinc-50 border-t border-zinc-200">
    <div class="max-w-7xl mx-auto px-4 text-center">
      <div class="flex items-center justify-center gap-2 mb-6">
        <Home class="text-blue-500" size={20} />
        <span class="text-lg font-black tracking-tighter uppercase text-zinc-900">Columbus<span class="text-blue-600">Home</span>Cleaners</span>
      </div>
      <p class="text-zinc-500 text-sm">
        &copy; {new Date().getFullYear()} Columbus Home Cleaners. All Rights Reserved.
        <br />
        Proudly serving Franklin, Delaware, and Fairfield counties.
      </p>
    </div>
  </footer>
</main>

<style>
  :global(html) {
    scroll-behavior: smooth;
  }
</style>
