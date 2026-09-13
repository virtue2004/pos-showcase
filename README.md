# Retail POS

A custom retail workspace built with Google Apps Script and Google Sheets, designed around clear navigation, fast checkout, and straightforward stock management for one company and one store.

**Status: version 0.3 — owner-only validation release.** Core workflows are implemented and tested locally. Live Google authorization, staff sign-in, device compatibility, and workload acceptance checks remain before production rollout.

## A view of the workspace

The screenshots below use fictional products, customers, and transactions from the local demo. They contain no live business data.

![Business overview with sales metrics, product performance, and recent transactions](media/overview.png)

![Responsive checkout with product search, category navigation, and an order panel](media/checkout.png)

## What is implemented

- Product catalog with categories, SKUs, barcodes, and reorder levels.
- One stock balance per product, supplier receiving, and adjustments.
- Checkout with discounts, tax, recorded cash/card/transfer or split payments, and printable receipts.
- USB/Bluetooth keyboard-scanner input and Code 128 product label generation.
- Full returns, register opening/closing, and cash reconciliation.
- Customers, suppliers, date-filtered reports, and CSV exports.
- Server-side owner/manager/cashier role checks and an audit history.
- Responsive desktop, tablet, and phone layouts, including a mobile order shortcut.

Camera scanning is optional and browser-dependent. Card and bank-transfer transactions are recorded after external confirmation; this release does not charge a payment gateway. Staff records do not automatically enable access to the owner-only Google deployment.

## Validation so far

- 26 business-rule and simulated Google-adapter tests passed.
- 7 browser tests passed, including barcode checkout, returns, stock adjustments, label rendering, onboarding, response-loss retries, and responsive layout checks.
- Desktop and mobile screenshots reviewed using fictional demo data.

These checks do not replace live Google, scanner, printer, permission, or load testing.

## Next milestones

- Complete live business setup and confirm persistent Google Sheets transactions.
- Validate staff identity and role permissions in the intended Google Workspace environment.
- Test actual barcode readers and receipt/label printers.
- Measure realistic checkout traffic and validate backup/recovery procedures.
- Expand capabilities based on pilot feedback, including payment integrations and additional retail workflows.

Offline checkout, native installation, partial returns, loyalty, supplier payables, and expiry/serial tracking are not part of this release.

## About this repository

This repository presents curated development progress and sanitized UI previews. Application source is maintained privately. Credentials, operational identifiers, private implementation files, and real customer records are excluded.

Built by [virtue2004](https://github.com/virtue2004).
