# RTeamProject's August Contributions

A summary of security contributions by RTeamProject in August 2026:

* Reported a weak JWT signing secret vulnerability in the Tari airdrop backend (`rwa.y.at`), tracked through `GHSA-7c58-g2hp-x29p`.
* Identified that access tokens are HS256-signed with the hardcoded literal `"secret"`, allowing any unauthenticated attacker to forge a valid session token for any user by substituting the victim's public UUID (exposed via the public `/leaderboard` endpoint) into the token payload.
* Demonstrated account takeover (read profile + modify display name) against a disposable test account, and showed that forging `role: "admin"` unlocks `/quest/*` routes on a separate service that trusts the JWT payload.
* Confirmed the same flaw on the staging host `rwa.yat.fyi` (no Turnstile captcha verification).
* Provided root-cause analysis, a concrete reproducer, impact assessment, and remediation guidance (environment-injected signing secret, role verification from the backend user store, rate limiting + captcha on production login).
* Coordinated the finding through private disclosure; the fix was applied by the Tari team and the contribution is tracked in `tari-project/special_contributions#27`.
