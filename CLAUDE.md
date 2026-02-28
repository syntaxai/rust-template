# Project Instructions

## Code Style
- Write minimal, idiomatic Rust — no unnecessary verbosity
- Prefer iterator chains over manual loops
- Use `?` operator instead of manual match/unwrap on Result/Option
- Prefer `derive` macros over manual trait implementations
- No comments unless logic is non-obvious
- No doc comments on private items
- Use short but descriptive variable names

## Crates to prefer (when applicable)
- `anyhow` for application error handling (instead of custom error types)
- `thiserror` for library error types (instead of manual `impl Display + Error`)
- `serde` + `serde_json` for serialization (instead of manual parsing)
- `clap` with derive for CLI args (instead of manual parsing)
- `itertools` for complex iterator chains

## Build & Check
- `cargo clippy` — uses strict token-minimizing lints (see Cargo.toml)
- `cargo clippy --fix --allow-dirty --allow-no-vcs` — auto-fix
- Clippy runs automatically via rust-analyzer on save in Zed
