# cvlt

**Vault: the member side's trust core.**

`cvlt` holds the member's private state (identity, device lineage, credentials,
proofs and storage), protected on every device and consistent across all of
the member's devices. It hands out **operations, never roots**: root and device
keys never leave the vault; narrowly scoped purpose keys may go to the engines
that need them. It runs isolated in its own cross-origin iframe, with proof
computation in a worker of that origin, and contains no network code.

Status: name reserved, no implementation yet.

## Structure

`cvlt` is the facade and decides (door, access rules, lineage rules, membership
credential). Its drawers are separate LGPL libraries that execute:

| Drawer | Library |
|---|---|
| Proofs | `cwlt` |
| Keys | `ckmg` |
| Signed replicated records | `cdht` |
| Encrypted web store | `cwst` |

## Boundaries

What it never does:

- Secrets never leave the device through `cvlt`; no network code.
- No own cryptography.
- No backup or recovery path (no-recovery principle): devices are added only from a live device.

## License

Copyright 2026 Julian Y. Richard Corbet. Licensed under the
[Functional Source License, Version 1.1, ALv2 Future License](LICENSE.md).
