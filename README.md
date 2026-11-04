# Retail Platform Showcase

This repository presents selected work from projects developed through Trippy Hippie Wholesale LLC and independent development: a point-of-sale system in daily use at the store, the company’s online store, and the tools and systems behind an ongoing Java game project.

The work began with practical problems: running a retail and wholesale business, serving customers, managing transactions, and building software that fits those needs. Each project continues to develop as requirements change and issues are found through daily use and testing.



## TrippyPOS

TrippyPOS is a proprietary point-of-sale system built for Trippy Hippie Wholesale LLC’s retail and wholesale store. It began with a Linux image flashed onto the register’s hardware and grew into a complete system that has run the store’s register every day since 2025.

The register pairs a touchscreen cashier view with a separate customer-facing display, and it keeps selling without an internet connection. It is built with **Electron, Node.js, and SQLite**, and currently includes more than 250 API routes, 62 database tables, and 83 automated test suites.

Work on the system includes:

- Product records, pricing, inventory, and checkout.
- Cashier and customer display layouts.
- Promotions, loyalty rewards, receipts, refunds, and transaction history.
- Card payments through a staff phone with Tap to Pay or a countertop card reader.
- Cash App payments shown to the customer as a QR code.
- Setup for the receipt printer, cash drawer, barcode scanner, and displays.
- Automatic updates delivered from a private repository.
- Testing and troubleshooting on the store’s own equipment.

TrippyPOS continues to be refined around the needs of the business and the equipment used in the store.

### Videos

Recorded on a test copy of TrippyPOS with sample products, customers, keys, and devices. Payment account details and links are hidden.

**Making a sale:** A rewards member is looked up, both screens follow the sale as items are added, a $10 reward is applied, and sales are paid by Cash App and by cash.

**Setting up a card reader:** A countertop card reader is paired, checked, and used for a sale. The register sends the exact amount to the reader and completes the sale once the charge is confirmed.

**Setting up card payments and Cash App:** Card payments can be taken on a staff phone with Tap to Pay. The register sends the exact sale amount to the phone, and the sale is completed only after the payment processor confirms the charge. Cash App payments are shown to the customer as a QR code, and staff confirm them once the payment appears in the store’s Cash App Business account.

**Setting up the printer, drawer, and scanner:** The register detects its connected equipment, prints a test receipt, opens the cash drawer, and adds an item with each barcode scan.

**Updates:** The register checks the store’s private repository for new versions and installs them only when it is idle.

### How It Works

A few of the decisions behind the system:

- **Payments are confirmed before a sale closes.** A card sale is completed only after the payment processor confirms the charge. The card is read on the phone or the reader, so card numbers never reach the register.
- **Finishing a sale is safe to repeat.** If the same payment result arrives twice, stock and loyalty points are only taken once.
- **Selling continues offline.** Changes are queued and sent to the online store when the connection returns.
- **Processors connect separately.** Payment processors connect apart from checkout, so a store can add or switch processors and readers without changing how a sale works.
- **Updates never interrupt a sale.** The register checks for updates every 15 minutes, then downloads, checks, and builds them. They install only when no sale is in progress, and the previous version is kept so it can be rolled back.

### Under the Hood

**Backend:** How the server finishes a sale, issues rewards, stores staff PINs, and upgrades the database without touching existing sales.

**Screens and sync:** How the customer display stays in step with the register, how change due is shown, and how sales reach the online store after a dropped connection.



## Business-to-Business Platform

The business-to-business platform supports communication and purchasing between the store and its retail and wholesale customers. It has served as the company’s online store at trippyhippie.org since 2022.

The site includes customer accounts, catalog search and filters, separate retail and wholesale pricing with quantity-discount tiers, and a cart that tracks each product variant. It shares one inventory and customer list with TrippyPOS.

It is built with **React, Next.js, TypeScript, Tailwind CSS, and Supabase**, and deployed through **Vercel**. Public use of the platform is no longer a priority as the business has adjusted its focus in response to market conditions.



## Avarren

Avarren is an independent Java game project in development. Its foundation has grown from ideas and individual systems developed over several years into a real-time game and supporting development suite.

The project uses **Java 21** and **OpenGL-based rendering**, with a modular structure that separates the game client, server, shared systems, launcher, world editor, and other development tools. Work spans:

- Engine rendering and performance.
- Game interfaces, character selection, inventory, and gameplay systems.
- World editing, terrain, object placement, and asset workflows.
- Character models, animation, rigging, and testing.
- Tools used to build and organize game content.

Avarren remains an ongoing project. No beta or release date has been announced.



## About This Repository

This repository shares selected examples and visual demonstrations of the work above. Primary project repositories remain private for business and security purposes.

Company website: [www.trippyhippie.org](https://www.trippyhippie.org/)  
Contact: [info@trippyhippie.org](mailto:info@trippyhippie.org)



## Copyright

Copyright © 2026 Trippy Hippie Wholesale LLC. All rights reserved for company-owned materials.

Unless otherwise stated, original company materials in this repository are not licensed for reuse or redistribution. Third-party materials remain subject to their respective licenses.
