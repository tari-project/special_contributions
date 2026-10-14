# m4r1m0's October Contributions

A summary of security contributions by m4r1m0 in October 2026:

* Reported a confidential transfer proof vulnerability in `tari-ootle`, submitted by email to the Tari security team and tracked in `GHSA-7vhp-937q-mc4w`.
* The report showed that `confidential.create_transfer_proof` computed the change output as the locked input value minus the confidential amount only, so a proof with a non-zero `reveal_amount` carried change overstated by exactly that amount. Because the balance proof can only verify when the committed values on both sides are equal, every confidential transfer proof with a reveal amount was rejected by the engine as invalid.
* Coordinated the finding through private disclosure; the fix was implemented by the Tari team in `tari-project/tari-ootle#2824`. The contribution is tracked in `tari-project/special_contributions#153`.
