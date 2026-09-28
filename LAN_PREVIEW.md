# Local-network mobile preview

The prototype supports an explicitly enabled HTTP preview on a private network address, allowing a phone and computer on the same network to use the locally running application. The server retains exact host and origin validation and binds only to the configured private address. Public deployments still require HTTPS.

Configuration checks cover opt-in, private address ranges, binding and port matching. The running application was checked through its local-network address. Windows Firewall configuration and phone-side connectivity remain environment-specific; camera scanning requires HTTPS. This preview mode keeps the existing database connection and does not migrate business records.
