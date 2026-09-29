# Relational SQLite deployment

The POS now has a relational SQLite deployment path for independently installed companies. The current application service is shared with the PostgreSQL backend, preserving staff authorization, sales, stock, partial returns, monthly statements and encrypted backup/restore workflows.

The migration tool takes a consistent read-only source snapshot, imports into a new local database and reconciles every relational table and authorized user view. Existing passwords and staff IDs are retained; sessions are cleared for sign-in after migration. The source remains available as a pre-cutover recovery copy.

Performance work removes remote database round trips, caches prepared statements and application state, and avoids rewriting the full recovery snapshot on every transaction. Each write still commits its audit event and affected relational rows atomically. A dashboard mutation affecting backup consistency was also corrected.

Fictional-data tests cover recovery after restart, concurrent last-stock sales, authorization, partial returns, encrypted backup/restore, monthly reporting and browser workflows. The small migration dataset showed substantially faster backend state preparation locally; these timings do not establish capacity for every workload. The UI still loads a complete authorized snapshot, so larger deployments need workload testing.

The local server supports phone access on the same network and a separate localhost listener. Camera scanning still requires HTTPS. A packaged installer, unattended off-device backups and production hardware acceptance remain deployment work.
