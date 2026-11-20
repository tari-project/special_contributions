# m4r1m0's November Contributions

A summary of security contributions by m4r1m0 in November 2026:

* Placed 1st in the Ootle Security Bug Hunt contest, reporting vulnerabilities in `tari-ootle` through private GitHub Security Advisories.
* The contribution is tracked in `tari-project/special_contributions#671`.

## Report 1 — GHSA-pgc3-w5cw-fm5v

Quadratic component-state validation on `SetState` is unmetered (O(n²) host work priced as a linear CBOR walk).

The report showed that quadratic component-state validation on `SetState` is unmetered (O(n²) host work priced as a linear CBOR walk). The fix was applied by the Tari team in `tari-ootle#3093`.

Tracked by `tari-project/special_contributions#358`.

## Report 2 — GHSA-gf2x-v6mp-cc46

`CallFunction` executes `&self` methods as static functions: component access rules are bypassed and the method acts with the template's resource authority.

The report showed that `CallFunction` executes `&self` methods as static functions: component access rules are bypassed and the method acts with the template's resource authority. The fix was applied by the Tari team in `tari-ootle#3273`.

Tracked by `tari-project/special_contributions#426`.

## Report 3 — GHSA-533f-pgxr-73c4

Validator state sync: a partially completed first sync is reported up to date after a committee layout change.

The report showed that validator state sync: a partially completed first sync is reported up to date after a committee layout change. The fix was applied by the Tari team in `tari-ootle#3312`.

Tracked by `tari-project/special_contributions#449`.

## Report 4 — GHSA-c8c5-x8q9-g5cx

`get_shard_snapshot` pins a 4 MiB unary response per RPC session, letting one peer hold gigabytes on a validator.

The report showed that `get_shard_snapshot` pins a 4 MiB unary response per RPC session, letting one peer hold gigabytes on a validator. The fix was applied by the Tari team in `tari-ootle#3370`.

Tracked by `tari-project/special_contributions#452`.

## Report 5 — GHSA-wm9x-3q2m-rphj

Declared-input load work is free when the fee intent fails: #3060's InputLoad/InputFanout charges are metered before the fee intent but never collected on the reject path.

The report showed that declared-input load work is free when the fee intent fails: #3060's InputLoad/InputFanout charges are metered before the fee intent but never collected on the reject path. The fix was applied by the Tari team in `tari-ootle#3381`.

Tracked by `tari-project/special_contributions#475`.

## Report 6 — GHSA-f2pj-25vc-7jjm

Gossipsub content-addressed message ids let an unauthorized peer suppress the honest `ForeignProposalNotification`: cross-shard foreign proposals are never fetched.

The report showed that gossipsub content-addressed message ids let an unauthorized peer suppress the honest `ForeignProposalNotification`: cross-shard foreign proposals are never fetched. The fix was applied by the Tari team in `tari-ootle#3506`.

Tracked by `tari-project/special_contributions#505`.

## Report 7 — GHSA-9f9q-g46r-7rrc

A validator that does not vote on a finalizing block reports the previous life cycle's decision.

The report showed that a validator that does not vote on a finalizing block reports the previous life cycle's decision. The fix was applied by the Tari team in `tari-ootle#3519`.

Tracked by `tari-project/special_contributions#521`.

Technical details remain in each advisory until published.
