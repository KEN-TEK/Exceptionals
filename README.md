# Elites: Online Store Front-End Prototype

A multi-page front-end prototype of an online clothing and accessories store, built in plain HTML, CSS and a little JavaScript as a team academic project at the Uganda Institute of Information and Communications Technology (UICT) in 2024.

> **Project status:** static prototype. There is no backend, database, user accounts, working cart or checkout. See [Known limitations](#known-limitations).

<!-- Add 2-3 screenshots here, e.g. ![Products page](screenshots/products.png) -->

## What it includes

| Page | Purpose |
|---|---|
| `index.html` | Home page with a cover image and a "Trending" product section |
| `products.html` | Large product listing (grid of product cards) with an animated heading |
| `clothes.html`, `shoes.html`, `watches.html` | Category pages |
| `accounts.html` | Payment-options page: links to Airtel Money, MTN Mobile Money, Stanbic, Centenary and Equity Bank online banking, and Binance Pay |
| `signup.html`, `signin.html` | Account pages [CONFIRM: describe what they contain] |
| `refund.html`, `privacy.html`, `terms.html` | Policy pages [CONFIRM] |

Every page shares the same header (logo, search box, navigation) and footer (links and copyright).

## Features

- **Sticky header** with a Flexbox navigation bar, hover and active states.
- **Responsive product grid** using CSS Grid (`repeat(auto-fit, minmax(200px, 1fr))`), so the number of columns adapts to the screen width.
- **Animations and transitions:** a `@keyframes` colour animation on the products heading and a smooth hover-zoom on product images.
- **Pricing display** in Ugandan shillings, with the original price struck through next to the sale price (home and category pages).
- **"Add to Cart" buttons** that show a confirmation message (`index.js`).
- **Payment options page** with links out to mobile-money, banking and crypto providers.

## Technologies

- HTML5
- CSS3 (Flexbox, Grid, keyframe animations, transitions, pseudo-classes)
- JavaScript (a single alert function)
- No frameworks or build tools

## Project structure

```
Elites_web/
├── images/                  product photos, logo, icons
├── index.html / index.css   home page
├── products.html / products.css
├── clothes.html, shoes.html, watches.html
├── accounts.html / accounts.css
├── signin.html, signup.html
├── refund.html / refund.css
├── privacy.html, terms.html
├── style.css, styles.css    additional stylesheets
└── index.js                 "Add to Cart" confirmation
```

## How to run

No installation is needed.

1. Download or clone the repository.
2. Open `index.html` in any modern browser.

Keep the `images/` folder next to the HTML files so pictures load.

## My contribution

I was **mainly responsible for the products page** (`products.html` and `products.css`): the product grid, the animated heading, the image hover effects, the button styling and the sticky navigation. I also contributed to shared layout and styling in other sections of the site. [CONFIRM and add team members' names, e.g. "Built with [NAMES]."]

## Known limitations

This project was written while learning, and I have kept the original work visible. Issues I know about:

- **No real shopping cart.** "Add to Cart" only displays a message. Nothing is stored, totalled or checked out.
- **Search box is not functional.** It is a visual element only.
- **`products.html` does not load `index.js`,** so its "Add to Cart" buttons call a function that is not defined on that page. *(Remove this line once the fix is committed.)*
- **Placeholder content on the products page:** every card is titled "item name", has no price, and some images repeat.
- **Payments page only links out** to external provider websites. It does not process payments.
- **HTML validity:** a few stray or unclosed tags (`<li>`, `</li>`), a `<header>` placed inside a `<p>`, and most images have no `alt` text.
- **CSS duplication:** the same rules (for example `.products`) are defined several times, and some old versions are commented out. Header and navigation styles are repeated across stylesheets.
- **Footer** still shows the copyright year 2022.
- **Not tested** on a wide range of browsers or devices. `-webkit-box-reflect` is non-standard and is not supported in Firefox.

## Possible improvements

- Build a working cart with JavaScript and `localStorage`.
- Store products as data (JSON) and generate the cards with JavaScript instead of copy-pasting HTML.
- Add `alt` text and fix the HTML so it passes a validator.
- Merge the duplicated CSS into one shared stylesheet.
- Add a responsive mobile menu and a working search filter.
- Add a backend for accounts, orders and payments.

## Notes

This README was drafted with AI assistance (Claude) and reviewed by the author.
