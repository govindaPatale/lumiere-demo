# Lumière — Adobe Target Demo Site

A premium e-commerce demo page with two Adobe Target mboxes for A/B testing demos.

## Mbox Locations

| Mbox Name | Element | What to test |
|---|---|---|
| `demo-hero-headline` | Hero headline + subtext | Different value propositions |
| `demo-hero-cta` | CTA button text + style | Button copy and colour |

## Setup

### 1. Add your at.js file
- Go to **Adobe Target UI → Administration → Implementation**
- Click **Download at.js** (version 2.11.8)
- Save it as `at.js` in this folder

### 2. Update index.html
Replace the at.js script tag with:
```html
<script src="at.js"></script>
```

### 3. Deploy to GitHub Pages
```bash
git add .
git commit -m "Add demo site"
git push
```
Go to repo **Settings → Pages → Source: main branch → / (root)**

## A/B Test Offers to Create in Target Agent

### Control (default — already on page)
- Headline: `Skin that tells your story`
- CTA: `Explore Collection`

### Variant B — Urgency headline
```html
<div class="hero-eyebrow">Limited Time Offer</div>
<h1 class="hero-headline">Your best skin<br><em>starts today</em></h1>
<p class="hero-sub">Join 200,000+ who transformed their skin with our science-backed ritual. Free shipping on orders over £60.</p>
```

### Variant B — CTA
```html
<div class="hero-actions">
  <a href="#products" class="btn-primary" id="hero-cta-btn">
    Shop Now — Free Shipping
    <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
      <path d="M1 7h12M8 3l4 4-4 4" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </svg>
  </a>
  <a href="#" class="btn-secondary" id="hero-secondary-btn">
    See bestsellers <span class="btn-arrow">→</span>
  </a>
</div>
```

## Debug Mode
Add `?debug=true` to the URL to see mbox boundaries and Target debug panel:
```
https://your-username.github.io/lumiere-demo/?debug=true
```

## Mbox Names to use in Target Agent
When creating activities in the agent, use these exact mbox names:
- `demo-hero-headline`
- `demo-hero-cta`
