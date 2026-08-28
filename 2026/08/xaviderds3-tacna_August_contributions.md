# xaviderds3-tacna's August Contributions

A summary of implementation contributions by xaviderds3-tacna (Xavier Flores) in August 2026:

* Implemented and merged `tari-project/tari#7974`, covering acceptance item 1 of `tari-project/special_contributions#20`.
* Added canonical excluded commitments to the wallet gRPC `TransferRequest`, allowing callers to bypass an explicitly identified unspendable output without stopping the wallet or editing its SQLite database.
* Validated commitment encoding and bounded the repeated request field before propagating the resulting `UtxoSelectionCriteria` through both one-sided and interactive transfer paths.
* Added regression coverage proving that coin selection chooses another available output when a commitment is excluded and returns insufficient funds when every available commitment is excluded.
* Kept the implementation compatible with the repository's strict Clippy and formatting requirements. The contribution was reviewed and merged by `SWvheerden` on 28 August 2026 as commit `7ce6becca07f84a6a86abd36280a586846a651cb`.
