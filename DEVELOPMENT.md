# Development journal

## Version 0.6 — flexible stock receiving

Made opening quantity optional. Purchases now work without supplier records and offer supplier and product suggestions. New product names can be received with quantity, unit cost, and selling price in a single transaction. After stock is saved, unfamiliar supplier names prompt an optional contact-details form. Existing catalog prices and transaction history are preserved.

## Version 0.5.1 — smoother product entry

Fixed a malformed navigation icon and removed the misleading loading cursor from unavailable products. Product search now updates results without rebuilding the checkout input or cart. New products receive suggested company-prefixed SKUs and internal barcodes, with an opening-stock field saved in the same transaction. Numeric zeros clear on focus and return if left empty.

Regression checks cover SVG console errors, stable search, generated codes, stock availability, and duplicate-safe opening quantities.

## Version 0.5 — password accounts

Replaced the planned Google OAuth approach with Owner-managed email/password accounts. A private Users sheet stores roles and salted password hashes. Added first-login password changes, login-attempt limits, expiring sessions, sign-out, and password resets that revoke access. Existing staff records migrate without rewriting sales history.

Automated checks exercise the Apps Script adapter and full browser login flow with fictional data. The deployed login page was verified in a signed-out browser. Authenticated Google-hosted acceptance testing remains necessary.

## Version 0.4 — focused checkout and receipts

Added Owner-created sales rep and account manager roles in the interface. Sales reps start at checkout, with protected catalog prices and restricted navigation. Search regains focus after accepted scans or product-name, SKU, and ID entry. Receipts retain sale details and attendant names, offer 58/80 mm layouts, download as standalone HTML, and print through the browser.

27 backend tests and 9 browser tests pass locally. Personal Gmail staff sign-in remains pending OAuth client configuration and integration; this is still an owner-only Google deployment.

## Version 0.3 — a simpler retail POS

Focused the application on one company and one store. Simplified setup, navigation, inventory, checkout, receipts, reports, CSV exports, and staff forms. Removed location management, internal stock transfers, and additional-company provisioning tools. Existing transaction history is preserved.

The POS retains barcode checkout, printable Code 128 labels, purchases, stock adjustments, cash/card/bank-transfer payment recording, receipts, full returns, registers, customers, suppliers, and reports. Desktop, tablet, and phone layouts remain supported.

Backend checks cover transaction integrity, permissions, retry protection, and compatibility with older records. Browser checks cover onboarding, navigation, checkout, returns, stock adjustments, barcode rendering, and responsive layouts. Screenshots use fictional demo data only. Live Google persistence, staff sign-in, and physical hardware still require acceptance testing.

## Foundation

Google Apps Script serves a custom HTML/CSS/JavaScript interface backed by Google Sheets. Application source is maintained in a private repository; this public showcase contains curated progress and sanitized previews.
