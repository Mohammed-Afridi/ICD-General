# ICD General Contracting - Technical Specification

## Technology Stack

- **HTML5**: Semantic markup
- **CSS3**: Custom CSS with CSS variables
- **JavaScript**: Vanilla JS (ES6+)
- **No Frameworks**: Pure HTML/CSS/JS as requested

## Project Structure

```
/mnt/okcomputer/output/website/
├── index.html          # Main HTML file
├── css/
│   └── styles.css      # All styles
├── js/
│   └── main.js         # All JavaScript
├── assets/
│   ├── logo_full.png   # Company logo
│   └── images/         # All service/section images
└── README.md
```

## Implementation Plan

### Phase 1: HTML Structure
- Semantic HTML5 elements (header, nav, section, footer)
- Proper heading hierarchy (h1 → h2 → h3)
- Accessible attributes (alt text, aria labels)
- Meta tags for SEO

### Phase 2: CSS Styling
- CSS custom properties for colors and spacing
- Mobile-first responsive design
- Flexbox and Grid layouts
- Smooth transitions and animations

### Phase 3: JavaScript
- Navbar scroll behavior
- Mobile menu toggle
- Scroll reveal animations (Intersection Observer)
- Smooth scroll to sections

## CSS Architecture

### Variables
```css
:root {
  --color-primary: #1a365d;
  --color-primary-dark: #0f2744;
  --color-secondary: #c53030;
  --color-secondary-dark: #9b2c2c;
  --color-accent: #d69e2e;
  --color-background: #f7fafc;
  --color-surface: #ffffff;
  --color-text-primary: #1a202c;
  --color-text-secondary: #4a5568;
  --color-text-light: #ffffff;
  --color-border: #e2e8f0;
  
  --container-max: 1200px;
  --section-padding: 80px;
  --transition-fast: 200ms;
  --transition-normal: 300ms;
  --transition-slow: 600ms;
}
```

### Breakpoints
- Mobile: < 640px
- Tablet: 640px - 1024px
- Desktop: > 1024px

## Animation Implementation Table

| Animation | Tech | Implementation |
|-----------|------|----------------|
| Navbar scroll | CSS + JS | Add `.scrolled` class on scroll > 50px |
| Hero text reveal | CSS | `@keyframes fadeInUp` with stagger delays |
| Scroll reveal | JS + CSS | Intersection Observer + `.reveal` class |
| Card hover | CSS | `transform: translateY(-8px)` + shadow |
| Button hover | CSS | `transform: scale(1.02)` + bg color change |
| Service icon hover | CSS | `transform: scale(1.1)` |

## Performance Considerations

- Lazy load images below the fold
- Use `will-change` sparingly on animated elements
- Minimize reflows with transform/opacity animations
- Support `prefers-reduced-motion`

## Browser Support

- Chrome/Edge (latest 2 versions)
- Firefox (latest 2 versions)
- Safari (latest 2 versions)
- Mobile browsers (iOS Safari, Chrome Android)
