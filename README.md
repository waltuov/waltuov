## `> whoami`

```
rust and typescript build tooling. i fix bugs upstream and build with ai.
also: web, ecommerce, security, local llm inference.
```

## `> open source`

mostly working on cc-rs, plus tokio and mio on windows. also wasm-bindgen, rolldown and oxc. some merged fixes:

- cc-rs: masm files for x86 windows targets now fall back to `llvm-ml` when `ml64.exe` isn't there, so they cross compile from linux and macos, and `CC_MASM_ASM` picks the assembler ([#1975](https://github.com/rust-lang/cc-rs/pull/1975))
- cc-rs: build scripts can now split compiling, archiving and linking with `Build::create_archive` and `emit_link_directives`, and still get cc's link setup right ([#1972](https://github.com/rust-lang/cc-rs/pull/1972))
- cc-rs: the static c++ stdlib now links with `-bundle`, so it works with mingw, and a new `CXXSTDLIB_STATIC` env var turns it on from outside the crate ([#1955](https://github.com/rust-lang/cc-rs/pull/1955), [#1957](https://github.com/rust-lang/cc-rs/pull/1957))
- mio: vectored reads and writes on windows named pipes now use every buffer, not just the first ([#2013](https://github.com/tokio-rs/mio/pull/2013))
- tokio: output written through `tokio::io::stdout()` no longer gets lost when the runtime shuts down ([#8506](https://github.com/tokio-rs/tokio/pull/8506))
- wasm-bindgen: two `inline_js` snippets that import the same name now each get their own binding instead of silently sharing one ([#5352](https://github.com/wasm-bindgen/wasm-bindgen/pull/5352))
- pnpm: package removal waits out windows file locks instead of failing ([#15409](https://github.com/pnpm/pnpm/pull/15409))
- rolldown: dev mode now notices a deleted or recreated file instead of serving a stale resolve ([#10986](https://github.com/rolldown/rolldown/pull/10986))
- oxc: oxfmt no longer drops a comment before `=` and prints the one after it twice ([#26997](https://github.com/oxc-project/oxc/pull/26997))
- insta: `cargo insta test --all-targets` with nextest no longer fails on its separate doctest run ([#941](https://github.com/mitsuhiko/insta/pull/941))
- svelte: `let:` next to a `children` snippet is now a compile error instead of a runtime crash ([#18873](https://github.com/sveltejs/svelte/pull/18873))

[all merged prs](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Awaltuov+-user%3Awaltuov&type=pullrequests)

## `> projects`

**[Bloxsmith](https://bloxsmith.net)**: ai ui generation for roblox studio. describe an interface, refine it in chat, and sync the editable result into your game. ~20k signups so far.

## `> inference`

deployed, operated and tuned large open-weight moe models for local inference on 4× PRO 6000 Blackwell GPUs: quantization, sglang/flashinfer serving, tensor parallelism, speculative decoding, long-context caching, benchmarking and reproducible cloud deployment.

## `> get in touch`

- email: waltuecom@gmail.com
- happy to talk about anything, just reach out

