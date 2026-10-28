# hokvo's October Contributions

A summary of security contributions by hokvo in October 2026:

* Reported a security vulnerability in `tari-universe`, submitted through GitHub Security Advisories and tracked in `GHSA-mj75-4pfh-7q38`.
* The report showed that the tapplet message handler did not check `event.origin` or `event.source`, so any window able to post to the Universe host window could invoke `TappletSigner` methods, including wallet reads and `sendOneSided` with attacker-controlled parameters; the swap iframe listener had the same gap.
* Testing was performed locally only; no shared network was touched.
* Coordinated the finding through private disclosure; the fix was implemented separately by the Tari team in `tari-project/universe#3355` and shipped in v1.6.18. The contribution is tracked in `tari-project/special_contributions#333`.
