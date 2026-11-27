# November 2026 Contributions — kiyeps

A summary of contributions by @kiyeps in November 2026:

- Security report to `tari-project/universe` via GitHub Security Advisory [GHSA-gr4c-r43w-8pp9](https://github.com/tari-project/universe/security/advisories/GHSA-gr4c-r43w-8pp9): **Monero seed PIN encryption used a single unsalted SHA-256 KDF, allowing offline brute force of the PIN keyspace**. The AES key protecting the Monero seed was a bare SHA-256 of the 4–6 digit PIN, so anyone holding the encrypted blob could brute-force the entire keyspace offline in seconds, while the Tari seed already used Argon2. The fix was implemented by the Tari team in [tari-project/universe#3464](https://github.com/tari-project/universe/pull/3464), deriving the key with salted Argon2id and re-encrypting existing blobs on the next PIN entry, and shipped in [v1.6.21](https://github.com/tari-project/universe/releases/tag/v1.6.21).
