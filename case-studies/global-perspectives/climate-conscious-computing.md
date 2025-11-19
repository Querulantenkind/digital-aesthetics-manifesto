# Climate-Conscious Computing: Sustainable Digital Practices

## Introduction

**Every byte has a carbon cost.**

Digital seems "clean"—no smoke, no waste. But:
- Data centers consume 1-2% of global electricity
- Networks transmit petabytes daily
- Devices require mining, manufacturing, disposal
- Cooling systems run 24/7

**Climate-conscious computing** asks:
- How do we reduce digital's environmental impact?
- Can code be sustainable?
- What does an eco-friendly internet look like?

This case study examines sustainable digital practices: the carbon footprint of computing, design strategies for reduction, the permacomputing movement, and how aesthetics intersect with climate justice.

---

## The Carbon Footprint of Digital

### Data Centers

**Energy consumption:**
- **1-2% of global electricity** (2020-2025)
- Growing rapidly (cloud computing, AI training)
- Equivalent to aviation industry

**Cooling:**
- Servers generate heat
- Cooling = significant energy use
- Water consumption (evaporative cooling)

**Location matters:**
- Iceland, Norway (renewable energy, cold climate)
- vs. coal-powered grids

**Efficiency (PUE - Power Usage Effectiveness):**
- Industry average: ~1.5 (50% overhead)
- Google: ~1.1 (efficient)
- Goal: 1.0 (no overhead)

### Networks

**Data transmission:**
- Every byte travels through routers, switches, undersea cables
- Energy per GB: ~0.06 kWh (2020 estimate)
- Increasing traffic = increasing energy

**5G:**
- Faster speeds
- But: more energy than 4G (initially)
- Infrastructure buildout = embodied carbon

### Devices

**Manufacturing:**
- Mining (rare earth metals)
- Factory production (energy-intensive)
- Transportation

**Use:**
- Laptops: 20-50W
- Desktops: 60-300W
- Phones: 2-5W
- Servers: 200-500W+

**Disposal:**
- E-waste growing (60 million tons/year)
- Toxins leach into soil, water
- Recycling rates low (~20%)

**Embodied carbon:**
- 70-80% of device's lifetime carbon is in manufacturing
- Using device longer = more sustainable
- Repair, not replace

---

## Carbon Cost of Web Pages

### Typical Page Weights (2025)

**Global average:**
- Desktop: ~2.5 MB
- Mobile: ~2.0 MB

**Carbon per page view:**
- ~0.5-1.0g CO2e (average site)
- Heavy site (5 MB): ~2-3g CO2e
- Light site (50 KB): ~0.02g CO2e

**Factors:**
- Page size (bytes)
- Green hosting (renewable energy)
- Caching (repeat visits cheaper)
- User's device efficiency

**Scale:**
- 1 million page views/month:
  - Heavy site: 2-3 tons CO2e/month
  - Light site: 20 kg CO2e/month
  - **100x difference**

### Website Carbon Calculator

**Tools:**
- websitecarbon.com
- Ecograder

**Example:**
- Enter URL
- Estimates CO2 per page view
- Cleaner than X% of sites tested

**Limitations:**
- Estimates (not exact)
- But: directionally correct, raises awareness

---

## Principles of Sustainable Design

### 1. Efficiency

**Optimize everything:**
- Images (compress, WebP/AVIF, responsive)
- CSS (remove unused, minify)
- JavaScript (question necessity, tree-shake, minify)
- Fonts (system fonts or subset web fonts)

**Result:**
- Smaller page size = less data = less energy

### 2. Green Hosting

**Choose providers with:**
- Renewable energy (wind, solar, hydro)
- PUE <1.2 (efficient data centers)
- Carbon offsetting (if renewables not available)

**Examples:**
- **Green Web Foundation directory** (greenweb.org)
- **Providers:** Google Cloud (carbon neutral), OVH (hydropower), Krystal (UK, 100% renewable)

### 3. Caching

**Browser caching:**
- Cache static assets (CSS, JS, images)
- Repeat visits = 0 bytes transferred
- Less energy

**CDNs (Content Delivery Networks):**
- Serve from nearest location
- Reduces transmission distance
- Lower latency, less energy

### 4. Dark Mode

**OLED screens:**
- Black pixels = off = no power
- Dark mode = energy savings (up to 60% on OLED)

**LCD screens:**
- Backlight always on
- Dark mode = minimal savings

**Implementation:**
```css
@media (prefers-color-scheme: dark) {
  body {
    background: #000;
    color: #fff;
  }
}
```

**Note:**
- Offer choice (not everyone prefers dark)
- Maintain accessibility (contrast)

### 5. Longevity

**Design for old devices:**
- No cutting-edge features required
- Works on 5+ year old phones
- Extends device lifespan = less e-waste

**Progressive enhancement:**
- Core content works everywhere
- Enhancements for capable devices

### 6. Static Over Dynamic

**Static sites:**
- Pre-rendered HTML
- No server computation per request
- Serve from CDN (cache)

**Dynamic sites:**
- Database queries
- Server computation
- More energy per request

**Static site generators:**
- Jekyll, Hugo, Eleventy, 11ty
- Build once, serve infinitely

---

## Permacomputing

### What is Permacomputing?

**Permaculture + computing:**
- Sustainable computing principles
- Design for longevity, repair, minimal waste
- Low energy, resilient systems

**Principles:**

**1. Keep it small**
- Minimal code
- Efficient algorithms
- No bloat

**2. Keep it repairable**
- Open source
- Documented
- Modular

**3. Keep it energy-efficient**
- Optimize computation
- Idle when not needed
- Low-power devices

**4. Keep it durable**
- Future-proof formats (plain text)
- Works on old hardware
- Long-term thinking

**5. Embrace limits**
- Constraints = creativity
- "Enough" vs. "more"
- Frugal abundance

### Examples

**CollapseOS:**
- Operating system for post-collapse scenario
- Runs on old hardware (Z80, etc.)
- Bootstrappable (self-hosting)
- Resilient

**Low-Tech Magazine (offline edition):**
- Solar-powered server
- Goes offline when sun down
- Dithered images (low bandwidth)
- Embraces constraints

**XXIIVV (Hundred Rabbits):**
- Developers living on sailboat
- Solar-powered computing
- Build tools that run on limited power
- Resilient, sustainable lifestyle

### Aesthetics

**Permacomputing aesthetic:**
- Minimalist (small code)
- Terminal-based (efficient)
- Retro (old hardware)
- Honest (shows constraints)

---

## Sustainable Coding Practices

### Efficient Algorithms

**Big O matters:**
- O(n²) vs. O(n log n) = huge difference
- Efficient algorithms = less computation = less energy

**Example:**
- Sorting 1 million items:
  - Bubble sort: ~1 trillion operations
  - Quicksort: ~20 million operations
  - 50,000x difference = 50,000x energy

### Lazy Loading

**Load only what's needed:**
- Images below fold → lazy load
- JavaScript modules → load on demand
- Videos → don't autoplay

**Result:**
- User scrolls away = bytes not loaded
- Energy saved

### Debouncing and Throttling

**Limit computation:**
- Debounce search input (wait until user stops typing)
- Throttle scroll events (only fire every 100ms)

**Result:**
- Fewer function calls
- Less CPU work
- Lower energy

### Avoid Polling

**Polling (bad):**
- Check server every X seconds
- Constant network requests
- Energy waste if nothing changed

**Alternatives:**
- WebSockets (server pushes updates)
- Server-Sent Events (SSE)
- Webhooks

### Database Queries

**Optimize:**
- Index properly (fast lookups)
- Avoid N+1 queries (batch)
- Cache results

**Result:**
- Faster queries
- Less server CPU
- Lower energy

### Static Site Generation

**Build once:**
- Generate HTML at build time
- Serve static files
- No server computation per request

**Frameworks:**
- Jekyll (Ruby)
- Hugo (Go, fast)
- Eleventy (JS)
- Gatsby (React)

---

## Design Patterns for Sustainability

### 1. Text-First Design

**Why:**
- Text is smallest (1 KB = ~500 words)
- Fast, accessible, low-carbon

**Examples:**
- Blogs (text + few images)
- News sites (articles, summaries)
- Documentation (mdBook, Docusaurus)

### 2. Monochrome / Limited Color

**Why:**
- Dark mode energy savings (OLED)
- Simpler CSS (smaller files)
- Clear, focused

**Examples:**
- Hacker News (orange + black/white)
- Terminal UIs (green on black)

### 3. System Fonts

**Why:**
- 0 bytes (no download)
- Instant rendering
- Lower energy (no font file transfer)

**Implementation:**
```css
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
```

### 4. Brutalism

**Why:**
- Minimal CSS (<5 KB)
- No images (often)
- Fast, efficient

**Aesthetic:**
- Raw HTML
- High contrast
- Functional

**Examples:**
- Craigslist
- Berkshire Hathaway

### 5. Progressive Web Apps (PWAs)

**Why:**
- Offline capability (service workers)
- Cache assets locally
- Reduce network requests

**Benefits:**
- Repeat visits = near-zero energy (serve from cache)
- Works offline
- Resilient

---

## Green Hosting Providers

### What to Look For

**Renewable energy:**
- Wind, solar, hydro
- Power Purchase Agreements (PPAs)
- On-site generation

**Efficient data centers:**
- Low PUE (<1.2)
- Free cooling (cold climates)
- Heat reuse

**Transparency:**
- Publish energy sources
- Carbon reports
- Certifications

### Examples

**Google Cloud / GCP:**
- Carbon neutral (offsets)
- Matching renewable energy
- Efficient data centers (PUE ~1.1)

**OVH:**
- Hydropower (Canada)
- Water cooling (efficient)
- European provider

**Krystal Hosting (UK):**
- 100% renewable energy
- B Corp certified
- Tree planting

**Infomaniak (Switzerland):**
- 100% renewable energy
- Zero carbon
- Privacy-focused

### Green Web Foundation

**GreenWebCheck:**
- greenweb.org
- Check if a host uses green energy
- Directory of green hosts

---

## The Role of AI and Machine Learning

### Carbon Cost of Training

**Large language models (LLMs):**
- GPT-3: ~552 tons CO2e to train (2020)
- GPT-4: estimates ~1000-2500 tons CO2e
- Equivalent to driving a car millions of miles

**Image generation models:**
- Stable Diffusion, DALL-E: hundreds of tons

**Why so high:**
- Weeks/months of GPU computation
- Thousands of GPUs (each 200-400W)
- Cooling

### Inference Costs

**Every AI query:**
- 0.01-0.1 Wh per query (estimate)
- Billions of queries/day = gigawatt-hours

**Growing rapidly:**
- ChatGPT, Copilot, image generators
- Embedded in apps

### Sustainable AI?

**Strategies:**
- Smaller models (distillation)
- Efficient architectures
- Renewable-powered data centers
- Necessary use (don't use AI for everything)

**Question to ask:**
- Do we need AI for this task?
- Can a simpler algorithm work?
- Is the carbon cost justified?

---

## Case Studies

### Low-Tech Magazine

**lowtechmagazine.com/offline**

**Solar-powered server:**
- Runs on solar panels
- Goes offline when solar power low
- "Site offline" message honest

**Design:**
- Dithered images (1-bit, tiny files)
- Minimal CSS
- System fonts
- Dark mode default (save energy)

**Philosophy:**
- Question tech solutionism
- Embrace constraints
- Sustainable web

**Impact:**
- Sparked conversation
- Inspired others
- Proof of concept

### Hundred Rabbits

**Studio on sailboat:**
- Developers Devine Lu Linvega & Rekka Bellum
- Live on sailboat (off-grid)
- Solar power only

**Tools they built:**
- **Orca** (music sequencer)
- **Left** (text editor)
- **Ronin** (graphic design tool)
- All: low-power, efficient, runs on Raspberry Pi

**Philosophy:**
- Permacomputing
- Resilience
- Minimalism
- DIY culture

**Aesthetic:**
- Terminal-based
- Pixel art
- Retro, functional

### Organic Basics (Sustainable Fashion E-Commerce)

**Low-impact website:**
- Optimized images (WebP)
- Lazy loading
- Green hosting
- Carbon calculator on site

**Message:**
- Sustainability = brand value
- Website reflects values
- Transparency

### Ecosia (Search Engine)

**Carbon-positive:**
- Ad revenue funds tree planting
- 45+ million trees planted (as of 2020s)
- Renewable-powered servers
- Financial transparency

**Business model:**
- Search → ads → trees
- Carbon-positive (removes more CO2 than emits)

---

## Criticisms and Challenges

### "Greenwashing"

**Issue:**
- Companies claim "green" without substance
- Carbon offsets = paying to pollute elsewhere
- Renewable energy claims (not always accurate)

**How to verify:**
- Look for certifications (B Corp, etc.)
- Transparency reports
- Third-party audits

### Accessibility Trade-offs?

**Concern:**
- Low-carbon design = minimal images, CSS
- Could hurt accessibility (color contrast, font size)

**Response:**
- Accessibility and sustainability **align**
- High contrast = clear design
- System fonts = fast + accessible
- Text-first = screen reader friendly

**No trade-off necessary.**

### User Experience?

**Concern:**
- Sustainable sites = ugly, slow, boring

**Response:**
- Craigslist = $1B/year (simple works)
- Hacker News = beloved (fast, focused)
- Low-Tech Magazine = beautiful (dithering aesthetic)

**Sustainability ≠ bad UX.**

### Individual vs. Systemic Change

**Reality:**
- Individual web developer's impact = small
- Data centers, ISPs, device manufacturers = large
- Systemic change needed

**But:**
- Every site matters (1M views = tons CO2)
- Cultural shift (awareness)
- Design practices influence industry

**Both/and, not either/or.**

---

## The Future: Carbon-Aware Computing

### Carbon-Aware Scheduling

**Idea:**
- Run computations when grid carbon-intensity low
- Delay non-urgent tasks (backups, AI training) to times when renewable energy abundant

**Example:**
- Google: Shift compute to times/locations with more renewable energy

**Benefits:**
- Same work, lower carbon
- No user-facing change

### Edge Computing

**Move computation closer to user:**
- Less data transmitted
- Lower latency
- Energy savings

**Example:**
- CDN edge functions (Cloudflare Workers, etc.)

### Serverless and Efficiency

**Serverless functions:**
- Pay per execution
- Idle = no energy
- Efficient scaling

**But:**
- Cold starts = energy cost
- Trade-offs exist

### Legislation and Standards

**Emerging:**
- EU: Right to Repair
- France: Carbon labels for digital services
- Regulations on e-waste

**Future:**
- Carbon budgets for sites?
- Mandatory efficiency standards?
- Incentives for green hosting?

---

## The Aesthetics of Sufficiency

### "Enough" vs. "More"

**Consumer culture:**
- More features
- More pixels
- More animations
- More data

**Sufficiency:**
- Enough features
- Enough quality
- Enough design
- Enough data

**Aesthetic of restraint.**

### Wabi-Sabi (Japanese Aesthetics)

**Principles:**
- Imperfection
- Impermanence
- Incompleteness

**Digital application:**
- No need for perfection (pixel-perfect)
- Embrace constraints (dithered images)
- Simplicity over complexity

### Frugal Abundance

**Not deprivation:**
- Rich experience with minimal resources
- Quality over quantity
- Joy in simplicity

**Examples:**
- Hacker News (text, yet vibrant community)
- Wikipedia (minimal design, infinite knowledge)
- Craigslist (plain, yet useful)

---

## Conclusion

**Climate-conscious computing is urgent.**

**The stakes:**
- Digital's carbon footprint growing
- Climate crisis accelerating
- We must act

**Core practices:**
- **Efficiency** (optimize everything)
- **Green hosting** (renewable energy)
- **Longevity** (design for old devices)
- **Static over dynamic** (pre-render)
- **Permacomputing** (sustainable, resilient systems)

**Aesthetic outcomes:**
- Text-first design
- Minimalism (brutalism, terminal UIs)
- System fonts
- Dark mode (OLED savings)
- Dithered images (Low-Tech Magazine)

**Philosophy:**
- Sufficiency over excess
- Constraint as creativity
- Sustainability as beauty

**The lesson:**
**Sustainable design is good design.** Low-carbon sites are fast, accessible, resilient, and often more beautiful.

**Code sustainably. Protect the planet.**

---

## Further Resources

### Tools
- Website Carbon: websitecarbon.com
- Ecograder: ecograder.com
- Green Web Check: greenweb.org

### Organizations
- Green Web Foundation: thegreenwebfoundation.org
- Sustainable Web Manifesto: sustainablewebmanifesto.com
- Climate Action Tech: climateaction.tech

### Reading
- *Designing for Sustainability* by Tim Frick
- Low-Tech Magazine: lowtechmagazine.com
- Permacomputing Wiki: permacomputing.net

### Communities
- ClimateAction.tech Slack
- r/permacomputing (Reddit)
- Hundred Rabbits: 100r.co

---

**Case Study Type:** Global Perspectives  
**Author:** Digital Aesthetics Manifesto Contributors  
**Date:** November 19, 2025  
**License:** CC-BY-SA 4.0
