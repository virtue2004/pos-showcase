# Development journal

## Version 0.2 — retail workflows and multiple branches

Implemented a custom responsive interface with an organization overview, checkout, products, inventory, purchases, customers, suppliers, registers, reports, branches, team roles, and settings.

Added exact barcode and SKU lookup for keyboard-style scanners, internally generated product codes, and printable Code 128 labels. Camera scanning is an optional enhancement on compatible browsers.

Connected the workflows to server-side validation and a transaction journal. Automated checks cover branch-specific stock, duplicate request protection, refunds, cash reconciliation, access rules, and independent organization setup. Browser tests found a small-screen overflow issue that was corrected; a fixed mobile order shortcut now keeps the cart easy to reach.

The local suite currently passes 25 domain/adapter tests and 6 browser tests. The application source was accepted by Apps Script and an owner-only web deployment was created. The screenshots in this repository use fictional demo data. Live Google authorization, persistence, and physical devices still need acceptance testing, and the release remains owner-only during that validation.

## Foundation

Selected Google Apps Script for the server and custom HTML/CSS/JavaScript UI, replacing the initial AppSheet direction to provide more interface design control. Google Sheets is the data platform.

Established separate private source and public showcase repositories. Public updates distinguish verified progress from planned functionality and never mirror private source history.
