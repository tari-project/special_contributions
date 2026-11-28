# Security Report Contribution: GHSA-vm2c-649x-xqj8

This document records the security contribution and vulnerability report regarding multi-shard transactions in `tari-ootle` locking a `ValidatorFeePool` substate and failing at `Command::LocalAccept` (`SubstateNotFound` / `DataInconsistency`) following in-place leader fee updates.

The underlying fix was resolved and merged in the main `tari-project/tari-ootle` repository.

Fixes #720