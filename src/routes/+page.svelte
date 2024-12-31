<script>
// @ts-nocheck
 
      import { Accordion } from '@skeletonlabs/skeleton-svelte';
      const faqs = [
    {
      value: "booking",
      question: "How far in advance should I book?",
      answer: "We recommend booking at least 2-3 weeks in advance to ensure availability for your preferred date."
    },
    {
      value: "area",
      question: "What area do you serve?",
      answer: "We serve all of Central Florida including Orlando, Tampa, and surrounding areas."
    },
    {
      value: "setup",
      question: "How long does setup take?",
      answer: "Setup typically takes 30-45 minutes, and we arrive early to ensure everything is ready for your event."
    }
  ];

  let accordionValue = faqs[0].value;
    const reviews = [
      {
        text: "Amazing foam party! The DJ brought the perfect energy and the foam was so much fun. Best decision for my son's birthday!",
        author: "Sarah M.",
        rating: 5
      },
      {
        text: "The 2-hour foam party was so much fun! The team was professional and made sure everyone had a blast. Would definitely recommend!",
        author: "Mike R.",
        rating: 5
      },
      {
        text: "Great experience from start to finish! The setup was quick and the cleanup was thorough. Perfect for our summer event!",
        author: "Jessica L.",
        rating: 5
      }
    ]
  
  
  
    const packages = [
      {
        title: "1-HOUR FOAM PARTY",
        price: "$349",
        features: [
          "Perfect for small events",
          "Professional foam equipment",
          "Setup and cleanup included",
          "Trained foam technician"
        ]
      },
      {
        title: "2-HOUR FOAM PARTY",
        price: "$449",
        features: [
          "Most popular package",
          "Extended foam time",
          "Setup and cleanup included",
          "Trained foam technician"
        ]
      },
      {
        title: "30-MINUTE FOAM PARTY",
        price: "$249",
        features: [
          "Quick foam experience",
          "Perfect for small groups",
          "Setup and cleanup included",
          "Trained foam technician"
        ]
      }
    ]
  </script>
  
  <div class="bg-[#3861fb] min-h-screen">
    <!-- Hero Section -->
    <section class="relative px-4 pt-20 pb-32 text-white">
      <div class="container mx-auto max-w-6xl">
        <div class="grid lg:grid-cols-2 gap-8 items-center">
          <div>
            <h1 class="text-4xl md:text-5xl font-bold mb-6">
              THE ULTIMATE FOAM PARTY SERVICE IN CENTRAL FLORIDA
            </h1>
            <p class="text-lg mb-8">
              Book a foam party and make your next event unforgettable! Perfect for birthdays, schools, festivals, fairs, and more!
            </p>
            <button class="bg-orange-500 hover:bg-orange-600 text-white px-8 py-3 rounded-full font-semibold">
              GET STARTED NOW
            </button>
          </div>
          <div class="relative">
            <img
              src="/placeholder.svg?height=400&width=400"
              alt="Foam party fun"
              class="rounded-full w-full max-w-md mx-auto"
            />
          </div>
        </div>
      </div>
      <div class="absolute bottom-0 left-0 right-0">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 120" class="fill-white">
          <path d="M0,64L80,69.3C160,75,320,85,480,80C640,75,800,53,960,48C1120,43,1280,53,1360,58.7L1440,64L1440,120L1360,120C1280,120,1120,120,960,120C800,120,640,120,480,120C320,120,160,120,80,120L0,120Z"></path>
        </svg>
      </div>
    </section>
  
    <!-- Video Section -->
    <section class="bg-white py-16 px-4">
      <div class="container mx-auto max-w-6xl">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#3861fb]">
          PROFESSIONAL FOAM PARTY COMPANY IN FLORIDA
        </h2>
        <div class="aspect-w-16 aspect-h-9">
          <div class="bg-gray-200 rounded-lg w-full h-[400px] flex items-center justify-center">
            <span class="text-gray-500">Video Placeholder</span>
          </div>
        </div>
      </div>
    </section>
  
    <!-- Reviews Section -->
    <section class="bg-[#3861fb] py-16 px-4 text-white">
      <div class="container mx-auto max-w-6xl">
        <h2 class="text-3xl font-bold text-center mb-12">CUSTOMER REVIEWS</h2>
        <div class="grid md:grid-cols-3 gap-8">
          {#each reviews as review}
            <div class="bg-white p-6 rounded-lg text-gray-800">
              <div class="flex gap-1 mb-4">
                {#each Array(review.rating) as _}
                  <svg class="w-5 h-5 text-yellow-400 fill-current" viewBox="0 0 20 20">
                    <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
                  </svg>
                {/each}
              </div>
              <p class="mb-4">{review.text}</p>
              <p class="font-semibold">{review.author}</p>
            </div>
          {/each}
        </div>
      </div>
    </section>
  
    <!-- How to Book -->
    <section class="bg-white py-16 px-4">
      <div class="container mx-auto max-w-6xl">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#3861fb]">HOW TO BOOK</h2>
        <div class="grid md:grid-cols-3 gap-8 text-center">
          <div>
            <div class="w-16 h-16 bg-[#3861fb] rounded-full flex items-center justify-center text-white text-xl font-bold mx-auto mb-4">1</div>
            <h3 class="font-semibold mb-2">Contact Us</h3>
            <p class="text-gray-600">Let us know the details of your event</p>
          </div>
          <div>
            <div class="w-16 h-16 bg-pink-500 rounded-full flex items-center justify-center text-white text-xl font-bold mx-auto mb-4">2</div>
            <h3 class="font-semibold mb-2">Reserve</h3>
            <p class="text-gray-600">We'll check availability and confirm your date</p>
          </div>
          <div>
            <div class="w-16 h-16 bg-orange-500 rounded-full flex items-center justify-center text-white text-xl font-bold mx-auto mb-4">3</div>
            <h3 class="font-semibold mb-2">Party Time!</h3>
            <p class="text-gray-600">We'll arrive and set up for your amazing foam party</p>
          </div>
        </div>
      </div>
    </section>
  
    <!-- Pricing -->
    <section class="bg-[#3861fb] py-16 px-4 text-white">
      <div class="container mx-auto max-w-6xl">
        <h2 class="text-3xl font-bold text-center mb-12">PRICING</h2>
        <div class="grid md:grid-cols-3 gap-8">
          {#each packages as pkg}
            <div class="bg-white p-6 rounded-lg text-gray-800">
              <h3 class="text-xl font-bold mb-4 text-center">{pkg.title}</h3>
              <p class="text-3xl font-bold text-center mb-6">{pkg.price}</p>
              <ul class="space-y-4 mb-8">
                {#each pkg.features as feature}
                  <li class="flex items-center gap-2">
                    <svg class="w-5 h-5 text-green-500" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
                    </svg>
                    {feature}
                  </li>
                {/each}
              </ul>
              <button class="w-full bg-orange-500 hover:bg-orange-600 text-white px-6 py-3 rounded-full font-semibold">
                Book Now
              </button>
            </div>
          {/each}
        </div>
      </div>
    </section>
  
   <!-- FAQ Section -->
<section class="bg-white py-16 px-4">
    <div class="container mx-auto max-w-6xl">
      <h2 class="text-3xl font-bold text-center mb-12 text-[#3861fb]">FREQUENTLY ASKED QUESTIONS</h2>
      <div class="max-w-2xl mx-auto">
        <Accordion value={accordionValue}>
          {#each faqs as faq}
            <Accordion.Item value={faq.value}>
              {#snippet lead()}<span class="text-[#3861fb]">Q</span>{/snippet}
              {#snippet control()}{faq.question}{/snippet}
              {#snippet panel()}{faq.answer}{/snippet}
            </Accordion.Item>
            <hr class="hr" />
          {/each}
        </Accordion>
      </div>
    </div>
  </section>
  
  <!-- Contact Form with Images -->
  <section class="bg-[#3861fb] py-16 px-4 text-white">
    <div class="container mx-auto max-w-6xl">
      <h2 class="text-3xl font-bold text-center mb-12">CONTACT US</h2>
      <div class="grid md:grid-cols-2 gap-8 items-center">
        <!-- Image Grid -->
        <div class="grid grid-cols-2 gap-4">
          {#each Array(4) as _, i}
            <div class="aspect-square overflow-hidden rounded-lg">
              <img 
                src="https://png.pngtree.com/thumb_back/fw800/background/20240518/pngtree-background-beautiful-wallpaper-image-image_15796837.jpg" 
                alt="Foam party event {i + 1}" 
                class="w-full h-full object-cover hover:scale-110 transition-transform duration-300"
              />
            </div>
          {/each}
        </div>
  
        <!-- Contact Form -->
        <div class="bg-white rounded-lg p-8 shadow-xl">
          <form class="space-y-6">
            <div class="grid grid-cols-2 gap-6">
              <div>
                <!-- svelte-ignore a11y_label_has_associated_control -->
                <label class="block text-sm font-medium text-gray-700 mb-2">First Name</label>
                <input 
                  type="text" 
                  class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-[#3861fb] focus:border-transparent transition-all" 
                  required
                />
              </div>
              <div>
                <!-- svelte-ignore a11y_label_has_associated_control -->
                <label class="block text-sm font-medium text-gray-700 mb-2">Last Name</label>
                <input 
                  type="text" 
                  class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-[#3861fb] focus:border-transparent transition-all" 
                  required
                />
              </div>
            </div>
            
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Email Address</label>
              <input 
                type="email" 
                class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-[#3861fb] focus:border-transparent transition-all" 
                required
              />
            </div>
            
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Phone Number</label>
              <input 
                type="tel" 
                class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-[#3861fb] focus:border-transparent transition-all" 
                required
              />
            </div>
            
            <div>
              <label class="block text-sm font-medium text-gray-700 mb-2">Message</label>
              <textarea 
                rows="4" 
                class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-[#3861fb] focus:border-transparent transition-all resize-none" 
                required
              ></textarea>
            </div>
            
            <button 
              type="submit" 
              class="w-full bg-orange-500 hover:bg-orange-600 text-white px-6 py-4 rounded-lg font-semibold transition-colors duration-200"
            >
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
  
    <footer class="bg-white py-4 text-center text-gray-600 text-sm">
      <div class="container mx-auto">
        © {new Date().getFullYear()} Foam Party. All rights reserved.
      </div>
    </footer>
  </div>
  
  <style>
    :global(body) {
      margin: 0;
      padding: 0;
    }
  </style>
  