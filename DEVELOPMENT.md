# Development journal

## Confirmed inter-branch stock movements

Owners and branch managers can request inventory transfers. The source manager confirms dispatch and the destination manager confirms receipt using exact product codes and counted quantities. Goods remain visibly in transit between confirmations, with stock movements, weighted costs and staff acknowledgements retained in backups. Local tests cover authorization, retry safety, reconciliation and desktop/mobile workflows.

Single-workspace branch views now hide unrelated cards. Notifications prioritize business events, while routine edits remain in the activity log. Previous-day registers require an explicit close-or-continue decision, and Nigerian local/international phone formats resolve consistently. Owners choose a branch when receiving new deliveries; managers remain scoped to their assigned branch. Production network, workload and hardware acceptance remain outstanding.

## Branch workspaces and reviewed debt reminders

The SQLite runtime now supports separate branch catalogs, stock, customers, suppliers, debts, jobs and registers within one company deployment. Owners can use a combined view or filter by branch, create branches, assign managers, review branch activity and contact managers. Managers can manage sales reps only within their assigned branch. Receipts identify the branch, while receipt numbers and staff IDs remain unique across the company.

Connected browsers receive authenticated live-update signals. Debt alerts use an Owner-configurable age threshold, and management can review individual WhatsApp or email drafts, including a queue of selected debtors. The software records prepared reminders; external messaging applications perform delivery. No customer messages were sent during verification.

Local checks cover cross-branch access rejection, stock/debt reconciliation, staff restrictions, backup/restore, live updates, and desktop/mobile workflows using fictional records. Existing single-store records stay in Main branch. Remote locations require an online central server; production network, hardware and workload acceptance remain necessary.

## Notification filters and workspace preferences

Notifications can be narrowed to low stock, out-of-stock products, bargained sales, large reductions, and bargains with unpaid balances. Product entry suggests similar existing names and rejects duplicate names regardless of capitalisation or extra spaces, while allowing distinct variations. Validation also runs on the server.

The sidebar control stays in a fixed screen position, with animated open/close icons. A light/dark switch remembers the device preference. Local checks cover product validation, imports, desktop/mobile navigation, filtering, and responsive layout using fictional records.

## Product-specific restocking shortcuts

Low-stock notifications now open the selected product in Stock alerts, expand previous supplier contacts and briefly highlight the product. Each product offers a Receive stock shortcut with the item preselected; suppliers remain optional. Mobile stock alerts display as readable product cards. Inventory adjustments remain reserved for count corrections.

## Compact navigation

The desktop sidebar can collapse to an icon strip while keeping stock and notification badges visible. The preference is remembered on the device. Brand and business-name shortcuts return to the permitted home screen, and the mobile navigation drawer remains available.

## Stock welcome and goods-only returns

Management sign-in now opens a dismissible stock summary with a translucent glass-style design, low/zero stock counts, previous supplier contact links and shortcuts to restocking pages. It appears once per sign-in and stays out of the cashier workflow. Owners and account managers can access the stock-alert page.

Blank reorder levels default to two across product creation, new items received with purchases and CSV imports; explicitly saved thresholds remain unchanged. Return screens show services as non-returnable, and server rules reject service or custom-charge refunds while preserving historical records and goods-return reconciliation.

## Service jobs and custom charges

The SQLite prototype now supports intake records for repair and other custom work, unique job barcodes, customer and company intake slips, deposits, progress tracking and linked final invoices. Variable charges can be checked out alone or alongside goods and fixed-price services.

Owners control staff access. Deposits are tracked separately from sales revenue and applied once at final checkout; outstanding balances use the existing debtor workflow. Refunds, register reconciliation, staff attribution and full backups preserve the history. Business profiles adapt intake labels for repairs, tailoring, laundry, printing and general services.

Automated domain, persistence and browser checks cover the core workflow, including barcode decoding and PDF generation. Physical device and production workload acceptance remain necessary. These profiles do not claim full industry-specific scheduling or production-management functionality.

## Bargain visibility

Checkout now gives a non-blocking warning when a bargain exceeds the configured reduction threshold. Every completed bargain below the normal total appears in management notifications, with operator, customer and payment context; larger reductions are highlighted. Receipt barcodes remain available without customer-facing scanning instructions. Domain and browser checks cover notification visibility, warning behavior and credit balances.

## Clearer checkout and receipt tracking

Product entry now distinguishes selling price from purchase cost and visibly confirms opening quantities. Checkout focuses payment entry and explains the customer details required for credit. Receipts show the amount received before change and include a scannable invoice barcode. Sales history retains original invoice totals and provides a separate linked returns view.

Fictional PostgreSQL browser checks cover opening stock, later deliveries, payment guidance, barcode decoding and sale lookup, and return reconciliation. Receipt PDFs were reviewed at both supported paper widths. Gross-profit explanations distinguish sales excluding tax from actual tax; operating-expense net profit is not yet calculated.

## Partial customer returns

Owners and account managers can return selected quantities from a historical sale, record a reason, and distinguish resellable goods from damaged goods. Separate return records preserve the original invoice and prevent quantities from being returned twice. Credit balances, cash refunds, stock valuation, receipts, sales analysis and monthly statements reconcile each return.

Fictional-data checks cover repeated returns, credit adjustments, tax/discount rounding, permissions, mobile workflows and receipt PDF rendering. The database upgrade preserves historical full returns. Card and bank refunds remain externally executed payments recorded by the POS.

## Monthly Owner statements

The PostgreSQL prototype now includes Owner-only monthly email settings and report previews. Statements cover sales, gross profit, collections, inventory, outstanding debts, stock reminders and a twelve-month sales chart, with detailed CSV attachments. Reports preserve historical month-end balances.

Scheduling includes persistent delivery status and duplicate-retry protection. Database restores pause automatic emails for recipient review. Local accounting, access-control, concurrency and mobile UI checks passed. Live sending still requires each company's email provider configuration and a running server or hosted scheduler; inbox delivery has not yet been validated.

## Mobile scanning and encrypted company backups

Added continuous browser-camera scanning with a bundled retail barcode decoder, duplicate-scan protection, stock checks and camera cleanup. Owner accounts can export an encrypted complete company backup, preview a restore, download a recovery copy and replace the destination database atomically. Staff IDs, accounts and transaction history are preserved while live sessions are revoked. Database deletion is guarded for Owner restore transactions. Fictional-data tests cover camera decoding, cross-database restore, continued sales, permissions and rollback. Actual phone/camera and client-hosting acceptance remain necessary.

## Barcode PDFs and staff receipt privacy

Barcode batches can now download as multipage A4 PDFs with per-product quantities and cutting guides. Product entry accepts package-barcode scans and keeps SKU synchronized; catalog and inventory search support consecutive scanner inputs. Permanent company-prefixed staff IDs replace operator names and emails on customer receipts. Attendants see their own Sales history, while authorized management retains the full view and shared debt collection remains available. Automated browser and database checks cover these changes; physical scanner and printer acceptance remains necessary.

## CSV imports and clearer barcode batches

Added Owner-only CSV templates and imports for products, services, customers and suppliers. Server-side matching avoids duplicate records, updates supplied values, preserves blank fields and reports conflicts. Per-record reports distinguish creation, updates, unchanged records and errors. Opening stock is applied only to new goods; interrupted requests can resume safely. Barcode batches now offer checkbox selection and separate quantities per product. Local browser and PostgreSQL checks cover these workflows.


## Personal Supabase prototype

The first private workbook copy has been imported into a dedicated Supabase database and reconciled against the source. The localhost application connects through a restricted database login, with anonymous data access denied. The original Sheets deployment remains unchanged. Hands-on sign-in and acceptance testing of the imported prototype are next.

## PostgreSQL migration candidate

The migration target is now a separate company-owned Supabase project for each deployment. A staged PostgreSQL backend stores readable relational records, preserves historical prices and audit history, and imports data with reconciliation and rollback checks. Staff access remains enforced by the server, using a restricted database login.

Local checks cover company isolation, simultaneous checkout of the last item, duplicate-request protection, repayments, returns and staff access revocation. Browser checks cover checkout, receipts, reports, labels and cashier access. The live system remains on Google Sheets; real-company import, hosted acceptance and recovery rehearsal are still required before cutover.

## Version 0.15 - staged SQLite backend and profit diagnostics

Added a local SQLite migration candidate with one database per company, retained business rules, staff authentication, transactional imports, reconciliation checks and backup tooling. Local tests exercise accounting, session revocation, company isolation and HTTP access boundaries. A profit breakdown explains historical costs and return adjustments. The live system still uses Google Sheets: online hosting, real-company migration and production acceptance are not complete.

## Version 0.14 - catalog identifiers, analytics and bulk labels

Product codes share server-validated reservations across IDs, SKUs and barcodes, including retired codes. SKU and barcode stay synchronized. Overview adds date, staff, item-type and payment-status filters with KPI comparisons and a charted PDF. Bulk label jobs support per-product quantities and printed cutting guides. Identifier tests include a 5,000-product catalog.

## Version 0.13 - historical returns, exports and staff access

Sales history provides full returns against the original invoice with a required reason, plus a company-branded PDF of the filtered date period. New transactions preserve the operator name, permanent login ID and role. Owner controls support activation, deactivation, role changes and deletion with access revocation and preserved historical records. The password minimum is eight characters.

## Version 0.12 - repayment entry and stock reminders

Repayments start blank with a live remaining-balance preview. Red stock and unread-notification counters remain visible on small screens. Notification reads are stored per management user, while stock reminders remain until replenishment. Inventory valuation covers all available goods regardless of search. Historical invoice prices remain preserved.


## Version 0.11 - PDF receipts and register controls

Added local PDF receipt downloads with a separate Print action, removed duplicate cash wording, and highlighted outstanding invoices. Product selection now requires a register and respects stock reserved in the current cart. Register history includes expected and counted cash with role-based visibility.

## Version 0.10 - services and sales filters

Added a service catalog and mixed goods/service checkout with historical line types. Services do not affect stock. Sales filters combine dates, item types and payment status. Cash received now starts blank; balance and change use larger, distinct colours.

## Version 0.9.1 - compact checkout

Arranged customer, price, and payment controls in desktop columns. Outstanding balances automatically use customer debt, with completion disabled until a valid name and phone are present.

## Version 0.9 - credit sales and repayments

Added live split-payment totals, zero-opening-cash guidance, credit checkout with required customer details, grouped debtor invoices, and auditable repayments. Receipts display cumulative payments and balances; cash repayments reconcile to the collecting register.

## Version 0.8 - focused checkout and stock follow-up

Separated item entry from payment entry with a larger checkout dialog and a return-to-products action. Added catalog/contact deletion while preserving historical records, Owner-only transaction detail corrections, and grouped stock alerts with supplier contact dropdowns.

## Version 0.7 - customer checkout and reminders

Added customer name suggestions and atomic customer creation during sales. Attendants can record bargained final totals while preserving catalog prices. Management sees low-stock reminders and historical large-reduction alerts with a configurable threshold. Receipts and refunds retain the actual amount charged.

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
