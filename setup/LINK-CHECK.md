# Link check – Taco Labs Express site (Oct 13, 2026)

Every link on every page was extracted from the rendered theme (home, menu, deals, about, visit, FAQ, allergens, all 70 item pages, all category pages, 404) in two setups: fully set up, and right after install with no collections or menus. 0 broken internal links in both.

## Internal pages (create these 6 pages in Shopify – step 4 of the setup guide)
/pages/menu · /pages/deals · /pages/about · /pages/contact · /pages/faq · /pages/allergens
Item pages (/products/…) come from the product CSV. Category pages (/collections/…) appear only if you create collections; otherwise item pages link back to the menu.

## External links
| Where | Goes to | Checked |
|---|---|---|
| Every "Order Pickup" button | https://toast.app/r/tacolabsboca1956/order/r-8c9862f4-f083-42c3-b63a-71433cac8f3c?diningOption=takeout | Loads "Taco Labs - Boca", 1956 NE 5th Ave Suite 3, pickup + delivery |
| "Uber Eats" buttons | https://www.ubereats.com/store/taco-labs/XatwzPcqXH-ub-f5dtfMAQ | Loads Taco Labs, 1956 NE 5th Ave #3 |
| "DoorDash" buttons | https://www.doordash.com/store/taco-labs-boca-raton-25880873/ | Loads Taco Labs, Boca Raton |
| Catering nav link + "Order Catering" | https://catering.tacolabsfl.com/pages/catering-menu | Loads the catering menu |
| "Visit Kitchen & Bar" | https://www.tacolabsfl.com | Your site (blocks automated checks; listed in Google results) |
| Instagram | https://www.instagram.com/tacolabs_fl/ | From your message and Google results |
| TikTok | https://www.tiktok.com/@tacolabsfl | From your message |
| Facebook | https://www.facebook.com/p/Taco-Labs-Boca-61552158317501/ | From your message |
| "Get Directions" (Boca) | Google Maps search for 1956 NE 5th Ave, Suite 3, Boca Raton, FL 33431 | Standard Google Maps link |
| "Get Directions" (Parkland) | Google Maps search for 7619 N State Road 7, Parkland, FL | Standard Google Maps link |
| "Read us on Google" | Google Maps search for Taco Labs, 1956 NE 5th Ave | Standard Google Maps link |
| Phone (Boca) | tel:+15619610585 → (561) 961-0585 | Taps to call on phones |
| Phone (Parkland) | tel:+17548121221 → (754) 812-1221 | Taps to call on phones |

Instagram, TikTok, Facebook and tacolabsfl.com block automated checkers, so click those four once after launch.

## Issues found on your Toast ordering page (fix in Toast, not Shopify)
- Still lists old items (e.g. Loaded Birria Fries) and some wings show no price.
- The Directions link on the Toast page ends with a stray "}" and doesn't work.
- The header hours and the hours table disagree (10 PM vs Sunday 9 PM).
