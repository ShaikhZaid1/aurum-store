# AURUM — Luxury E-Commerce Store

A beautifully crafted, single-file luxury e-commerce web application built with plain HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies — just open and run.

---

## Features

- **Animated Hero Section** — Full-screen landing with staggered text reveals and a scroll indicator
- **Scrolling Marquee** — Promotional banner with smooth infinite scroll
- **Product Catalog** — 12 curated products across 5 categories
- **Category Filtering** — Instantly filter by Outerwear, Knitwear, Accessories, Footwear, and Fragrance
- **Live Search** — Real-time product search from the navigation bar
- **Product Quick-Add** — Hover cards reveal an Add to Cart button without opening a modal
- **Product Modal** — Full detail view with description, size selector, and add-to-cart action
- **Sliding Cart Panel** — Drawer-style cart with quantity controls, item removal, and live subtotal
- **Toast Notifications** — Lightweight feedback messages for cart and wishlist actions
- **Responsive Design** — Adapts gracefully to mobile and tablet viewports
- **Keyboard Accessible** — `Escape` key closes modals and the cart panel

---

## Getting Started

No installation required. Simply open the file in any modern browser.

```bash
# Clone or download the project
open aurum-store.html
```

Or double-click `aurum-store.html` in your file explorer.

---

## Project Structure

```
aurum-store.html     # Complete application — styles, markup, and logic in one file
README.md            # Project documentation
```

The entire application lives in a single HTML file, organized into three sections:

| Section | Description |
|---|---|
| `<style>` | All CSS, custom properties (variables), animations, and responsive rules |
| `<body>` | Semantic HTML markup — nav, hero, shop, features, footer, overlays |
| `<script>` | Product data, cart logic, filtering, search, modal, and toast system |

---

## Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Semantic structure |
| CSS3 | Custom properties, Grid, Flexbox, animations |
| Vanilla JavaScript | Cart, filters, search, modals, DOM manipulation |
| Google Fonts | Cormorant Garamond (display) + DM Sans (body) |

No npm. No bundler. No framework.

---

## Product Categories

| Category | Count |
|---|---|
| Outerwear | 2 |
| Knitwear | 3 |
| Accessories | 3 |
| Footwear | 2 |
| Fragrance | 2 |

---

## Design System

**Color Palette**

| Token | Value | Usage |
|---|---|---|
| `--bg` | `#0c0b09` | Page background |
| `--bg2` | `#141210` | Surface background |
| `--bg3` | `#1c1a16` | Elevated surface |
| `--gold` | `#c9a84c` | Primary accent |
| `--gold2` | `#e8c96a` | Accent hover state |
| `--cream` | `#f0e8d8` | Primary text |
| `--cream2` | `#b8aa96` | Secondary text |
| `--muted` | `#7a7060` | Muted / placeholder text |

**Typography**

- **Display / Headings** — Cormorant Garamond, weights 300 & 600
- **Body / UI** — DM Sans, weights 300, 400 & 500

---

## Customization

### Adding a Product

Add a new object to the `products` array in the `<script>` section:

```javascript
{
  id: 13,
  name: 'Linen Shirt',
  cat: 'knitwear',        // must match a filter category
  emoji: '👕',
  price: 3800,
  sale: 5200,             // optional — shows strikethrough price
  badge: 'new',           // 'new', 'sale', or '' for none
  desc: 'A relaxed linen shirt...'
}
```

### Adding a Category

1. Add a filter button in the `#filters` div:
```html
<button class="filter-btn" data-cat="your-category">Your Category</button>
```
2. Use the same value for `cat` in the products array.

### Changing the Currency

Search for `₹` in the script and replace with your preferred currency symbol. Update `toLocaleString('en-IN')` to match your locale (e.g., `'en-US'` for USD).

---

## Browser Support

Works in all modern browsers that support CSS Custom Properties, CSS Grid, and ES6+.

| Browser | Support |
|---|---|
| Chrome 80+ | ✓ |
| Firefox 75+ | ✓ |
| Safari 13.1+ | ✓ |
| Edge 80+ | ✓ |

---

## Possible Extensions

- Checkout page with form validation
- Wishlist with localStorage persistence
- Product image gallery (replace emoji with real images)
- Size guide modal
- Related products section
- Discount / coupon code system
- Backend integration (Stripe, Razorpay, Shopify API)

---

## License

MIT — free to use, modify, and distribute for personal and commercial projects.

---

*Crafted with care. No dependencies harmed in the making of this project.*
