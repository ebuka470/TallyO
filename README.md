# TallyO

Simple stock management for small businesses.

TallyO is a mobile-first inventory and sales tracking app designed to help small business owners keep track of what they have, what they buy, what they sell, and what is running low — without complicated accounting language.

✨ Features

- 📦 Add and manage products
- 🧾 Record purchases and sales
- ➕ Quickly add products to your quantity
- ➖ Quickly remove products from your quantity
- 💰 Track buying and selling prices
- ⚠️ Get reminders when products are running low
- 🔎 Search and filter products
- 🖼️ Add product images
- 📊 View simple business summaries
- 🧾 View sales and purchase history
- 🌙 Light and dark mode
- 📱 Mobile-first responsive design
- 💾 Automatic local data storage
- 📤 Export a complete backup
- 📥 Import backups and restore your data
- 🎨 Business-specific product units
- 🚀 Demo mode for trying TallyO
- 📲 Installable as a Progressive Web App (PWA)
- 📴 Works offline after it has been loaded

📁 Project Structure

tallyo/
├── index.html
├── manifest.json
├── service-worker.js
└── README.md

"index.html"

The main TallyO application.

The current version is intentionally kept as a single HTML file containing the app's interface, styling, and JavaScript functionality.

"manifest.json"

Contains the PWA information used when installing TallyO:

- App name
- Short name
- Theme colour
- Start URL
- Display mode
- App icons

"service-worker.js"

Handles offline functionality and caching.

It allows the TallyO app shell to remain available when the device temporarily has no internet connection.

🚀 Running TallyO

TallyO can be hosted as a static website.

For local development, you can use a simple local server.

For example:

python -m http.server 8000

Then open:

http://localhost:8000

«Opening "index.html" directly with "file://" is not enough for PWA features such as service workers.»

📲 Installing TallyO

TallyO is designed to work as a Progressive Web App.

When hosted over HTTPS, supported browsers can offer an Install App option.

After installation, TallyO opens in its own app-like window instead of a normal browser tab.

📴 Offline Mode

TallyO uses a service worker to cache the application shell.

Once the app has been loaded successfully, the cached version can be opened without an internet connection.

Most of TallyO's core functionality works locally because inventory data is stored in the browser.

💾 Data & Backups

TallyO stores its working data locally in the browser.

This includes things such as:

- Business information
- Products
- Quantities
- Prices
- Transactions
- Product images
- Settings
- Theme preferences

Creating a backup

Go to:

Settings → Demo & backup → Save backup

TallyO exports your data as a JSON backup file.

Restoring a backup

Go to:

Settings → Demo & backup → Import backup

Select a previously exported TallyO JSON backup.

TallyO validates the backup before replacing the current data.

🧪 Demo Mode

TallyO includes a demo mode with sample products and transactions.

Use it to explore the application without entering real business data.

To leave demo mode:

Settings → Demo & backup → Exit demo

🏪 Business Types

TallyO can adapt product counting options to different kinds of businesses, including:

- General retail
- Fashion & clothing
- Phone accessories
- Food & provisions
- Beauty & cosmetics
- Farming & produce
- Electronics
- Other

Examples of available units include:

Pieces
Packs
Pairs
Sets
Boxes
Cartons
Bags
Sacks
Baskets
Bottles
Jars
Cups
Trays
Bunches
Kg
Grams
Litres

🔐 Privacy

TallyO's core inventory data is stored locally in the user's browser.

The app does not require an online account for its basic inventory functionality.

Users should keep exported backups somewhere safe because clearing browser/site data can remove locally stored application data.

🛠️ Technology

TallyO currently uses:

- HTML
- CSS
- JavaScript
- LocalStorage
- Service Workers
- Web App Manifest
- Progressive Web App (PWA) APIs

No framework is required for the current version.

📌 Important

For production deployment:

1. Serve TallyO over HTTPS.
2. Keep "index.html", "manifest.json", and "service-worker.js" together.
3. Make sure the service worker is served from the correct scope.
4. Test installation on Android and desktop browsers.
5. Test backup and restore before using TallyO with important business data.

📄 License

Add your preferred license here before publicly distributing the project.

---

TallyO — Know what you have. Know what you sold. Keep your business moving.
