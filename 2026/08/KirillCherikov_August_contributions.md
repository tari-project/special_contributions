# KirillCherikov's August Contributions

A summary of security contributions by KirillCherikov in August 2026:

* Reported a private-key extraction vulnerability in the Minotari Ledger wallet, tracked through `GHSA-g9mx-9jmr-65vq`.
* Identified that the device-side `GetScriptOffset` anti-extraction guard counted unique Ledger-derived keys globally but did not require the sender-offset and script sides to be disjoint by key identity.
* Demonstrated that a malicious host could place the same key identity on both sides of the final subtraction, satisfy the existing two-key guard, and cancel the shared key so that a hardware-bound private spend scalar is revealed.
* Traced the reachable request path through `ledger_get_script_offset` and the key-manager wrapper, confirming that neither layer rejected cross-side identity overlap and that the device lacked a semantic-role branch allow-list.
* Provided root-cause and algebraic analysis, a concrete reproducer, impact assessment, affected-code verification, and remediation guidance covering device-side identity disjointness, host-side early validation, branch-role allow-lists, and regression tests.
* Coordinated the finding through private disclosure; the remaining device-side disjointness and branch-role hardening work is tracked in `tari-project/special_contributions#18`.