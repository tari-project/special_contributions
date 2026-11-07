# Vallejo1921's November Contributions

A summary of contributions by Vallejo1921 in November 2026:

- Contributed an exact CBOR decoding hardening to `tari-ootle` in [tari-project/tari-ootle#3331](https://github.com/tari-project/tari-ootle/pull/3331).
- The hardening enforces strict exact-length CBOR deserialization across non-consensus entrypoints (`Substate::from_bytes`, `TemplateMetadata::from_cbor`, and `arg_to_value`), rejecting inputs with trailing unconsumed bytes.
- Eliminates parser permissiveness where malicious or malformed payloads could embed trailing unparsed bytes past valid data.
- Merged into `development` by the Tari team.
- This contribution is tracked by `tari-project/special_contributions#458`.
