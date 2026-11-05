# Retail Platform Showcase

Built and maintained by Austin Alberts, owner of Trippy Hippie Wholesale LLC.

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

https://github.com/user-attachments/assets/da5fd52e-1cb8-4794-83ed-8f1d343bb887



**Setting up a card reader:** A countertop card reader is paired, checked, and used for a sale. The register sends the exact amount to the reader and completes the sale once the charge is confirmed.

https://github.com/user-attachments/assets/9ee8a820-8b85-4f73-b7ff-81b439e49de8





**Setting up card payments and Cash App:** Card payments can be taken on a staff phone with Tap to Pay. The register sends the exact sale amount to the phone, and the sale is completed only after the payment processor confirms the charge. Cash App payments are shown to the customer as a QR code, and staff confirm them once the payment appears in the store’s Cash App Business account.

https://github.com/user-attachments/assets/9e6cddfc-ff3f-43ed-a6e2-c50508956894





**Setting up the printer, drawer, and scanner:** The register detects its connected equipment, prints a test receipt, opens the cash drawer, and adds an item with each barcode scan.

https://github.com/user-attachments/assets/80e602f3-0150-4a06-9582-7a770604bbfb





**Updates:** The register checks the store’s private repository for new versions and installs them only when it is idle.

https://github.com/user-attachments/assets/861a1725-476e-44f6-aaf8-f0b0f23ae8aa





### How It Works

A few of the decisions behind the system:

- **Payments are confirmed before a sale closes.** A card sale is completed only after the payment processor confirms the charge. The card is read on the phone or the reader, so card numbers never reach the register.
- **Finishing a sale is safe to repeat.** If the same payment result arrives twice, stock and loyalty points are only taken once.
- **Selling continues offline.** Changes are queued and sent to the online store when the connection returns.
- **Processors connect separately.** Payment processors connect apart from checkout, so a store can add or switch processors and readers without changing how a sale works.
- **Updates never interrupt a sale.** The register checks for updates every 15 minutes, then downloads, checks, and builds them. They install only when no sale is in progress, and the previous version is kept so it can be rolled back.

### Under the Hood

**Backend:** How the server finishes a sale, issues rewards, stores staff PINs, and upgrades the database without touching existing sales.

https://github.com/user-attachments/assets/6110aea1-4561-4ea0-b1b6-aecb4b9f38e0




**Screens and sync:** How the customer display stays in step with the register, how change due is shown, and how sales reach the online store after a dropped connection.

https://github.com/user-attachments/assets/d6d396aa-520f-461d-b0ba-52497da0a218






## Retail and Wholesale Online Store

The online store supports communication and purchasing between the store and its retail and wholesale customers. It has served as the company’s online store at trippyhippie.org since 2022.

The site includes customer accounts, catalog search and filters, separate retail and wholesale pricing with quantity-discount tiers, and a cart that tracks each product variant. It shares one inventory and customer list with TrippyPOS.

It is built with **React, Next.js, TypeScript, Tailwind CSS, and Supabase**, and deployed through **Vercel**.

### Videos

Recorded on a test copy of the site with sample products, accounts, and orders.

**Wholesale onboarding:** A business applies for wholesale access with its contact details and preferences. A representative reviews and approves it, and wholesale pricing turns on for that account.

https://github.com/user-attachments/assets/b7c1214a-4eee-4421-9f7d-37d3582f4324




**Shopping:** A customer browses the catalog, chooses product options, sees quantity discounts in the cart, and signs in to see wholesale prices.

https://github.com/user-attachments/assets/7074ac5e-6567-4a4a-b61a-23cb9af8e44e





**Admin back office:** A product is added with its prices, stock, and bulk discounts, an order is marked as shipped, and the new product appears in the shop.


https://github.com/user-attachments/assets/c53804df-494c-429d-900e-c264de33d541





**Mobile view:** The same store on a phone, from browsing and checkout to wholesale pricing and order history.

https://github.com/user-attachments/assets/dc31bb4f-a471-4caf-ac4e-255c73c92f96








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
