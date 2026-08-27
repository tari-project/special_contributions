# endscene665's August Contributions

A summary of security contributions by endscene665 in August 2026:

* Reported that two public `BaseNodeWalletRpcService` P2P RPC methods accepted unbounded repeated protobuf fields, tracked through `GHSA-vj49-p32c-v9gc`.
* Identified that `transaction_batch_query` processed every supplied signature with a kernel lookup and a mempool query on miss, and that `fetch_matching_utxos` allocated and queried the database for every supplied output hash.
* Showed that the 6 MiB RPC frame still allowed tens of thousands of elements per request, and that session limits (100 global / 10 per peer) bound session count rather than request cardinality.
* Noted that neighbouring methods already rejected oversized collections (`utxo_query`, `query_deleted`), so the missing bounds looked unintentional.
* Recommended server-side cardinality checks before allocation or database access, optional deduplication where response semantics allow it, regression tests, and an audit of other public RPC repeated fields.
* Coordinated the finding through private disclosure. The core bound landed in `tari-project/tari#7938` as shared `MAX_ALLOWED_QUERY_SIZE` (512). Remaining hardening is tracked in `tari-project/special_contributions#19`.
