# Taco Labs Express – "Win a Free Treat" sign-up pop-up

## How it works
1. A first-time visitor (or someone about to leave) sees the pop-up.
2. They enter an email **or** a phone number.
3. They instantly get one unique code from your Toast codes. They choose their treat: a free margarita, free tres leches or free horchata.
4. The same code is emailed / texted to them, and their contact goes into your marketing list for future emails and texts.

## Why Klaviyo (not code inside the theme)
Handing out 1,000 one-time codes needs a server. If the codes lived in the website code, anyone could open the page source and copy all 1,000.
Klaviyo (free Shopify app; free up to 250 contacts, then paid; SMS is paid) does exactly this:
- **Uploaded coupons:** you upload a CSV of codes from any system (Toast included). Each sign-up gets the next unused code, shown on screen. No code is ever given twice. 100–5,000 codes per upload.
- **Targeting:** new visitors only, exit intent, time delay, scroll depth, "don't show again" rules, desktop vs mobile.
- **Email + SMS lists** with the consent wording the law requires, and a CSV export of every contact.

## Letting guests choose their treat (recommended setup)
Make **one** kind of code in Toast that unlocks **any one** of the three items, and let the guest choose when they redeem:
- In Toast, create a discount "Free Treat": 100% off **one** item from a group of Margarita (any flavor), Tres Leches Cake and Horchata. One-time use, one per check.
- Create your 1,000 unique codes for that one discount, e.g. `TREAT-XXXXXX`.
- One coupon pool in Klaviyo, one code per sign-up. The guest picks margarita, tres leches or horchata at the counter or in online ordering.

This is the simplest option for guests and staff: one code type to train on, no wrong-prize mix-ups, and you see in Toast which treat people pick.

**Alternative: guests choose in the pop-up.** Step 1 asks for the email or phone, step 2 shows three buttons (Margarita / Tres Leches / Horchata), and each button opens its own success step with its own uploaded code pool (MARG-, TRES-, HORC-). It works, but you need three code pools sized to a demand you can't predict, and a pool can run out while the others sit unused.

## Step by step
1. **Install Klaviyo:** Shopify admin → Apps → search "Klaviyo" → install → connect the store.
2. **Turn on the app embed:** Online Store → Themes → Customize → App embeds (left sidebar) → Klaviyo → on → Save. (The Taco Labs Express theme supports app embeds; nothing to code.)
3. **Enable uploaded coupons:** Klaviyo → Settings → Other → Profile maintenance → enable Uploaded Coupons.
4. **Create the coupon:** Klaviyo → Content → Coupons → Create → Uploaded coupon. Name it `Free Treat 2026`. Upload `free-treat-codes.csv` (I'll send it). Add a **static backup code** in case codes run out (e.g. a generic $3-off code from Toast).
5. **Build the form:** Klaviyo → Sign-up forms → Create → Popup (desktop) + Flyout (mobile). Use the design and copy below.
6. **Set targeting and behavior** exactly as in the table below.
7. **Welcome messages:** Klaviyo → Flows → "Welcome series" template, triggered by the form:
   - Email 1 (immediately): "Your free treat code: {{ coupon }}. Pick a margarita, tres leches or horchata." Include how to redeem, expiry and the menu link.
   - SMS 1 (immediately, if they gave a phone number): "Taco Labs Express: your code is {{ coupon }}. Show it at the counter or use it in online ordering. Expires in 30 days. Reply STOP to opt out."
8. **Test** on desktop and phone in a private window, then publish.

## Pop-up design (match the website)
- Colors: black #141414 background, coral #f87f84 button, yellow #ffb844 headline accent, white text.
- Fonts: Anton for the headline, Work Sans for body (add both in Klaviyo → Settings → Fonts → Google Fonts).
- Image: `tlx-tacos-hero.jpg` (in the theme assets) on the left on desktop; no image on mobile.
- Step 1 headline: **WIN A FREE TREAT**
- Step 1 text: "Join the Lab list and get a free treat on your next visit: your pick of a margarita, tres leches or horchata."
- Fields: Email (or a "Use phone instead" option) → Button: **GET MY FREE TREAT**
- Step 2 (optional): "Want Taco Tuesday deals by text?" Phone field + Klaviyo's SMS consent text → Button: **TEXT ME DEALS** / link "No thanks"
- Success: "**YOUR FREE TREAT IS READY!** Code: {coupon}. Use it for a free margarita, tres leches or horchata, your choice. Show it at the counter or enter it in online ordering. One per guest, expires in 30 days. We also emailed it to you."
- Fine print: "One code per person. Margarita 21+ with valid ID. With any purchase. Expires 30 days after issue."

## Targeting and behavior (the "doesn't annoy people" logic)
| Setting | Desktop | Mobile |
|---|---|---|
| Who sees it | Not already in Klaviyo (new visitors only) | Same |
| When | Exit intent **or** after 15 seconds, whichever comes first | After 50% scroll **or** 20 seconds (phones have no exit intent) |
| Pages | All pages except /pages/allergens | Same |
| Re-show after closing | Not for **30 days** | 30 days |
| After sign-up | Never again | Never again |
| Format | Center popup | Bottom flyout (Google penalizes full-screen mobile popups) |
| Teaser after closing | Small "Free treat" tab bottom-left, so they can reopen it | Same |
| Click outside to close | On | On |

Result: each person sees it at most once a month, never after signing up, and never on their first second on the page.

## In Toast
- Create the codes as **one-time use**, valid for **30 days**, one per check.
- The margarita choice: 21+ only, with any food purchase (see note below).
- Set them up so they work both in-store and in Toast online ordering.

## Note on the free margarita
Florida regulates how alcohol licensees promote and give away drinks. Before launch, check the wording with your liquor-license attorney or the Florida Division of Alcoholic Beverages & Tobacco. A common safe version is "free margarita with any entrée purchase, 21+ with valid ID, dine-in". If in doubt, swap the margarita prize for a free churro.

## Getting the contact list
Klaviyo → Audience → Lists & segments → "Free Treat sign-ups" → Manage → Export to CSV (email, phone, consent, sign-up date, code issued).
Send email campaigns and texts from Klaviyo directly; it tracks unsubscribes and SMS consent for you.

## What I need from you
1. The 1,000 Toast codes (one discount, any of the three items).
2. One static backup code for when they run out.
I'll send back `free-treat-codes.csv`, checked for duplicates and ready to upload in step 4.
