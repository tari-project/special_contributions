## sands786's October Contributions

A summary of security contributions by sands786 in October 2026:

- Reported a forged cross-shard foreign proposal pledge vulnerability in `tari-ootle` through GitHub Security Advisories (`GHSA-m298-6jj3-fg7c`).

- The report demonstrated that foreign proposal pledge values were not bound to quorum certificates, enabling unbacked cross-shard asset minting.

- Provided a passing proof-of-concept test, root cause analysis, and fix suggestion to the Tari team.

- These contributions are tracked by `tari-project/special_contributions#83`.

- Reported a wallet daemon denial-of-service vulnerability in `tari-ootle` through GitHub Security Advisories (`GHSA-g234-qrqg-35ch`).

- The report demonstrated that a single 2 KB manifest with deeply nested parentheses causes the manifest parser to overflow its stack, aborting the entire walletd daemon process.

- Provided a passing proof-of-concept test, root cause analysis, and fix suggestion to the Tari team.

- These contributions are tracked by `tari-project/special_contributions#92`.

## [Bug Hunt] Unmetered template return value decoding bypasses compute budget (GHSA-wjvw-6j6r-x7q6)

- **Severity:** Moderate (published)
- **Package:** tari_engine <= 0.43.0
- **CWE:** CWE-400
- **Summary:** Template return values decoded via `IndexedValue::from_raw` outside the compute meter, allowing up to 128 KiB per return value to bypass the compute budget entirely.
- **Fix:** tari-project/tari-ootle#2858
- **Retro bounty issue:** tari-project/special_contributions#122

- Reported a template module name bypass of the std. topic reservation in `tari-ootle` through GitHub Security Advisories ( GHSA-gvgw-pg6g-fr2x ).
- These contributions are tracked by tari-project/special_contributions#139.

- Reported an oversized foreign proposals vulnerability in `tari-ootle` through GitHub Security Advisories ( GHSA-27ch-g89f-mgx4 ).
- The report showed that oversized foreign proposals silently stall the shard for the epoch.
- These contributions are tracked by tari-project/special_contributions#149.

 ## [Bug_Hunt] Unauthenticated ForeignProposal validation cost denial of service pins consensus worker (GHSA-g592-vph9-hm4g)

- **Severity:** Low (published)
- **Package:** tari_consensus <= 0.43.0
- **Summary:** Unauthenticated `ForeignProposal` messages reach committee resolution and signature verification before rejection, allowing an attacker to pin the consensus worker with validation-cost denial of service.
- **Fix:** tari-project/tari-ootle#2920
- **Retro bounty issue:** tari-project/special_contributions#178

- Reported an unauthenticated ForeignProposal validation cost denial of service vulnerability in `tari-ootle` through GitHub Security Advisories ( GHSA-g592-vph9-hm4g ).
- The report showed that unauthenticated ForeignProposal validation cost pins the consensus worker.
- These contributions are tracked by tari-project/special_contributions#178.
 ## [Bug_Hunt] Unauthenticated WebAuthn auth_start endpoint leaks username existence via allowCredentials (GHSA-9p3v-6v6f-8m76)

- **Summary:** The unauthenticated WebAuthn `auth_start` endpoint returns an allowCredentials list that reflects whether the supplied username exists, allowing username registration to be tested without any credential.
- **Fix:** tari-project/tari-ootle#3064
- **Retro bounty issue:** tari-project/special_contributions#307

- Reported an unauthenticated WebAuthn auth_start username existence leak in `tari-ootle` through GitHub Security Advisories ( GHSA-9p3v-6v6f-8m76 ).
- The report showed that the allowCredentials list returned by auth_start reveals whether a username is registered.
- These contributions are tracked by tari-project/special_contributions#307.



