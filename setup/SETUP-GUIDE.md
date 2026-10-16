# Taco Labs Express – Shopify setup guide (boca.tacolabsfl.com)

How the site works: Shopify is the website (menu with prices, deals, about, FAQ, location).
Food orders go to Toast Online Ordering, so they print straight to the kitchen with every tortilla and hold-topping choice.
Delivery buttons go to Uber Eats and DoorDash. Catering is a link out to catering.tacolabsfl.com.
Nobody checks out on Shopify, so there is no cart or checkout to set up.

## What's in this kit
| File | What it is |
|---|---|
| taco-labs-express-theme.zip | The custom theme. Upload as-is. |
| taco-labs-express-products.csv | All 70 menu items with prices, descriptions and tags. |
| pages/*.html | Copy for the About, Deals, Allergens and Contact pages. |
| brand/ | Logo lockups, favicon, social share image. |

## Build order (about 1 hour)

### 1. Upload the theme
Online Store → Themes → Add theme → Upload zip file → choose `taco-labs-express-theme.zip`. Don't publish yet.

### 2. Import the menu
Products → Import → choose `taco-labs-express-products.csv`. Check "Publish new products to all sales channels". 70 products.
After import, spot-check 3 items (e.g. Birria Beef Taco $4.99, 3-Taco Combo $14.99, Original Margarita $7.99).

### 3. Create 14 collections (optional, recommended)
The menu page and Fan Favorites already work without collections: the theme groups items by product type and tag. Collections add category pages (/collections/chicken-tacos) and let you reorder items by dragging.
Products → Collections → Create collection. Type = **Smart**, condition **Product type is equal to** the type below.
Keep the title exactly as written so the web address (handle) matches the theme. Sort: **Manually** (items then show in menu order; drag to adjust).

| Collection title | Condition | Handle (check under "Search engine listing") |
|---|---|---|
| Taco Combos | Product type = Taco Combos | taco-combos |
| Chicken Tacos | Product type = Chicken Tacos | chicken-tacos |
| Veggie Tacos | Product type = Veggie Tacos | veggie-tacos |
| Beef & Seafood Tacos | Product type = Beef & Seafood Tacos | beef-seafood-tacos |
| Burritos & Bowls | Product type = Burritos & Bowls | burritos-bowls |
| Quesadillas & Specials | Product type = Quesadillas & Specials | quesadillas-specials |
| Chips & Dips | Product type = Chips & Dips | chips-dips |
| Wings | Product type = Wings | wings |
| Sides | Product type = Sides | sides |
| Desserts | Product type = Desserts | desserts |
| Kids | Product type = Kids | kids |
| Drinks | Product type = Drinks | drinks |
| Margaritas | Product type = Margaritas | margaritas |
| Fan Favorites | **Any** condition: Product tag = Fan Favorite, Product tag = Bestseller | fan-favorites |

### 4. Create 6 pages
Online Store → Pages → Add page. Use these **exact titles** (Shopify turns them into the web addresses the site links to). Leave the Theme template on **Default page**: the theme shows the right sections on each page by itself.

| Title (exact) | Content to paste | Web address it gets |
|---|---|---|
| Menu | leave empty | /pages/menu |
| Deals | pages/deals.html | /pages/deals |
| About | pages/about.html | /pages/about |
| Contact | pages/contact.html | /pages/contact |
| FAQ | leave empty | /pages/faq |
| Allergens | pages/allergens.html | /pages/allergens |

To paste HTML: in the page editor click the `<>` (Show HTML) button, paste, save.
Why the template list may be missing: Shopify only lists templates from your **published** theme. You don't need them here, but they appear once this theme is published.

### 5. Navigation (optional)
The header and footer already show the right links out of the box. Create these menus only if you want to change them.
Online Store → Navigation.
- **Main menu** (handle `main-menu`): Menu → /pages/menu · Deals → /pages/deals · Catering → https://catering.tacolabsfl.com/pages/catering-menu · About → /pages/about · Visit → /pages/contact
- **Footer menu** (handle `footer`): Menu · Deals · FAQ · Allergens & Dietary · Catering (same link) · Visit & Contact

### 6. Theme settings (Customize → Theme settings)
- **Ordering links:** already filled in: Toast pickup, Uber Eats and DoorDash.
- **Catering site link:** https://catering.tacolabsfl.com/pages/catering-menu
- **Social:** already filled in: Instagram @tacolabs_fl, TikTok @tacolabsfl, Facebook.
- Address, phone and hours are pre-filled. Colors match the printed menu.

### 7. Check every page in the editor, then publish
Home, Menu, Deals, About, Visit, FAQ, one product, one collection. Then Themes → Publish.
Remove the store password: Online Store → Preferences → Password protection (needs a paid plan).

### 8. Domain (skip if boca.tacolabsfl.com already points to this store)
Settings → Domains → Connect existing domain → `boca.tacolabsfl.com`. At your DNS provider add a CNAME record: host `boca` → `shops.myshopify.com`. Set it as the primary domain.

### 9. SEO (Online Store → Preferences, and each page's "Search engine listing")
| Page | Title | Description |
|---|---|---|
| Home | Taco Labs Express – Tacos in Downtown Boca Raton | 20 globally inspired tacos from $3.99 at 1956 NE 5th Ave, Boca Raton. Birria, al pastor, Korean BBQ and more. Order pickup online. |
| Menu | Menu – Taco Labs Express Boca Raton | Full menu with prices: tacos from $3.99, 3-taco combo $14.99, burritos, bowls, Quesa Birria, wings, margaritas. |
| Deals | Taco Tuesday, Happy Hour & AYCE – Taco Labs Express | $3 & $4 tacos and $5 margaritas on Taco Tuesday and Happy Hour (dine-in), lunch combos from $9.99, All You Can Eat $24.99. |
| About | About Taco Labs Express Boca | Fast-casual, globally inspired tacos in downtown Boca Raton. |
| Visit & Contact | Hours & Location – Taco Labs Express Boca | 1956 NE 5th Ave, Suite 3, Boca Raton. Tue–Sat 11:30 AM–10 PM, Sun 11:30 AM–9 PM, closed Monday. (561) 961-0585. |
| FAQ | FAQ – Taco Labs Express | Ordering, gluten-friendly options, vegetarian tacos, deals and catering. |

### 10. After launch
- Google Business Profile: website → https://boca.tacolabsfl.com, menu link → /pages/menu, order link → your Toast link.
- Instagram / Facebook bio link → https://boca.tacolabsfl.com
- Price change? Update it in **Toast** (what guests pay) **and** in the Shopify product (what the site shows). They don't sync.

## Photos, reviews and Instagram (Customize → Home page)
- **Hero → Background food photo:** your best food shot, landscape, 2000 px+ wide. It is darkened behind the text automatically.
- **Image with text:** a food or dining-room photo next to the "Tacos from everywhere" intro.
- **Photo gallery (Inside the Lab):** 3 photos. The first one shows large.
- **Reviews (What Boca Says):** add your real Google rating and review count in the "Google" rating block, and paste 3 real Google reviews word for word with the reviewer's name as shown on Google. Empty review cards stay hidden on the live site. Set "Link to all reviews" to your Google Maps listing.
- **Instagram (From the Lab):** set your handle, then add 6 recent post photos (square). Each tile links to your Instagram. For a feed that updates on its own, install an Instagram feed app from the Shopify App Store and add its block here instead.
Empty photo slots only show in the theme editor, never to customers.
- **Already filled in:** Google 4.8 · 1,271 reviews, Uber Eats 4.5 · 1,500+ ratings, one Google review, Instagram @tacolabs_fl, TikTok @tacolabsfl.
- **Photos are built into the theme.** 14 of your photos load straight from the theme files (hero, intro, gallery, Instagram tiles, catering, About page). No separate upload. To swap one, pick a new photo in that section; it overrides the built-in one.

## Product photos (optional)
Square, at least 1200×1200, on product pages: Birria Beef Taco, Al Pastor Chicken Taco, Smash Beef Supreme, Bang Bang Shrimp, 3-Taco Combo, Burrito, Quesa Birria, Street Corn, Guac & Chips, Wings.
Homepage hero: uses your built-in tacos photo. To replace it: Customize → Hero → Side photo (landscape 4:3, at least 1400 px wide).

## Still needed from you
1. Two more Google reviews (full text + name) to replace the one that calls the jackfruit taco vegan.
2. A high-resolution logo and full-size photos (the current photos are 287–680 px).
3. The Parkland ZIP code (33067 or 33073) for the Kitchen & Bar card.
4. Rename your Google Business Profile from "Taco Labs - Kitchen & Bar (East Boca)" to "Taco Labs Express Boca".
5. Update your Toast online ordering menu to the Express menu (it still shows Loaded Birria Fries, wings without prices and a broken Directions link).
