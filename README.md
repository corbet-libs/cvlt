# cvlt

**Vault: encrypted secret storage on the device.**

`cvlt` will store the member's secrets (device keys, openings, credentials) encrypted on the device, using established storage and crypto (WebCrypto, IndexedDB, or Veilid `keyvaluedb`) instead of own crypto.

Status: name reserved, no implementation yet.

## Boundaries

What it does:

- Stores and retrieves encrypted secrets on the member's device.

What it never does:

- Client only: secrets never leave the device through `cvlt`.
- No own cryptography.
- No backup or recovery path (no-recovery principle).

## License

Copyright 2026 Julian Y. Richard Corbet. Licensed under
[LGPL-3.0-only](LICENSES/LGPL-3.0-only.txt)
[WITH LGPL-3.0-linking-exception](LICENSES/LGPL-3.0-linking-exception.txt).
See [LICENSE.md](LICENSE.md).
