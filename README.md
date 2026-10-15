## `> whoami`

```
rust and typescript build tooling. i fix bugs upstream and build with ai.
also: web, ecommerce, security, local llm inference.
```

## `> open source`

mostly working on cc-rs, plus tokio and mio on windows. also wasm-bindgen, rolldown and oxc. some merged fixes:

- cc-rs: build scripts can now collect the commands cc runs and write a `compile_commands.json`, so clangd and other c tooling understand the c code in rust crates. asked for since 2020 ([#1990](https://github.com/rust-lang/cc-rs/pull/1990))
- cc-rs: masm files for x86 windows targets now fall back to `llvm-ml` when `ml64.exe` isn't there, so they cross compile from linux and macos, and `CC_MASM_ASM` picks the assembler ([#1975](https://github.com/rust-lang/cc-rs/pull/1975))
- cc-rs: c++ stdlib linking: cc now links `libc++` when clang uses it instead of assuming `libstdc++`, the static stdlib links with `-bundle` so it works with mingw, and `CXXSTDLIB_STATIC` turns it on from outside the crate ([#1978](https://github.com/rust-lang/cc-rs/pull/1978), [#1955](https://github.com/rust-lang/cc-rs/pull/1955), [#1957](https://github.com/rust-lang/cc-rs/pull/1957))
- mio: windows named pipes now use every buffer in vectored reads and writes, and size reads to the caller's buffer (up to 64 KiB) instead of always 4 KiB ([#2013](https://github.com/tokio-rs/mio/pull/2013), [#2022](https://github.com/tokio-rs/mio/pull/2022))
- tokio: output written through `tokio::io::stdout()` no longer gets lost when the runtime shuts down ([#8506](https://github.com/tokio-rs/tokio/pull/8506))
- tokio: closing a semaphore and reading or writing a `tokio::io::duplex` pipe now wake waiting tasks after letting go of the lock, so a waker that touches the same semaphore or pipe can't hang the thread ([#8529](https://github.com/tokio-rs/tokio/pull/8529), [#8618](https://github.com/tokio-rs/tokio/pull/8618))
- wasm-bindgen: slice arguments: the typescript types of exported functions now accept a plain array for `&[u8]`, `&[f64]` and other number slices, and debug builds check slice and vector arguments, so an `ArrayBuffer` passed as `&[u8]` or the wrong typed array for `&mut [T]` throws a clear error instead of silently giving empty or corrupted data ([#5373](https://github.com/wasm-bindgen/wasm-bindgen/pull/5373), [#5367](https://github.com/wasm-bindgen/wasm-bindgen/pull/5367))
- wasm-bindgen: two `inline_js` snippets that import the same name now each get their own binding instead of silently sharing one ([#5352](https://github.com/wasm-bindgen/wasm-bindgen/pull/5352))
- pnpm: package removal waits out windows file locks instead of failing ([#15409](https://github.com/pnpm/pnpm/pull/15409))
- rolldown: `preserveModules` builds now sanitize chunk names like `Comp.vue?vue&type=script`, which broke vue library builds on windows ([#11087](https://github.com/rolldown/rolldown/pull/11087))
- oxc: the minifier no longer turns `(0, o?.f)()` or `(t = o.f)()` into a call with a different `this`, or an indirect `eval` into a direct one ([#27082](https://github.com/oxc-project/oxc/pull/27082))
- svelte: `let:` next to a `children` snippet is now a compile error instead of a runtime crash ([#18873](https://github.com/sveltejs/svelte/pull/18873))

[all merged prs](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Awaltuov+-user%3Awaltuov&type=pullrequests)

## `> projects`

**[Bloxsmith](https://bloxsmith.net)**: ai ui generation for roblox studio. describe an interface, refine it in chat, and sync the editable result into your game. ~20k signups so far.

## `> inference`

deployed, operated and tuned large open-weight moe models for local inference on 4× PRO 6000 Blackwell GPUs: quantization, sglang/flashinfer serving, tensor parallelism, speculative decoding, long-context caching, benchmarking and reproducible cloud deployment.

## `> get in touch`

- email: waltuecom@gmail.com
- happy to talk about anything, just reach out

