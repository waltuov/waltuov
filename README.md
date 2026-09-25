## `> whoami`

```
rust and typescript build tooling. i fix bugs upstream and build with ai.
also: web, ecommerce, security, local llm inference.
```

## `> open source`

currently working on the oxc minifier, with rolldown next to it. some merged fixes:

- oxc: oxfmt no longer drops a comment before `=` and prints the one after it twice ([#26997](https://github.com/oxc-project/oxc/pull/26997))
- pnpm: package removal waits out windows file locks instead of failing ([#15409](https://github.com/pnpm/pnpm/pull/15409))
- pnpm: `patch-commit` patches with a no-newline marker mid-hunk apply again ([#15554](https://github.com/pnpm/pnpm/pull/15554))
- wasm-bindgen: field getters no longer trip `unsafe_op_in_unsafe_fn` inside macros ([#5347](https://github.com/wasm-bindgen/wasm-bindgen/pull/5347))
- wasm-bindgen: `inspectable` tuple structs get a valid `toJSON` again ([#5349](https://github.com/wasm-bindgen/wasm-bindgen/pull/5349))
- cc-rs: `-Ctarget-feature` from `RUSTFLAGS` now reaches gcc and clang on x86 ([#1948](https://github.com/rust-lang/cc-rs/pull/1948))
- cc-rs: the static c++ stdlib now links with `-bundle`, so it works with mingw ([#1955](https://github.com/rust-lang/cc-rs/pull/1955))
- svelte: `let:` next to a `children` snippet is now a compile error instead of a runtime crash ([#18873](https://github.com/sveltejs/svelte/pull/18873))

[all merged prs](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Awaltuov+-user%3Awaltuov&type=pullrequests)

## `> projects`

**[Bloxsmith](https://bloxsmith.net)**: ai ui generation for roblox studio. describe an interface, refine it in chat, and sync the editable result into your game. ~19k signups so far.

## `> inference`

deployed, operated and tuned large open-weight moe models for local inference on 4× PRO 6000 Blackwell GPUs: quantization, sglang/flashinfer serving, tensor parallelism, speculative decoding, long-context caching, benchmarking and reproducible cloud deployment.

## `> get in touch`

- email: waltuecom@gmail.com
- happy to talk about anything, just reach out
