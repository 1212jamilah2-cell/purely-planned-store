# Kindred Pages — Digital Planner Store v2 (Prototype)

This is a **separate React + TypeScript + Vite project**, designed to deploy on Vercel. It does not modify Plateful.

## Features
- Six collections: Health & Wellness, Hydration, Nutrition & Recipes, Student, Financial, Professional.
- Printable PDF and tablet-friendly digital format selector.
- Basic / Plus / Deluxe packages, four styles, optional sticker/template/motivation add-ons.
- Responsive shopping interface and shopping bag demonstration.
- Optional virtual pet **demo** with local mini-goal celebrations (no real reminders, push notifications, account sync, or games).
- Draft disclaimer, license and privacy information.
- Actual cover previews from the earlier Health & Wellness planner files. Other collections are **coming soon**.

## Important readiness boundaries
**This is not a live commerce store.** No payments, real checkout, protected digital file delivery, customer accounts, PDF generation, real reminder notifications, or interactive games are implemented. The add-to-bag control only demonstrates an existing basic Health planner selection; all other combinations are previews. Prices are illustrative and should be reviewed. No actual customer medical, educational, or financial data is collected by this demo.

The health cover previews are representative of existing PDFs; they do not imply that every format/tier/color/add-on combination has been generated. The original Health PDFs are **not** bundled as downloadable paid assets in this source-code ZIP. Keep products in private storage once checkout is configured.

## Run locally on Windows 11
1. Install Node.js LTS from https://nodejs.org and Visual Studio Code from https://code.visualstudio.com
2. Extract this ZIP, open the `digital-planner-store-v2` folder in VS Code.
3. Open **Terminal > New Terminal**.
4. Run `npm install` and then `npm run dev`.
5. Open the localhost URL shown by Vite.
6. Before deploying, run `npm run build`.

## Deploy to Vercel
1. Create a **new** GitHub repository for this folder (do not overwrite Plateful).
2. Push the code to GitHub.
3. In Vercel, choose **Add New > Project** and import that repository.
4. Framework preset: Vite; build command: `npm run build`; output directory: `dist`.
5. Deploy. The result is a public **demo** only; leave checkout disabled.

## Required before real sales
- Produce, inspect and test every advertised PDF format, package, style and add-on. Validate hyperlinks, fillable fields, print quality, accessibility and app compatibility.
- Create individual product preview images showing the **actual pages** for each purchasable variant.
- Implement server-side checkout with Stripe or another provider, verify signed webhook events, and issue expiring per-order download links from private storage. Never rely on client-side payment confirmation or expose private PDFs in `public/`.
- Add a real order database, support email, refunds/cancellation policy, business identity, taxes/sales tax review, and accessible terms/privacy/cookie notices.
- If creating interactive pets and games, design a separate consent-based web app, allow complete opt-out, avoid guilt or streak pressure, and obtain any necessary notifications permissions.
- Legal and medical/nutrition/financial/educational disclaimers are **draft templates** only, not legal advice. Review local laws, consumer rights, privacy rules, advertising claims, and accessibility requirements with qualified professionals.

## Suggested future phases
1. **Catalog MVP:** six category landing pages, real basic PDFs, verified previews, search and bundles.
2. **Checkout:** secure payments, tax configuration, protected digital fulfillment, email receipts and refund workflows.
3. **Customizer:** generate truly personalized PDFs (theme, page selection, stickers) on a server, and validate downloads.
4. **Companion app:** optional pet, local goals, opt-in reminders, gentle games, accessibility and data export/delete.

## Project structure
- `src/main.tsx` — React storefront and interactive prototype
- `src/styles.css` — responsive styling
- `public/previews/` — previews of previously created Health & Wellness PDFs
- `index.html` — application entry

**Do not place private customer information, Stripe secret keys, or paid download files in `public/` or client code.**
