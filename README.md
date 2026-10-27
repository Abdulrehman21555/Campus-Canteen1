# Campus Canteen — React Frontend

A responsive campus-canteen ordering frontend built with React, Vite, and React Router. The original `canteen-app.zip` project is not modified; this is a separate project folder.

## Features
- Responsive phone, tablet, and desktop layout with semantic HTML, CSS Grid/Flexbox, and media queries.
- Menu is loaded from `public/menu.json` using `useEffect`, `fetch`, and `async/await` (with loading and error states). Item information is not hard-coded into the page.
- Reusable `MenuList`, `ItemCard`, and `Cart` components.
- Live search, category filters, and favourite toggle.
- React Router screens: Menu (`/`), item details (`/item/:id`), and Cart (`/cart`).
- Shared cart state via React Context; the header count, quantities, and subtotal update immediately without reloading.
- Local food image assets in `public/images`.

## Run locally
1. Install Node.js (LTS) if it is not already installed.
2. Extract the ZIP and open this folder in VS Code.
3. Open a terminal in this folder and run:
   ```bash
   npm install
   npm run dev
   ```
4. Open the local URL printed by Vite (usually `http://localhost:5173`).
5. To verify a production build, run `npm run build`.

Keep `public/menu.json` in the public folder so `fetch('/menu.json')` can load it. Prices are shown in Pakistani rupees (Rs.). Checkout is a frontend demo; a real order needs a backend/payment integration.

## Screen recording submission
A screen recording is not included because it needs to be recorded from a running browser on your computer. To make a short 30–60 second recording:
1. Start the app using `npm run dev` and open it in the browser.
2. Search for “burger”, then switch categories (e.g. Drinks).
3. Open a food item card to show the item-details route, then use Back to menu.
4. Add two items; point out that the header cart count changes instantly.
5. Open “My order”, increase/decrease a quantity, and show the total updating.

On Windows, use `Win + Alt + R` (Xbox Game Bar) or Snipping Tool's screen-record option if available. Save the recording as `campus-canteen-demo.mp4` alongside your submission.
