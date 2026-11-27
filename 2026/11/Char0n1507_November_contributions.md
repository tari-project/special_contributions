# Char0n1507 November 2026 Contributions

## Security Vulnerability Report — GHSA-3rc7-6cr6-8mx8

Fixes #679

Reported a security vulnerability in `tari-universe` where every app config 
file was written with 0644 permissions under a world-traversable directory. 
On a shared machine, this allowed any local user to read the MCP bearer token, 
airdrop tokens, and the wallet view key, and reach the MCP control plane.

The fix was implemented in tari-project/universe#3473, which creates config 
files as owner-only and tightens existing installs on startup. Shipped in v1.6.21.

XTM Address: <your XTM address here>
