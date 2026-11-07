# sands786's November Contributions

A summary of security contributions by sands786 in November 2026:

- Reported an unsigned ProposalCertificate shard_group vulnerability in `tari-ootle` through GitHub Security Advisories ( GHSA-rgw9-phr2-f42g ).

- The report demonstrated that the shard_group value on a ProposalCertificate is unsigned, enabling a Byzantine committee member to relabel it so the forged value persists into a victim's persisted leaf block.

- The mechanism was confirmed by the Tari team, and the fix was implemented separately by sdbondi in tari-ootle#3371.

- These contributions are tracked by `tari-project/special_contributions#446`.

- Reported a missing voter-side no-state-changes-after-EOE check in `tari-ootle` by email to the Tari security team.

- The report demonstrated that crash recovery can stamp a divergent genesis root because no voter-side check rejects state changes after the end of an epoch.

- The fix was implemented separately by sdbondi in tari-ootle#2820.

- These contributions are tracked by `tari-project/special_contributions#460`.
