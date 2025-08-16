
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>UGA FEST — Aggro Traders Company</title>

  <!-- Tailwind (CDN) so you can edit without any build tools -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: { sans: ["ui-sans-serif", "system-ui", "-apple-system", "Segoe UI", "Roboto", "Ubuntu", "Noto Sans", "Cantarell", "Helvetica Neue", "Arial", "sans-serif"] },
        }
      }
    }
  </script>

  <!-- Lucide icons (non‑React) -->
  <script defer src="https://unpkg.com/lucide@latest/dist/umd/lucide.js"></script>

  <style>
    /* Simple helper so sections don't hide under sticky nav */
    section[id] { scroll-margin-top: 80px; }
  </style>
</head>
<body class="font-sans antialiased text-gray-900" id="top">

  <!-- ====== QUICK SETTINGS (edit these values) ====== -->
  <script>
    // EDIT ME ↓↓↓
    const SETTINGS = {
      eventTitle: "UGA FEST",
      // Uganda Independence Day is Oct 9 – adjust time and timezone as needed
      eventDateISO: "2025-10-09T10:00:00", 
      venueName: "(Set Venue)", // e.g., Kololo Airstrip
      venueAddress: "Kampala, Uganda",
      googleMapsLink: "https://www.google.com/maps/search/?api=1&query=Kampala%2C%20Uganda",
      organizer: "Aggro Traders Company",
      contactPhone: "+256 000 000 000",
      contactEmail: "info@aggrotraders.co.ug",
      tickets: [
        { name: "Early Bird", price: "UGX 25,000", includes: ["Day access", "Sports participation", "General party entry"], cta: "Buy Early Bird" },
        { name: "Standard", price: "UGX 40,000", includes: ["Full day access", "Participation kit", "Party + DJ set"], cta: "Buy Standard" },
        { name: "VIP Night", price: "UGX 100,000", includes: ["VIP lounge", "Priority bar", "Backstage photo op"], cta: "Buy VIP" },
      ],
      schedule: [
        { time: "10:00", title: "Gates Open & Registration", blurb: "Check in, collect wristbands and participation kits.", icon: "info" },
        { time: "11:00", title: "Community Run (5 km)", blurb: "All levels welcome. Medics & water points on route.", icon: "dumbbell" },
        { time: "13:00", title: "Football 5-a-side Heats", blurb: "Mixed teams; knockout rounds in the afternoon.", icon: "dumbbell" },
        { time: "15:30", title: "Basketball 3×3 & Tug of War", blurb: "Courtside MC, instant brackets, prizes for winners.", icon: "dumbbell" },
        { time: "18:30", title: "Sunset Ceremony & Awards", blurb: "Recognition of teams, partners, and community leaders.", icon: "shield-check" },
        { time: "20:00 → late", title: "UGA FEST Night Party (DJ Line‑up)", blurb: "Main stage lights on. Dance until late! Age 18+ after 20:00.", icon: "music" },
      ],
    };
  </script>

  <!-- ====== NAVBAR ====== -->
  <header class="sticky top-0 z-50 bg-white/80 backdrop-blur border-b border-gray-100">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 flex h-16 items-center justify-between">
      <a href="#top" class="flex items-center gap-2 font-bold">
        <span class="inline-grid h-8 w-8 place-items-center rounded-xl bg-purple-600 text-white">UF</span>
        <span id="brand-title">UGA FEST</span>
      </a>
      <nav class="hidden md:flex items-center gap-6 text-sm text-gray-700">
        <a href="#about" class="hover:text-gray-900">About</a>
        <a href="#activities" class="hover:text-gray-900">Activities</a>
        <a href="#schedule" class="hover:text-gray-900">Schedule</a>
        <a href="#tickets" class="hover:text-gray-900">Tickets</a>
        <a href="#venue" class="hover:text-gray-900">Venue</a>
        <a href="#faqs" class="hover:text-gray-900">FAQs</a>
        <a href="#contact" class="hover:text-gray-900">Contact</a>
      </nav>
      <a href="#tickets" class="inline-flex items-center justify-center gap-2 rounded-2xl bg-purple-600 px-5 py-3 text-sm font-semibold text-white shadow-sm transition hover:bg-purple-700">
        <i data-lucide="ticket" class="h-4 w-4"></i> Buy Tickets
      </a>
    </div>
  </header>

  <!-- ====== HERO ====== -->
  <section class="relative isolate overflow-hidden bg-gradient-to-br from-purple-700 via-fuchsia-600 to-rose-500 text-white">
    <div aria-hidden class="absolute inset-0 bg-[radial-gradient(circle_at_20%_10%,rgba(255,255,255,0.15),transparent_50%),radial-gradient(circle_at_80%_50%,rgba(255,255,255,0.12),transparent_50%)]"></div>
    <div class="relative z-10 mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-24 sm:py-32">
      <span class="inline-flex items-center gap-2 rounded-full bg-white/10 px-3 py-1 text-sm font-medium ring-1 ring-white/20 backdrop-blur">
        <i data-lucide="shield-check" class="h-4 w-4"></i>
        <span id="presented-by">Presented by Aggro Traders Company</span>
      </span>
      <h1 class="mt-6 text-4xl font-black tracking-tight sm:text-6xl" id="hero-title">UGA FEST: Sports Day & Night Party</h1>
      <p class="mt-5 text-lg/8 text-white/90 max-w-3xl">
        A full-day celebration of Uganda's independence — community sports, local food & crafts, and a high-energy night party with top DJs.
      </p>
      <div class="mt-8 flex flex-wrap items-center gap-3 text-white/90">
        <span class="inline-flex items-center gap-2 rounded-full bg-white/10 px-3 py-1 text-sm font-medium ring-1 ring-white/20"><i data-lucide="calendar" class="h-4 w-4"></i> <span id="hero-datetime">Date & time</span></span>
        <span class="inline-flex items-center gap-2 rounded-full bg-white/10 px-3 py-1 text-sm font-medium ring-1 ring-white/20"><i data-lucide="map-pin" class="h-4 w-4"></i> <span id="hero-venue">Venue · Address</span></span>
      </div>

      <!-- Countdown -->
      <div class="mt-8 grid w-full max-w-xl grid-cols-4 gap-2 sm:gap-3">
        <div class="rounded-2xl bg-white/10 p-4 text-center ring-1 ring-white/20">
          <div id="cd-days" class="text-3xl font-black">00</div>
          <div class="text-xs uppercase tracking-wider text-white/80">Days</div>
        </div>
        <div class="rounded-2xl bg-white/10 p-4 text-center ring-1 ring-white/20">
          <div id="cd-hours" class="text-3xl font-black">00</div>
          <div class="text-xs uppercase tracking-wider text-white/80">Hours</div>
        </div>
        <div class="rounded-2xl bg-white/10 p-4 text-center ring-1 ring-white/20">
          <div id="cd-minutes" class="text-3xl font-black">00</div>
          <div class="text-xs uppercase tracking-wider text-white/80">Minutes</div>
        </div>
        <div class="rounded-2xl bg-white/10 p-4 text-center ring-1 ring-white/20">
          <div id="cd-seconds" class="text-3xl font-black">00</div>
          <div class="text-xs uppercase tracking-wider text-white/80">Seconds</div>
        </div>
      </div>

      <div class="mt-8 flex flex-wrap items-center gap-3">
        <a href="#tickets" class="inline-flex items-center gap-2 rounded-2xl bg-purple-900/40 px-5 py-3 font-semibold text-white ring-1 ring-white/20 transition hover:bg-purple-900/60"><i data-lucide="ticket" class="h-4 w-4"></i> Get Tickets</a>
        <a id="directions-link" href="#" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-2xl bg-white/10 px-5 py-3 font-semibold text-white ring-1 ring-white/20 transition hover:bg-white/20"><i data-lucide="navigation" class="h-4 w-4"></i> Get Directions</a>
      </div>
    </div>
  </section>

  <!-- ====== ABOUT ====== -->
  <section id="about" class="py-16 sm:py-20 bg-gray-50">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">About the Festival</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">A community-first celebration of independence</h2>
        <p class="mt-4 text-gray-600">UGA FEST is a day‑long experience that brings together sports lovers, families, creators and party people to celebrate Uganda's spirit. Organized by <span id="org-name">Aggro Traders Company</span>, the festival blends friendly competition with music, food, and culture.</p>
      </div>
      <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-purple-50 p-3 text-purple-700"><i data-lucide="dumbbell" class="h-6 w-6"></i></div>
            <div>
              <h3 class="text-lg font-semibold">Sports Arena</h3>
              <p class="mt-1 text-gray-600">5 km Run, 5‑a‑side football, 3×3 basketball, tug of war, fun drills — all levels welcome.</p>
            </div>
          </div>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-purple-50 p-3 text-purple-700"><i data-lucide="music" class="h-6 w-6"></i></div>
            <div>
              <h3 class="text-lg font-semibold">Night Party</h3>
              <p class="mt-1 text-gray-600">Main stage DJs, live acts and dance until late. VIP lounge available.</p>
            </div>
          </div>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-purple-50 p-3 text-purple-700"><i data-lucide="users" class="h-6 w-6"></i></div>
            <div>
              <h3 class="text-lg font-semibold">Family & Community</h3>
              <p class="mt-1 text-gray-600">Kids' zone, market stalls, local food & crafts, community awards.</p>
            </div>
          </div>
        </div></div>
      </div>
    </div>
  </section>

  <!-- ====== ACTIVITIES ====== -->
  <section id="activities" class="py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">Activities</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Sports by day, party by night</h2>
        <p class="mt-4 text-gray-600">Join solo, bring a team, or just cheer from the sidelines. Then switch to party mode after sunset.</p>
      </div>
      <div class="grid gap-6 lg:grid-cols-2">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-emerald-50 p-3 text-emerald-700"><i data-lucide="dumbbell" class="h-6 w-6"></i></div>
            <div>
              <h3 class="text-lg font-semibold">Sports Zone</h3>
              <ul class="mt-2 list-disc pl-5 text-gray-700">
                <li>Community Run (5 km) — chip timing optional</li>
                <li>Football 5‑a‑side — mixed teams, quick games</li>
                <li>Basketball 3×3 — courtside MC & brackets</li>
                <li>Fun challenges — tug of war, sack race, skills</li>
              </ul>
              <p class="mt-3 text-sm text-gray-500">Bring sportswear. Water stations and medics on site.</p>
            </div>
          </div>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-pink-50 p-3 text-pink-700"><i data-lucide="music" class="h-6 w-6"></i></div>
            <div>
              <h3 class="text-lg font-semibold">Night Party</h3>
              <p class="mt-2 text-gray-700">Main stage DJs with Afrobeat, Amapiano, Dancehall. Light shows, photo booths, VIP lounge.</p>
              <p class="mt-3 text-sm text-gray-500">Age 18+ after 20:00. Security screening applies.</p>
            </div>
          </div>
        </div></div>
      </div>
    </div>
  </section>

  <!-- ====== SCHEDULE ====== -->
  <section id="schedule" class="py-16 sm:py-20 bg-gray-50">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">Schedule</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Plan your day</h2>
        <p class="mt-4 text-gray-600">Times may slightly adjust. Arrive early for registration.</p>
      </div>
      <ol id="schedule-list" class="relative ml-4 border-l border-gray-200"></ol>
    </div>
  </section>

  <!-- ====== TICKETS & PAYMENT ====== -->
  <section id="tickets" class="py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">Tickets & Payment</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Choose your pass</h2>
        <p class="mt-4 text-gray-600">Secure your spot. Limited early bird tickets available.</p>
      </div>
      <div id="ticket-grid" class="grid gap-6 lg:grid-cols-3"></div>

      <div id="payment" class="mt-10 grid gap-6 lg:grid-cols-2">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-yellow-50 p-3 text-yellow-700"><i data-lucide="wallet" class="h-6 w-6"></i></div>
            <div class="flex-1">
              <h3 class="text-lg font-semibold">Mobile Money</h3>
              <p class="mt-2 text-gray-700">Pay via MTN/Airtel Mobile Money, then upload your receipt during check‑in.</p>
              <div class="mt-4 grid gap-3 text-sm">
                <div class="rounded-xl bg-gray-50 p-3"><strong>MTN MoMo:</strong> 256‑XXX‑XXX (UGA FEST)</div>
                <div class="rounded-xl bg-gray-50 p-3"><strong>Airtel Money:</strong> 256‑YYY‑YYY (UGA FEST)</div>
                <div class="rounded-xl bg-gray-50 p-3"><strong>Reference:</strong> Use your phone number</div>
              </div>
              <a href="#contact" class="mt-4 inline-flex items-center gap-2 text-sm font-semibold text-purple-700 hover:underline"><i data-lucide="info" class="h-4 w-4"></i> Need help with payment?</a>
            </div>
          </div>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-blue-50 p-3 text-blue-700"><i data-lucide="credit-card" class="h-6 w-6"></i></div>
            <div class="flex-1">
              <h3 class="text-lg font-semibold">Bank Transfer / Card</h3>
              <p class="mt-2 text-gray-700">For bank transfers or online card payments, use the details below.</p>
              <div class="mt-4 grid gap-3 text-sm">
                <div class="rounded-xl bg-gray-50 p-3"><strong>Account Name:</strong> Aggro Traders Company</div>
                <div class="rounded-xl bg-gray-50 p-3"><strong>Bank:</strong> (Add bank name)</div>
                <div class="rounded-xl bg-gray-50 p-3"><strong>Account No. / IBAN:</strong> (Add account no.)</div>
                <div class="rounded-xl bg-gray-50 p-3"><strong>SWIFT / Branch:</strong> (Add code)</div>
              </div>
              <div class="mt-4 flex flex-wrap items-center gap-2 text-xs text-gray-500">
                <i data-lucide="shield-check" class="h-4 w-4"></i> Payments processed securely. Keep your confirmation email/SMS.
              </div>
            </div>
          </div>
        </div></div>
      </div>
    </div>
  </section>

  <!-- ====== VENUE ====== -->
  <section id="venue" class="py-16 sm:py-20 bg-gray-50">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">Venue</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Where to find us</h2>
        <p class="mt-4 text-gray-600">Plan your route and arrive early. On‑site parking is limited; rideshare recommended.</p>
      </div>
      <div class="grid gap-6 lg:grid-cols-2">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <div class="flex items-start gap-4">
            <div class="rounded-2xl bg-purple-50 p-3 text-purple-700"><i data-lucide="map-pin" class="h-6 w-6"></i></div>
            <div>
              <h3 id="venue-name" class="text-lg font-semibold">(Set Venue)</h3>
              <p id="venue-address" class="mt-1 text-gray-600">Kampala, Uganda</p>
              <div class="mt-4 flex flex-wrap items-center gap-3">
                <a id="maps-open" href="#" target="_blank" rel="noreferrer" class="inline-flex items-center gap-2 rounded-xl bg-gray-900 px-4 py-2 font-semibold text-white transition hover:bg-black"><i data-lucide="navigation" class="h-4 w-4"></i> Open in Google Maps</a>
                <a href="#faqs" class="inline-flex items-center gap-2 rounded-xl bg-white px-4 py-2 font-semibold text-gray-900 ring-1 ring-gray-200 hover:bg-gray-50"><i data-lucide="info" class="h-4 w-4"></i> Travel & entry info</a>
              </div>
            </div>
          </div>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm overflow-hidden">
          <div class="aspect-video w-full">
            <iframe title="Map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d63831.72077264047!2d32.546!3d0.315!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x177dbbc3f2c439a7%3A0x4f4ff09f0f7b4c7e!2sKampala%2C%20Uganda!5e0!3m2!1sen!2sug!4v1710000000000" width="600" height="450" style="border:0" allowfullscreen loading="lazy" referrerpolicy="no-referrer-when-downgrade" class="h-full w-full"></iframe>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ====== FAQs ====== -->
  <section id="faqs" class="py-16 sm:py-20">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">FAQs</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Good to know</h2>
      </div>
      <div class="grid gap-6 lg:grid-cols-2">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <h3 class="text-base font-semibold">What should I bring?</h3>
          <p class="mt-2 text-gray-600">Valid ID, mobile phone (for e‑tickets), sportswear, sun protection, and cashless payment method.</p>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <h3 class="text-base font-semibold">Age policy?</h3>
          <p class="mt-2 text-gray-600">Family‑friendly all day. After 20:00 the party is strictly 18+ with ID checks.</p>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <h3 class="text-base font-semibold">Can I buy tickets on the day?</h3>
          <p class="mt-2 text-gray-600">Yes, if not sold out. We recommend purchasing online in advance to secure your spot.</p>
        </div></div>
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
          <h3 class="text-base font-semibold">Accessibility?</h3>
          <p class="mt-2 text-gray-600">Accessible entry and viewing areas available. Contact us for specific accommodations.</p>
        </div></div>
      </div>
    </div>
  </section>

  <!-- ====== CONTACT ====== -->
  <section id="contact" class="py-16 sm:py-20 bg-gray-50">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8">
      <div class="mb-10 max-w-3xl">
        <p class="mb-2 text-sm font-semibold uppercase tracking-widest text-purple-600">Contact</p>
        <h2 class="text-3xl font-bold tracking-tight sm:text-4xl">Talk to us</h2>
        <p class="mt-4 text-gray-600">For partnerships, team registrations, media passes or vendor stalls, drop us a line.</p>
      </div>
      <div class="grid gap-6 lg:grid-cols-3">
        <div class="rounded-2xl border border-gray-200 bg-white shadow-sm lg:col-span-2"><div class="p-6 sm:p-8">
          <form onsubmit="event.preventDefault(); alert('Thanks! We received your message.');" class="grid gap-4 sm:grid-cols-2">
            <div>
              <label class="mb-1 block text-sm font-medium">Full name</label>
              <input class="w-full rounded-xl border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-purple-500" required>
            </div>
            <div>
              <label class="mb-1 block text-sm font-medium">Email</label>
              <input type="email" class="w-full rounded-xl border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-purple-500" required>
            </div>
            <div class="sm:col-span-2">
              <label class="mb-1 block text-sm font-medium">Message</label>
              <textarea rows="4" class="w-full rounded-xl border border-gray-300 px-3 py-2 focus:outline-none focus:ring-2 focus:ring-purple-500" placeholder="Sponsorship inquiry, team registration, etc." required></textarea>
            </div>
            <button type="submit" class="inline-flex items-center justify-center gap-2 rounded-2xl bg-purple-600 px-5 py-3 font-semibold text-white transition hover:bg-purple-700"><i data-lucide="mail" class="h-4 w-4"></i> Send message</button>
          </form>
        </div></div>
        <div class="grid gap-6">
          <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
            <h3 class="text-base font-semibold">Organizer</h3>
            <p id="org-box-name" class="mt-1 text-gray-600">Aggro Traders Company</p>
            <div class="mt-3 grid gap-2 text-sm text-gray-700">
              <div class="flex items-center gap-2"><i data-lucide="phone" class="h-4 w-4"></i> <span id="org-phone">+256 000 000 000</span></div>
              <div class="flex items-center gap-2"><i data-lucide="mail" class="h-4 w-4"></i> <span id="org-email">info@aggrotraders.co.ug</span></div>
              <div class="flex items-center gap-2"><i data-lucide="globe" class="h-4 w-4"></i> <a href="#" class="underline decoration-dotted">Website</a></div>
            </div>
          </div></div>
          <div class="rounded-2xl border border-gray-200 bg-white shadow-sm"><div class="p-6 sm:p-8">
            <h3 class="text-base font-semibold">Follow updates</h3>
            <div class="mt-3 flex items-center gap-3">
              <a aria-label="Instagram" href="#" class="rounded-full p-2 ring-1 ring-gray-200 hover:bg-gray-50"><i data-lucide="instagram" class="h-5 w-5"></i></a>
              <a aria-label="Facebook" href="#" class="rounded-full p-2 ring-1 ring-gray-200 hover:bg-gray-50"><i data-lucide="facebook" class="h-5 w-5"></i></a>
              <a aria-label="Twitter/X" href="#" class="rounded-full p-2 ring-1 ring-gray-200 hover:bg-gray-50"><i data-lucide="twitter" class="h-5 w-5"></i></a>
            </div>
            <p class="mt-3 text-sm text-gray-600">Share with <span class="font-semibold">#UGAFEST</span></p>
          </div></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ====== FOOTER ====== -->
  <footer class="border-t border-gray-100 bg-white py-10 text-sm">
    <div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 flex flex-col items-center justify-between gap-4 sm:flex-row">
      <p class="text-gray-600">© <span id="year"></span> <span id="org-foot">Aggro Traders Company</span>. All rights reserved.</p>
      <div class="flex flex-wrap items-center gap-4 text-gray-600">
        <a href="#tickets" class="hover:text-gray-900">Tickets</a>
        <a href="#venue" class="hover:text-gray-900">Venue</a>
        <a href="#faqs" class="hover:text-gray-900">FAQs</a>
        <a href="#contact" class="hover:text-gray-900">Contact</a>
      </div>
    </div>
  </footer>

  <!-- ====== PAGE SCRIPT (vanilla JS) ====== -->
  <script>
    // Fill basic text from SETTINGS
    document.getElementById('brand-title').textContent = SETTINGS.eventTitle;
    document.getElementById('presented-by').textContent = `Presented by ${SETTINGS.organizer}`;
    document.getElementById('hero-title').textContent = `${SETTINGS.eventTitle}: Sports Day & Night Party`;
    document.getElementById('org-name').textContent = SETTINGS.organizer;
    document.getElementById('org-box-name').textContent = SETTINGS.organizer;
    document.getElementById('org-foot').textContent = SETTINGS.organizer;
    document.getElementById('org-phone').textContent = SETTINGS.contactPhone;
    document.getElementById('org-email').textContent = SETTINGS.contactEmail;
    document.getElementById('venue-name').textContent = SETTINGS.venueName;
    document.getElementById('venue-address').textContent = SETTINGS.venueAddress;
    document.getElementById('year').textContent = new Date().getFullYear();

    // Date/time + links
    const dt = new Date(SETTINGS.eventDateISO);
    const dtText = dt.toLocaleString(undefined, { dateStyle: 'full', timeStyle: 'short' });
    document.getElementById('hero-datetime').textContent = dtText;
    document.getElementById('hero-venue').textContent = `${SETTINGS.venueName} · ${SETTINGS.venueAddress}`;
    document.getElementById('directions-link').href = SETTINGS.googleMapsLink;
    document.getElementById('maps-open').href = SETTINGS.googleMapsLink;

    // Countdown
    function updateCountdown() {
      const target = dt.getTime();
      const now = Date.now();
      const diff = Math.max(0, target - now);
      const days = Math.floor(diff / (1000*60*60*24));
      const hours = Math.floor((diff / (1000*60*60)) % 24);
      const minutes = Math.floor((diff / (1000*60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);
      const pad = (n) => String(n).padStart(2, '0');
      document.getElementById('cd-days').textContent = pad(days);
      document.getElementById('cd-hours').textContent = pad(hours);
      document.getElementById('cd-minutes').textContent = pad(minutes);
      document.getElementById('cd-seconds').textContent = pad(seconds);
    }
    updateCountdown();
    setInterval(updateCountdown, 1000);

    // Tickets
    const ticketGrid = document.getElementById('ticket-grid');
    SETTINGS.tickets.forEach(tier => {
      const card = document.createElement('div');
      card.className = 'rounded-2xl border border-gray-200 bg-white shadow-sm';
      card.innerHTML = `
        <div class="p-6 sm:p-8">
          <h3 class="text-lg font-semibold">${tier.name}</h3>
          <div class="mt-2 text-3xl font-black">${tier.price}</div>
          <ul class="mt-4 space-y-2 text-gray-700">
            ${tier.includes.map(it => `<li class='flex items-start gap-2'><i data-lucide="shield-check" class="h-4 w-4 mt-0.5 text-emerald-600"></i><span>${it}</span></li>`).join('')}
          </ul>
          <a href="#payment" class="mt-6 inline-flex w-full items-center justify-center gap-2 rounded-xl bg-purple-600 px-4 py-2 font-semibold text-white transition hover:bg-purple-700"><i data-lucide="ticket" class="h-4 w-4"></i> ${tier.cta}</a>
        </div>`;
      ticketGrid.appendChild(card);
    });

    // Schedule
    const sched = document.getElementById('schedule-list');
    SETTINGS.schedule.forEach((item, idx) => {
      const li = document.createElement('li');
      li.className = 'mb-8 ml-6 relative';
      li.innerHTML = `
        <span class="absolute -left-3 flex h-6 w-6 items-center justify-center rounded-full bg-purple-600 text-white ring-8 ring-white">
          <i data-lucide="${item.icon}" class="h-3.5 w-3.5"></i>
        </span>
        <time class="text-sm font-semibold text-purple-700">${item.time}</time>
        <h3 class="mt-1 text-lg font-semibold">${item.title}</h3>
        <p class="mt-1 text-gray-600">${item.blurb}</p>`;
      sched.appendChild(li);
    });

    // Initialize icons after dynamic content is in the DOM
    window.addEventListener('load', () => {
      if (window.lucide && lucide.createIcons) { lucide.createIcons(); }
    });
  </script>
</body>
</html>
			
