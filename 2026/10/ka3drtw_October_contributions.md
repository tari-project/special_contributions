# ka3drtw's October Contributions

A summary of security contributions by ka3drtw in October 2026:

- Reported a legacy wallet credential cleanup vulnerability in `tari-universe`, submitted through GitHub Security Advisories and tracked in `GHSA-qhqr-xhmr-w9vf`.
- The report showed that the migration into keyring-backed credential storage read the legacy `credentials_backup.bin` fallback containing reversibly encoded Tari seed passphrase and Monero seed material, but did not remove the file after successful migration, leaving an offline-recoverable copy of wallet secrets in the application data directory and potentially in backups.
- Provided source-code analysis and an exact-format local proof of concept confirming recovery of the legacy credential material and persistence of the fallback file after modeled successful migration. Testing was performed locally only; no shared network, production service, real wallet seed, passphrase, token, transaction, or user data was used.
- The fix was implemented by the Tari team in `tari-project/universe#3353`, hardened in `tari-project/universe#3361`, and shipped in Tari Universe v1.6.18. The contribution is tracked in `tari-project/special_contributions#336`.
