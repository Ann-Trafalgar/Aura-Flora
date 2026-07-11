# AURA FLORA

AURA FLORA is a warm, modern floral-commerce prototype built with PHP, HTML, CSS, and vanilla JavaScript. Its signature feature is an interactive AI event simulator that transforms an unstyled wedding or birthday venue into a customized floral event without requiring the user to upload a photo.

## Features

### Homepage and brand experience

- Premium responsive storefront design for desktop, tablet, and mobile.
- Hero section centered on buyer confidence through spatial visualization.
- Direct calls to action for the Preview Studio and product collection.
- Featured seasonal arrangements and occasion-based discovery.
- Customer rating and social-proof presentation.
- Local sourcing story featuring Dangwa Market and Benguet farms.
- Visible sustainability and waste-to-value messaging.
- Newsletter form and complete storefront footer navigation.

### AI Event Preview Studio

- Built-in venue simulation that works without uploading a photo.
- Wedding and birthday event choices.
- Animated multi-stage AI scan sequence that simulates:
  - Venue geometry mapping.
  - Ambient-light analysis.
  - Space and focal-point detection.
  - Floral-zone composition.
- Open-air garden wedding environment with sky, greenery, aisle, guest tables, and floral ceremony arch.
- Indoor birthday-party environment with colorful lighting, balloons, confetti, decorated tables, and a celebration backdrop.
- Animated transformation from an unstyled venue to a completed floral event.
- Live AI design notes and event-status caption.
- Reset and replay controls.
- Optional room-photo upload for a personalized preview.
- Uploaded images remain on the user's device and are processed in the browser.
- Canvas-based floral image overlay for uploaded room photos.
- Click-to-position an arrangement within an uploaded image.
- Downloadable image output for uploaded-photo previews.
- Shareable simulated-event preview link.

### Live event customization

- Four selectable arrangement styles:
  - Garden blush.
  - Sculptural sunset.
  - Benguet greenery.
  - Golden keepsake.
- Arrangement selection changes the flowers, colors, foliage, table pieces, and floral arch in the simulated venue.
- Three live vase styles:
  - Classic ceramic.
  - Clear glass.
  - Stone pedestal.
- Four color moods:
  - Natural blush.
  - Warm sunset.
  - Cool whites.
  - Monochrome.
- Floral-abundance slider for changing the scale and fullness of venue decorations.
- Animated transitions and feedback messages whenever a customization is applied.

### Product catalog and shopping

- Product collection with bouquets, centerpieces, gifts, keepsakes, and subscriptions.
- Category filtering.
- Occasion filtering for weddings, birthdays, graduations, anniversaries, corporate events, and sympathy arrangements.
- Price-tier filtering for budget, standard, and premium products.
- Responsive product cards with images, names, palettes, categories, and Philippine peso pricing.
- Individual product-detail pages.
- Product descriptions, ratings, review counts, size controls, and palette swatches.
- Local sourcing information on product pages.
- Delivery and flower-care information.
- “Preview in My Space” link from each product to the Preview Studio.
- Add-to-bag interaction with live cart count.

### Cart and checkout

- Persistent shopping cart.
- Quantity-aware subtotal and total calculation.
- Remove-item controls.
- Responsive order-summary panel.
- Mock checkout dialog with recipient and delivery-address fields.
- Simulated payment options for:
  - GCash.
  - Maya.
  - Credit or debit card.
  - Cash on delivery.
- Successful checkout creates an order in the customer account.

### Flash Deals and waste reduction

- Dedicated Flash Deals page for near-expiry flowers.
- Original and discounted price comparison.
- Automatic discount-percentage display.
- Freshness indicator showing the recommended use window.
- Waste-to-value collection explaining how older flowers become:
  - Pressed floral art.
  - Resin keepsakes and jewelry.
  - Botanical aroma products.
- Visible rescued-stem and avoided-loss metrics.

### Subscription boxes

- Monthly and weekly recurring-flower plans from ₱800 to ₱1,200.
- Everyday Edit, Signature, and Weekly Table options.
- Plan-benefit comparison.
- One-click simulated subscription activation.
- Active-plan and next-delivery information in the customer account.
- Messaging for pausing, skipping, or managing recurring deliveries.

### Event and corporate booking

- Consultation-request form for weddings, corporate events, bulk orders, and private celebrations.
- Captures customer name, email address, event date, event type, venue type, guest count, estimated budget, and creative notes.
- Three-step booking journey presentation.
- Generated consultation reference number.
- Booking-status tracking beginning with “Requested.”
- Consultation requests appear inside the customer account.

### Customer account and retention

- Account overview dashboard.
- Persistent order history with order number, date, payment method, total, and fulfillment status.
- Active-subscription information.
- Consultation-request history and status.
- Automatically generated personal referral code.
- Referral messaging offering ₱100 credit for a successful referral.
- Copy-referral-code control.
- Empty states for new users with no orders or bookings.

### Vendor and admin dashboard

- Dedicated vendor-studio interface.
- Sales-this-month metric.
- Active-order and delivery counts.
- Rescued-stem and avoided-loss metrics.
- Inventory-expiry alert count.
- AI demand-forecasting panel with confidence score.
- Recommended weekly order volumes for roses, sunflowers, and white mums.
- Seasonal-demand indicators for weddings, graduations, and corporate events.
- Live flower-batch inventory table.
- Batch source, intake date, best-by date, and freshness display.
- Automatic remaining-freshness calculation.
- Fresh, near-expiry, and critical visual statuses.
- Automatic Flash Deals messaging for batches with three or fewer days remaining.
- Add-batch dialog for recording flower variety, supplier, intake date, and expiry date.

### Data persistence and prototype behavior

- Cart, orders, bookings, subscription, referral code, and inventory batches persist through browser `localStorage`.
- No database or environment variables are required for the prototype.
- All AI analysis, payments, order management, demand forecasts, referral rewards, and booking statuses are clearly simulated front-end experiences.
- External floral photography is loaded from Unsplash.

## Pages

- Home
- Shop / Catalog
- Product Detail
- AI Event Preview Studio
- Flash Deals
- Subscription Plans
- Event and Corporate Booking
- Cart and Checkout
- Customer Account
- Vendor / Admin Dashboard

The PHP application uses a query-string router, for example `?page=preview`, `?page=shop`, and `?page=admin`.

## Technology

- PHP 8+
- HTML5
- CSS3 animations, transforms, responsive layouts, and simulated 3D perspective
- Vanilla JavaScript
- HTML Canvas for uploaded-photo compositing
- Browser `localStorage` for prototype persistence
- Google Fonts
- Unsplash images
- XAMPP / Apache for local development
- Vercel community PHP runtime for cloud deployment

## Project structure

```text
Aura-Flora/
├── api/
│   └── index.php       # Vercel serverless PHP entry point
├── assets/
│   ├── app.js          # Interactions, simulation, cart, account, and admin logic
│   └── style.css       # Responsive design and event environments
├── index.php           # Main XAMPP application and page router
├── vercel.json         # Vercel PHP runtime and request routes
├── .vercelignore       # Files excluded from Vercel uploads
└── README.md
```

## Run with XAMPP

1. Place the project inside the XAMPP `htdocs` folder.
2. Start Apache from the XAMPP Control Panel.
3. Open the project in a browser, for example:

```text
http://localhost/Fabianes/wasdd/
```

## Deploy to Vercel

1. Import `Ann-Trafalgar/Aura-Flora` from GitHub into Vercel.
2. Set the Framework Preset to **Other**.
3. Leave the Build Command empty.
4. Leave the Output Directory empty.
5. Keep the Root Directory set to the repository root.
6. Deploy.

The included `vercel.json` configures `vercel-php@0.9.0` and sends application requests to `api/index.php`. Static files under `/assets` are served directly.
