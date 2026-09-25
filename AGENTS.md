# Agent instructions

Write all code comments and documentation in English.

## Product boundary

- Vault: encrypted secret storage on the member's device.
- Stores and retrieves encrypted secrets on the member's device.
- Client only: secrets never leave the device through `cvlt`.
- No own cryptography.
- No backup or recovery path (no-recovery principle).
- This crate is LGPL-3.0-only WITH LGPL-3.0-linking-exception. Do not add implementation code available only under the full GPL or AGPL.

## Quality boundary

- `cargo fmt --check`, `cargo clippy --all-targets` (no warnings),
  `cargo test` — all green before every commit. No local workstation
  builds; use GHA, Crow as fallback.
