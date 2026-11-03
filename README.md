# Retail Platform Showcase

This repository presents selected work from projects developed through Trippy Hippie Wholesale LLC and independent development. It covers retail software, web applications, and the tools and systems behind an ongoing Java game project.

The work began with practical problems: running a retail and wholesale business, communicating with customers, managing transactions, and building software that could be adapted to those needs. The projects continue to develop as requirements change and issues are identified through use and testing.









## TrippyPOS

TrippyPOS is a proprietary point-of-sale system developed for Trippy Hippie Wholesale LLC’s physical retail and wholesale operations. The project began with a flashed Linux kernel and was developed into a consolidated system that has been in daily use at the store since 2025.

The system combines front-end and back-end work around the daily process of making a sale. Its interfaces include a touchscreen cashier view and a separate customer-facing display. It is built with Electron, Node.js, and SQLite, and at the time of writing has over 250 API routes, 62 database tables, and 83 automated test suites. The project has involved work on:

Product records, pricing, inventory, and checkout workflows.
Cashier and customer display layouts.
Promotions, loyalty rewards, transaction history, receipts, and payment states.
Card payments through a paired phone app or a countertop card reader.
Setup for the receipt printer, cash drawer, barcode scanner, and displays.
Connections between the cashier interface and customer display.
Updates delivered to the register from a private repository.
Testing and troubleshooting pairing, responsiveness, and performance.

TrippyPOS continues to be refined around the needs of the business and the equipment used in the store.

## Videos

**These were recorded on a test copy of TrippyPOS using sample products, customers, keys, and devices. Payment account details and links have been hidden.**

**Making a sale:** A rewards member is looked up, both screens follow the sale as items are added, a $10 reward is applied, and sales are paid with Cash App and with cash.

**Setting up a card reader:** A countertop reader is paired, checked, and used for a card sale. The register sends the exact amount to the reader and completes the sale once the charge is confirmed.

**Setting up card payments and Cash App:** The phone payment app and Cash App are set up in Settings, and a card sale is sent to the staff phone.

**Setting up the printer, drawer, and scanner:** The register finds its connected equipment, prints a test receipt, opens the cash drawer, and adds items with the barcode scanner.

**Updates:** The register checks the store’s private repository for updates and installs them when it is idle.

## How It Works

**A few of the decisions behind the system:**

**A card sale is only completed after the charge has been confirmed with the payment processor:** The card is read on the phone or the reader, so card numbers never reach the register.

**Finishing a sale is safe to repeat:** If the same payment result arrives twice, stock and loyalty points are not taken twice.

**The register keeps selling without internet:** Changes are queued and sent to the online store once the connection returns.

**Payment processors connect separately from checkout, so another processor or reader can be added without changing how a sale works.**

**Updates are checked every 15 minutes, then downloaded, checked, and built on the register:** They install only when no sale is in progress, and the previous version is kept so it can be rolled back.

**Backend:** How the server finishes a sale, issues rewards, stores staff PINs, and upgrades the database without touching existing sales.

**Screens and sync:** How the customer display stays in step with the register, how change due is shown, and how sales reach the online store after a dropped connection.









## Business-to-Business Platform

The business-to-business platform was developed to support communication and purchasing between retail and wholesale customers. It brought together customer-facing web interfaces and supporting business services, and has served as the company’s online store at trippyhippie.org since 2022.

The site includes customer accounts, catalog search and filters, separate retail and wholesale pricing with quantity-discount tiers, and a cart that tracks each product variant. It shares one inventory and customer list with TrippyPOS.

The project has included work with React, Next.js, TypeScript, Tailwind CSS, Supabase, and web deployment through Vercel. Public use of the platform is no longer a priority as the business has adjusted its focus in response to market conditions.









## Avarren

Avarren is an independent Java game project in development. Its foundation has grown from ideas and individual systems developed over several years into a real-time game and supporting development suite.

The project uses Java 21 and OpenGL-based rendering, with a modular structure that separates the game client, server, shared systems, launcher, world editor, and other development tools. Work spans:

Engine rendering and performance.
Game interfaces, character selection, inventory, and gameplay systems.
World editing, terrain, object placement, and asset workflows.
Character models, animation, rigging, and testing.
Tools used to build and organize game content.

Avarren remains an ongoing project. No beta or release date has been announced.









## About This Repository

This repository is intended to share selected examples and visual demonstrations of the work above. Primary project repositories remain private for business and security purposes.

Company website: [www.trippyhippie.org](https://www.trippyhippie.org/)  
Contact: [info@trippyhippie.org](mailto:info@trippyhippie.org)




## Copyright

Copyright © 2026 Trippy Hippie Wholesale LLC. All rights reserved for company-owned materials.

Unless otherwise stated, original company materials in this repository are not licensed for reuse or redistribution. Third-party materials remain subject to their respective licenses.
