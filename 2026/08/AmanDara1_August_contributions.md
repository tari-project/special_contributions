# AmanDara1's August Contributions

A summary of security contributions by AmanDara1 in August 2026:

* Reported an unauthenticated remote denial-of-service vulnerability affecting `minotari_node`, tracked through `GHSA-4r27-mpgm-hx3h`.
* Identified that the wallet-query HTTP endpoint `/sync_utxos_by_block` accepted an effectively unbounded `page` value and performed arithmetic that could overflow in release builds.
* Demonstrated that the resulting panic reached the node's global panic hook, causing the entire `minotari_node` process to terminate and taking P2P networking, synchronization, gRPC, and mining interfaces offline.
* Verified the affected version range, provided a reproducible local proof of concept and negative control, and documented the complete attack path and remediation recommendations.
* Coordinated the finding through private disclosure and provided technical guidance covering arithmetic hardening, request validation, panic handling, and HTTP service exposure.
* The arithmetic issue was subsequently addressed in `tari-project/tari#7961`, with the remaining hardening work tracked in `tari-project/special_contributions#17`.
