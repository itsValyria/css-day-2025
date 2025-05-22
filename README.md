# CSS Day 2025 - My Demo

For this demo, I experimented with scroll-driven animations using the brand-new `animation-timeline: view()` feature. This lets you trigger CSS animations based on the position of an element in the viewport -- no JavaScript needed!

### ✨ What happens in my demo?
As the `.container` element scrolls into view, a few animations kick in:

A trigger animation sets a custom property `--animate: true`, which activates the animation container query.

The `.text` element scales in with a smooth motion and starts a gradient animation on the text using `background-image` and `background-clip`.

When the container scrolls out again, a reverse pop-back animation plays, scaling the text down and fading it out using a `--primary-color` that blends in with the background.

All animations respect user preferences with `prefers-reduced-motion`. ✨

### 🔍 CSS features used:
`@supports (animation-timeline: view())` to conditionally apply scroll-based animations

`@container style(--animate: true)` to trigger further animations when a custom property is set

`animation-timeline: view()` and `animation-range` for scroll-based timing

Custom easing with `linear()` and `cubic-bezier()` to give the animations more personality

Fluid typography and color transitions using gradients and `background-clip: text`

### 🧠 Why I chose this
I'm fascinated by how much is now possible in CSS without touching JavaScript. And I hate JavaScript. Scroll-driven animations make interactions feel alive and responsive to the user's journey through the page. I wanted to explore this with minimal markup and maximum style -- because I've never really built something fun with it during the past two years.
