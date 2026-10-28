# biran01's October Contributions

A summary of security contributions by biran01 in October 2026:

* Reported a sensitive-data-exposure vulnerability in `tari-universe`, submitted through GitHub Security Advisories and tracked in `GHSA-gc23-qrx4-44w6`.
* The report showed that the Send Logs support flow zipped the whole app config directory into the uploaded archive, including `config_core.json` (airdrop access and refresh tokens) and `config_wallet.json` (wallet view private key). It included a root-cause analysis and a suggested fix.
* Testing was performed locally only; no shared network was touched.
* Coordinated the finding through private disclosure; the fix was applied by the Tari team in `tari-project/universe#3354` and shipped in v1.6.18. Technical details remain in the advisory until it is published. The contribution is tracked in `tari-project/special_contributions#335`.
