## `> whoami`

```
rust and typescript build tooling. i fix bugs upstream and build with ai.
also: web, ecommerce, security, local llm inference.
```

## `> open source`

merged bug fixes in pnpm, wasm-bindgen, rust-lang/cc-rs, oxc and svelte.

- pnpm: `update --no-save` now respects overrides ([#15261](https://github.com/pnpm/pnpm/pull/15261))
- pnpm: package removal waits out windows file locks instead of failing ([#15409](https://github.com/pnpm/pnpm/pull/15409))
- pnpm: a `devEngines.runtime` range with `||` no longer installs the `node` npm package ([#15443](https://github.com/pnpm/pnpm/pull/15443))
- pnpm: `deploy --legacy` no longer marks the source workspace as outdated ([#15458](https://github.com/pnpm/pnpm/pull/15458))
- pnpm: switching to a pinned pnpm version keeps release age approvals without a workspace file ([#15461](https://github.com/pnpm/pnpm/pull/15461))
- pnpm: `publish` now honors a scoped registry set in `publishConfig` ([#15574](https://github.com/pnpm/pnpm/pull/15574))
- pnpm: `patch-commit` patches with a no-newline marker mid-hunk apply again ([#15554](https://github.com/pnpm/pnpm/pull/15554))
- pnpm: `cargo doc` works on windows again, which unblocks the pre-push hook there ([#15605](https://github.com/pnpm/pnpm/pull/15605))
- wasm-bindgen: the headless test runner keeps the path of a remote webdriver url ([#5345](https://github.com/wasm-bindgen/wasm-bindgen/pull/5345))
- wasm-bindgen: the schema mismatch error names the wasm file and the cli binary ([#5346](https://github.com/wasm-bindgen/wasm-bindgen/pull/5346))
- wasm-bindgen: field getters no longer trip `unsafe_op_in_unsafe_fn` inside macros ([#5347](https://github.com/wasm-bindgen/wasm-bindgen/pull/5347))
- wasm-bindgen: `inspectable` tuple structs get a valid `toJSON` again ([#5349](https://github.com/wasm-bindgen/wasm-bindgen/pull/5349))
- cc-rs: `-Ctarget-feature` from `RUSTFLAGS` now reaches gcc and clang on x86 ([#1948](https://github.com/rust-lang/cc-rs/pull/1948))
- cc-rs: a `/link` flag no longer breaks msvc builds, it gets dropped with a warning ([#1949](https://github.com/rust-lang/cc-rs/pull/1949))
- cc-rs: `expand()` with msvc no longer prints the file name as a warning ([#1950](https://github.com/rust-lang/cc-rs/pull/1950))
- oxc: oxfmt no longer drops a comment before `=` and prints the one after it twice ([#26997](https://github.com/oxc-project/oxc/pull/26997))
- svelte: `let:` next to a `children` snippet is now a compile error instead of a runtime crash ([#18873](https://github.com/sveltejs/svelte/pull/18873))

## `> projects`

**[Bloxsmith](https://bloxsmith.net)**: ai ui generation for roblox studio. describe an interface, refine it in chat, and sync the editable result into your game.

## `> inference`

deployed, operated and tuned large open-weight moe models for local inference on 4× PRO 6000 Blackwell GPUs: quantization, sglang/flashinfer serving, tensor parallelism, speculative decoding, long-context caching, benchmarking and reproducible cloud deployment.

## `> get in touch`

- email: waltuecom@gmail.com
- happy to talk about anything, just reach out
