<!-- SPDX-License-Identifier: CC-BY-SA-4.0 -->

# Contributing to DOSovoi

Open an issue describing the problem or send a focused pull request against
`main`. Include the behavior before and after the change and the checks you ran.
Do not include personal terminal contents, credentials, or private configuration.

Use stable Rust 1.80 or newer. From the repository root, run:

```sh
cargo fmt --all --check
cargo clippy --workspace --all-targets --locked -- -D warnings
cargo test --workspace --locked
```

Keep the core library deterministic and preserve the command-line contract:
commands finish immediately, operation is opt-in and local, and risk signals
come only from explicit user input. Mascot appearance must never imply that a
command or environment has been assessed as safe. Preserve plain/ASCII output,
`NO_COLOR`, care mode and immediate disabling when changing presentation.

Add a regression for changed behavior, including error paths where relevant.
Separate cultural or human-factors claims from evidence; the prototype is not
an authoritative portrayal of Slavic belief or a validated safety intervention.

Code uses MPL-2.0 and documentation uses CC-BY-SA-4.0, as recorded in the
repository's existing licence declarations. Keep changes within the requested
scope and explain any new dependency.
