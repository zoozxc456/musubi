<template>
  <UApp>
    <div
      class="min-h-screen bg-stone-50 text-stone-800 font-sans overflow-x-hidden antialiased selection:bg-stone-200 selection:text-stone-900"
    >
      <div
        class="hidden lg:block fixed top-0 left-0 w-5/12 h-screen overflow-hidden z-0 bg-stone-900"
      >
        <img
          src="https://images.unsplash.com/photo-1519741497674-611481863552?ixlib=rb-4.0.3&auto=format&fit=crop&w=1200&q=90"
          class="absolute inset-0 w-full h-full object-cover opacity-0 animate-zoom-fade-in"
          alt="Wedding Couple"
        />

        <div
          class="absolute inset-0 bg-black/30 flex flex-col justify-center items-center text-white text-center p-12"
        >
          <p
            class="text-sm tracking-[0.3em] uppercase mb-6 border-b border-white/50 pb-2 opacity-0 animate-fade-in-up"
            style="animation-delay: 500ms"
          >
            Save The Date
          </p>
          <h1
            class="text-7xl font-serif mb-6 drop-shadow-lg opacity-0 animate-fade-in-up"
            style="animation-delay: 800ms"
          >
            Alex <br />
            <span class="text-5xl font-light italic">&</span> <br />
            Sarah
          </h1>
          <p
            class="text-xl font-light tracking-wide mt-4 opacity-0 animate-fade-in-up"
            style="animation-delay: 1200ms"
          >
            2026. 10. 24
          </p>
        </div>
      </div>

      <div
        class="w-full lg:w-7/12 lg:ml-auto relative z-10 bg-stone-50 opacity-0 animate-fade-in-right"
        style="animation-delay: 800ms"
      >
        <nav
          class="sticky top-0 bg-stone-50/90 backdrop-blur-md px-6 py-4 lg:px-12 lg:py-6 flex justify-between items-center z-50 border-b border-stone-200/50"
        >
          <div class="text-xl font-serif font-bold lg:hidden">A & S</div>
          <div
            class="hidden lg:flex space-x-8 text-xs font-bold tracking-[0.15em] text-stone-400 uppercase"
          >
            <a href="#details" class="hover:text-stone-900 transition-colors"
              >Details</a
            >
            <a href="#gallery" class="hover:text-stone-900 transition-colors"
              >Gallery</a
            >
            <a href="#location" class="hover:text-stone-900 transition-colors"
              >Location</a
            >
          </div>
          <button
            @click="showRsvp = true"
            class="bg-stone-800 text-white px-6 py-2 lg:px-8 lg:py-3 rounded-full text-xs font-bold tracking-widest hover:bg-stone-700 transition-all transform hover:-translate-y-0.5 shadow-lg cursor-pointer"
          >
            RSVP
          </button>
        </nav>

        <main class="px-6 py-12 lg:px-24 lg:py-20 max-w-4xl mx-auto">
          <div
            class="lg:hidden mb-12 rounded-xl overflow-hidden relative h-[60vh]"
          >
            <img
              src="https://images.unsplash.com/photo-1519741497674-611481863552?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
              class="absolute inset-0 w-full h-full object-cover"
            />
            <div
              class="absolute inset-0 bg-black/40 flex flex-col justify-end p-8 text-white text-center"
            >
              <h1 class="text-5xl font-serif mb-2">Alex & Sarah</h1>
              <p class="text-sm tracking-widest">2026. 10. 24</p>
            </div>
          </div>

          <section id="details" class="mb-24 text-center">
            <div
              class="hidden lg:block w-[1px] bg-stone-800 h-16 mx-auto mb-8"
            ></div>
            <h2 class="text-3xl lg:text-4xl font-serif mb-8 text-stone-800">
              誠摯邀請
            </h2>
            <p
              class="text-stone-500 leading-loose text-base lg:text-lg mb-8 max-w-2xl mx-auto font-light"
            >
              在這美好的日子裡，我們想與最親愛的您分享這份喜悅。<br />
              誠摯邀請您與家人一同見證我們的愛情旅程。
            </p>

            <div
              class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-16 border-t border-b border-stone-200 py-12"
            >
              <div class="text-center group cursor-default">
                <div
                  class="text-3xl mb-3 transform group-hover:-translate-y-1 transition-transform"
                >
                  🥂
                </div>
                <h3
                  class="font-bold text-stone-800 tracking-widest text-sm uppercase"
                >
                  Reception
                </h3>
                <p class="text-stone-400 text-sm mt-1 font-serif italic">
                  17:30
                </p>
              </div>
              <div
                class="text-center md:border-l md:border-r border-stone-200 group cursor-default"
              >
                <div
                  class="text-3xl mb-3 transform group-hover:-translate-y-1 transition-transform"
                >
                  💍
                </div>
                <h3
                  class="font-bold text-stone-800 tracking-widest text-sm uppercase"
                >
                  Ceremony
                </h3>
                <p class="text-stone-400 text-sm mt-1 font-serif italic">
                  18:00
                </p>
              </div>
              <div class="text-center group cursor-default">
                <div
                  class="text-3xl mb-3 transform group-hover:-translate-y-1 transition-transform"
                >
                  🍽️
                </div>
                <h3
                  class="font-bold text-stone-800 tracking-widest text-sm uppercase"
                >
                  Banquet
                </h3>
                <p class="text-stone-400 text-sm mt-1 font-serif italic">
                  18:30
                </p>
              </div>
            </div>
          </section>

          <section id="gallery" class="mb-24">
            <h2 class="text-3xl font-serif mb-12 text-center text-stone-800">
              Our Moments
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
              <div class="space-y-6">
                <img
                  src="https://images.unsplash.com/photo-1681605011813-0fbe143ccd69?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                  class="w-full rounded-sm shadow-md hover:shadow-xl hover:opacity-95 transition-all duration-500 cursor-pointer"
                />
                <img
                  src="https://images.unsplash.com/photo-1581629779584-0aa1621f7d01?q=80&w=1470&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                  class="w-full rounded-sm shadow-md hover:shadow-xl hover:opacity-95 transition-all duration-500 cursor-pointer"
                />
              </div>
              <div class="space-y-6 md:pt-16">
                <img
                  src="https://images.unsplash.com/photo-1552061056-83b758da8cb3?q=80&w=1405&auto=format&fit=crop&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
                  class="w-full rounded-sm shadow-md hover:shadow-xl hover:opacity-95 transition-all duration-500 cursor-pointer"
                />
                <div
                  class="bg-stone-100 h-64 rounded-sm flex items-center justify-center text-stone-400 font-serif text-2xl p-8 text-center leading-relaxed italic"
                >
                  "We loved with a love that was more than love."
                </div>
              </div>
            </div>
          </section>

          <footer
            class="mt-24 text-center text-stone-300 text-xs tracking-widest uppercase pb-10"
          >
            <p>© 2026 Musubi Wedding System</p>
          </footer>
        </main>
      </div>
      <RsvpDialog v-model:open="showRsvp" />
    </div>
  </UApp>
</template>

<script setup lang="ts">
useHead({
  title: 'Alex & Sarah Wedding',
  link: [
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Lato:wght@300;400;700&family=Playfair+Display:ital,wght@0,400;0,700;1,400&display=swap',
    },
  ],
});

const showRsvp = ref(false);
</script>
