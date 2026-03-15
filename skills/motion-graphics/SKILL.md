---
name: motion-graphics
description: Create animations using CSS keyframes, GSAP, Lottie/bodymovin, and JavaScript. Use when user asks to create animations, animated elements, loading spinners, scroll animations, page transitions, micro-interactions, animated backgrounds, Lottie animations, GSAP timelines, or any motion design for web.
license: MIT
metadata:
  version: 1.0.0
  author: Sam
  category: design
  domain: animation
  updated: 2026-02-25
  tech-stack: CSS, GSAP, Lottie, JavaScript
---

# Motion Graphics

Create professional web animations: CSS keyframes, GSAP, Lottie, scroll effects, and micro-interactions.

---

## Keywords

animation, css animation, keyframes, gsap, lottie, bodymovin, motion design, scroll animation, page transition, micro-interaction, loading animation, hover effect, animated background, parallax, motion graphics, web animation

---

## Core Workflows

### Workflow 1: CSS Keyframe Animations

```css
/* Fade In Up */
@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
.animate-fade-in-up {
  animation: fadeInUp 0.6s ease-out forwards;
}

/* Slide In from Left */
@keyframes slideInLeft {
  from { opacity: 0; transform: translateX(-60px); }
  to { opacity: 1; transform: translateX(0); }
}

/* Scale Bounce */
@keyframes scaleBounce {
  0% { transform: scale(0); }
  60% { transform: scale(1.1); }
  100% { transform: scale(1); }
}

/* Gradient Shift (Background) */
@keyframes gradientShift {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}
.animated-gradient {
  background: linear-gradient(-45deg, #6366f1, #ec4899, #06b6d4, #8b5cf6);
  background-size: 400% 400%;
  animation: gradientShift 6s ease infinite;
}

/* Pulse Glow */
@keyframes pulseGlow {
  0%, 100% { box-shadow: 0 0 20px rgba(99, 102, 241, 0.3); }
  50% { box-shadow: 0 0 40px rgba(99, 102, 241, 0.6); }
}

/* Float (subtle hover) */
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}
.floating { animation: float 3s ease-in-out infinite; }

/* Typewriter Effect */
@keyframes typewriter {
  from { width: 0; }
  to { width: 100%; }
}
@keyframes blink {
  50% { border-color: transparent; }
}
.typewriter {
  overflow: hidden; white-space: nowrap;
  border-right: 3px solid #6366f1;
  width: 0;
  animation: typewriter 2s steps(30) 0.5s forwards, blink 0.7s step-end infinite;
}

/* Staggered children */
.stagger-container > *:nth-child(1) { animation-delay: 0ms; }
.stagger-container > *:nth-child(2) { animation-delay: 100ms; }
.stagger-container > *:nth-child(3) { animation-delay: 200ms; }
.stagger-container > *:nth-child(4) { animation-delay: 300ms; }
.stagger-container > *:nth-child(5) { animation-delay: 400ms; }
```

### Workflow 2: Loading Spinners & States

```html
<!-- Spinner Ring -->
<style>
.spinner {
  width: 40px; height: 40px;
  border: 3px solid rgba(99, 102, 241, 0.2);
  border-top-color: #6366f1;
  border-radius: 50%;
  animation: spin 0.8s linear infinite;
}
@keyframes spin { to { transform: rotate(360deg); } }
</style>

<!-- Skeleton Loading -->
<style>
.skeleton {
  background: linear-gradient(90deg, #1e293b 25%, #334155 50%, #1e293b 75%);
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
  border-radius: 8px;
}
@keyframes shimmer { to { background-position: -200% 0; } }
</style>

<!-- Dot Pulse -->
<style>
.dot-pulse { display: flex; gap: 6px; }
.dot-pulse span {
  width: 8px; height: 8px; border-radius: 50%;
  background: #6366f1;
  animation: dotBounce 1.4s ease-in-out infinite;
}
.dot-pulse span:nth-child(2) { animation-delay: 0.16s; }
.dot-pulse span:nth-child(3) { animation-delay: 0.32s; }
@keyframes dotBounce {
  0%, 80%, 100% { transform: scale(0.6); opacity: 0.4; }
  40% { transform: scale(1); opacity: 1; }
}
</style>
<div class="dot-pulse"><span></span><span></span><span></span></div>

<!-- Progress Bar -->
<style>
.progress-bar {
  height: 4px; background: rgba(99,102,241,0.2); border-radius: 2px; overflow: hidden;
}
.progress-fill {
  height: 100%; border-radius: 2px;
  background: linear-gradient(90deg, #6366f1, #ec4899);
  animation: progress 2s ease-in-out forwards;
}
@keyframes progress { from { width: 0; } to { width: 100%; } }
</style>
```

### Workflow 3: GSAP Animations

```html
<script src="https://cdn.jsdelivr.net/npm/gsap@3/dist/gsap.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/gsap@3/dist/ScrollTrigger.min.js"></script>
<script>
gsap.registerPlugin(ScrollTrigger);

// Basic animation
gsap.from('.hero-title', {
  y: 60, opacity: 0, duration: 1, ease: 'power3.out'
});

// Staggered entrance
gsap.from('.card', {
  y: 40, opacity: 0, duration: 0.6, stagger: 0.15, ease: 'power2.out'
});

// Scroll-triggered animation
gsap.from('.section-content', {
  scrollTrigger: {
    trigger: '.section-content',
    start: 'top 80%',
    end: 'top 20%',
    toggleActions: 'play none none reverse',
  },
  y: 60, opacity: 0, duration: 0.8, ease: 'power2.out'
});

// Timeline (sequential animations)
const tl = gsap.timeline({ delay: 0.3 });
tl.from('.logo', { scale: 0, duration: 0.5, ease: 'back.out(1.7)' })
  .from('.nav-item', { y: -20, opacity: 0, stagger: 0.1 })
  .from('.hero-text', { x: -40, opacity: 0, duration: 0.6 })
  .from('.cta-button', { scale: 0.8, opacity: 0, duration: 0.4, ease: 'back.out(2)' });

// Counter animation
gsap.to('.stat-number', {
  innerText: 1000,
  duration: 2,
  snap: { innerText: 1 },
  scrollTrigger: { trigger: '.stat-number', start: 'top 80%' }
});

// Parallax effect
gsap.to('.parallax-bg', {
  yPercent: -30,
  scrollTrigger: {
    trigger: '.parallax-section',
    start: 'top bottom',
    end: 'bottom top',
    scrub: true,
  }
});
</script>
```

### Workflow 4: Lottie Animations

```html
<!-- Load Lottie player -->
<script src="https://unpkg.com/@lottiefiles/lottie-player@latest/dist/lottie-player.js"></script>

<!-- Use Lottie animation -->
<lottie-player 
  src="https://assets.lottiefiles.com/packages/lf20_animation.json"
  background="transparent"
  speed="1"
  style="width: 300px; height: 300px;"
  loop
  autoplay>
</lottie-player>
```

**Create Lottie-compatible JSON with bodymovin format:**
```javascript
// Lottie JSON structure (simplified)
{
  "v": "5.7.1",           // bodymovin version
  "fr": 30,               // frame rate
  "ip": 0,                // start frame
  "op": 60,               // end frame
  "w": 400,               // width
  "h": 400,               // height
  "assets": [],           // images, pre-comps
  "layers": [             // animation layers
    {
      "ty": 4,            // shape layer
      "nm": "circle",     // name
      "ks": {             // transform
        "o": { "a": 0, "k": 100 },  // opacity
        "p": { "a": 1, "k": [       // position (animated)
          { "t": 0, "s": [200, 200] },
          { "t": 30, "s": [200, 100] }
        ]}
      },
      "shapes": [/* shape data */]
    }
  ]
}
```

**Where to find free Lottie animations:**
- [LottieFiles](https://lottiefiles.com) — largest library
- [IconScout](https://iconscout.com/lottie-animations) — curated collection
- [Motion.dev](https://motion.dev) — developer-focused

### Workflow 5: Hover & Micro-Interactions

```css
/* Button hover with ripple */
.btn {
  position: relative; overflow: hidden;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}
.btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(99, 102, 241, 0.3);
}
.btn:active { transform: translateY(0); }

/* Card hover lift */
.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
}

/* Link underline animation */
.animated-link {
  position: relative; text-decoration: none;
}
.animated-link::after {
  content: ''; position: absolute; bottom: -2px; left: 0;
  width: 0; height: 2px;
  background: linear-gradient(90deg, #6366f1, #ec4899);
  transition: width 0.3s ease;
}
.animated-link:hover::after { width: 100%; }

/* Icon rotation */
.icon-rotate { transition: transform 0.3s ease; }
.icon-rotate:hover { transform: rotate(90deg); }

/* Smooth expand */
.expandable {
  max-height: 0; overflow: hidden;
  transition: max-height 0.4s ease, opacity 0.3s ease;
  opacity: 0;
}
.expandable.open { max-height: 500px; opacity: 1; }
```

---

## Performance Tips

1. **Prefer `transform` and `opacity`** — they don't trigger layout recalculation
2. **Use `will-change`** sparingly for heavy animations: `will-change: transform;`
3. **Avoid animating `width`, `height`, `top`, `left`** — causes layout thrashing
4. **Use `requestAnimationFrame`** for JavaScript animations
5. **Prefer CSS over JS** for simple animations (better performance)
6. **Use `prefers-reduced-motion`** for accessibility:
   ```css
   @media (prefers-reduced-motion: reduce) {
     *, *::before, *::after {
       animation-duration: 0.01ms !important;
       transition-duration: 0.01ms !important;
     }
   }
   ```
