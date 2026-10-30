# Security contribution for issue #64

Security report for GHSA-q7qg-fgqp-p96v.

The report identified that public liquidity pools allowed arbitrary LP token minting and reserve theft.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#2759. This file records the contribution for the retro bounty; no code changes are required.


# Security contribution for issue #109

Security report for the direct stealth UTXO burn authorization-bypass issue acknowledged in tari-project/special_contributions#109.

The report identified that the StealthUtxoBurn path could bypass the expected resource authorization hook.

The fix was implemented separately. This file records the contribution for the retro bounty; no code changes are required.


# Security contribution for issue #291

Bug report for GHSA-mf7r-4pfr-2qg3.

The report identified that coalesced UTXO protobuf frames are dropped and wallet scan cursor skips owned outputs.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#3047. This file records the contribution for the retro bounty; no code changes are required.
# Security contribution for issue #275

Security report for GHSA-8v88-58fr-4878.

The report identified that mutable authorization signature order transfers new-account ownership to an attacker.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#3019. This file records the contribution for the retro bounty; no code changes are required.
# Security contribution for issue #258

Security report for GHSA-cxj9-vwm7-5wjg.

The report identified that uTXO stream repeats resource-wide SQLite scans for every requested shard.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#2989. This file records the contribution for the retro bounty; no code changes are required.
# Security contribution for issue #297

Bug report for GHSA-28cx-xpx5-3xq2.

The report identified that omitted confidential output poisons wallet scan state after indexer recovery.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#3052. This file records the contribution for the retro bounty; no code changes are required.
# Security contribution for issue #296

Security report for GHSA-52vp-j7ph-m3g3.

The report identified that forged UTXO Spent update persistently hides an unspent wallet output.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#3057. This file records the contribution for the retro bounty; no code changes are required.
# Security contribution for issue #316

Security report for GHSA-x3rp-9mf5-53mm.

The report identified that manifest global reuse amplifies authorized wallet requests into stored over-limit dry runs.

The fix was implemented separately by @sdbondi in tari-project/tari-ootle#3121. This file records the contribution for the retro bounty; no code changes are required.
