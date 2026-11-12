# VELORA® storefront

## Technical implementation plan

The workspace was empty. I used a no-build, dependency-free HTML/CSS/JavaScript app so the full demo runs locally without replacing any existing infrastructure. The storefront is a hash-routed single-page application; product data and presentation are separated in `app.js` and `styles.css`. Browser local storage persists the cart, applied promo, and demonstration orders.

## Run it

Open `index.html` in a modern browser, or serve this directory with any static HTTP server (for example, `npx serve .`). Product photography and the four font families load from Google Fonts and Unsplash, so those assets require an internet connection. The rest of the app runs locally.

## Payment and data

This is a frontend demonstration. Checkout does not collect card credentials, call a payment provider, charge money, or verify server-side orders. Orders, payment outcomes, and tracking milestones are stored in the current browser only. Demo payment codes: `WELCOME10`, `VELORA15`, `FREESHIP`. The checkout includes an explicit failure simulation. Cash on delivery is represented as a selection in the demo, not a dispatched real order.

## Included routes

- `#/` Home
- `#/shop` Catalog, search, category/price/availability/color filters and sorting
- `#/product/:slug` Product details, gallery, options, quantity, add-to-bag and buy now
- `#/cart` Cart editing and promotional codes
- `#/checkout` Address validation, delivery methods and simulated payment choices
- `#/order-success/:reference` Demo receipt and status
- `#/tracking` Browser-local order lookup and simulated timeline
- `#/about`, `#/account`

The catalog contains 16 demonstration products across five categories. Images are remote Unsplash assets. No real account, fulfillment, inventory backend, tax calculation, payment gateway, or webhooks are configured.
