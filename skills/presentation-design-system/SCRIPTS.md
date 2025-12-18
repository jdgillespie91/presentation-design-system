# Presentation JavaScript

Copy this JavaScript into the `<script>` tag at the end of `<body>`.

```javascript
const slides = document.querySelectorAll('.slide');
const totalSlides = slides.length;

function getCurrentSlide() {
  const hash = window.location.hash;
  if (!hash) return 1;
  const num = parseInt(hash.replace('#slide', ''));
  return isNaN(num) ? 1 : num;
}

function goToSlide(n) {
  if (n >= 1 && n <= totalSlides) {
    window.location.hash = `#slide${n}`;
  }
}

document.addEventListener('keydown', (e) => {
  const current = getCurrentSlide();
  if (e.key === 'ArrowRight' || e.key === ' ') {
    e.preventDefault();
    goToSlide(current + 1);
  } else if (e.key === 'ArrowLeft') {
    e.preventDefault();
    goToSlide(current - 1);
  }
});
```

## Navigation Controls

- **Right Arrow** or **Spacebar**: Next slide
- **Left Arrow**: Previous slide

## How It Works

1. Slides are shown/hidden using CSS `:target` selector based on URL hash
2. First slide is visible by default when no hash is present
3. The script updates `window.location.hash` to navigate between slides
4. Hash format is `#slideN` where N is the slide number (1-indexed)
