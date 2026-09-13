# Development journal

## Version 0.3 — a simpler retail POS

Focused the application on one company and one store. Simplified setup, navigation, inventory, checkout, receipts, reports, CSV exports, and staff forms. Removed location management, internal stock transfers, and additional-company provisioning tools. Existing transaction history is preserved.

The POS retains barcode checkout, printable Code 128 labels, purchases, stock adjustments, cash/card/bank-transfer payment recording, receipts, full returns, registers, customers, suppliers, and reports. Desktop, tablet, and phone layouts remain supported.

Backend checks cover transaction integrity, permissions, retry protection, and compatibility with older records. Browser checks cover onboarding, navigation, checkout, returns, stock adjustments, barcode rendering, and responsive layouts. Screenshots use fictional demo data only. Live Google persistence, staff sign-in, and physical hardware still require acceptance testing.

## Foundation

Google Apps Script serves a custom HTML/CSS/JavaScript interface backed by Google Sheets. Application source is maintained in a private repository; this public showcase contains curated progress and sanitized previews.
