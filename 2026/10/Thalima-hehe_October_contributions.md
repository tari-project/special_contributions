# Thalima-hehe's October Contributions

A summary of security contributions by Thalima-hehe in October 2026:

* Reported a validation bypass in `tari-ootle` where foreign proposals attached to leader blocks skip validation, enabling forged cross-shard state, submitted through GitHub Security Advisories and tracked in `GHSA-ffmc-66pq-4cgx`.
* The report showed that when a leader proposes a block, attached foreign proposals from other shard groups are never run through `check_foreign_proposal`, so a malicious leader can attach forged proposals with fabricated state and validators will execute cross-shard transactions against the false data without any check.
* Provided root-cause analysis and a runnable in-repo proof of concept. Testing was performed locally only; no shared network was touched.
* Coordinated the finding through private disclosure; the fix was implemented by the Tari team in `tari-ootle#2827`. The contribution is tracked in `tari-project/special_contributions#104`.

* Reported that epoch committee rotation orphans mid-flight transaction locks in `tari-ootle`, permanently bricking substates network-wide, submitted through GitHub Security Advisories and tracked in `GHSA-9f5q-6h58-r4c3`.
* The report showed that when a shard committee rotates at an epoch boundary, incoming validators have no pool record for in-flight transactions and return TransactionNotInPool no-votes, blocking the 2f+1 quorum needed to finalize. The orphaned Exclusive substate locks are only released via the pool-record-present finalize path, which can never execute — so the locks stay forever and future transactions on those substates fail network-wide. The realistic trigger is a committee-count change.
* Provided root-cause analysis and a runnable in-repo proof of concept. Testing was performed locally only; no shared network was touched.
* Coordinated the finding through private disclosure; the fix was implemented by sdbondi in `tari-ootle#2957`. The contribution is tracked in `tari-project/special_contributions#229`.
