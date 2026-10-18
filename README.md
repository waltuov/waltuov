hi, i'm waltu. i'm self-employed and have been making and running my own projects since i was a teen, from online stores and tiktok pages to software. right now that's ai products and rust build tooling. i like getting deep into one problem for hours, mostly in engineering, ai or security. i build with ai.

### my own work

- [Bloxsmith](https://bloxsmith.net): ai ui generation for roblox studio. describe an interface, refine it in chat, and sync the editable result into your game. 21k+ signups so far.
- local inference: deployed and tuned big open-weight moe models on 4x pro 6000 blackwell gpus (sglang, quantization, speculative decoding, long context).

### open source

most of my upstream work is in [cc-rs](https://github.com/rust-lang/cc-rs), the crate rust build scripts use to compile c and c++ code. 20+ merged prs there so far, some of them:

- cc-rs: `compile_commands.json` output, so clangd and other c tools understand the c code in rust crates. asked for since 2020 ([#1990](https://github.com/rust-lang/cc-rs/pull/1990))
- cc-rs: masm falls back to `llvm-ml`, so x86 windows targets cross compile from linux and macos ([#1975](https://github.com/rust-lang/cc-rs/pull/1975))
- cc-rs: links libc++ when clang uses it, and the static c++ stdlib works with mingw ([#1978](https://github.com/rust-lang/cc-rs/pull/1978), [#1955](https://github.com/rust-lang/cc-rs/pull/1955), [#1957](https://github.com/rust-lang/cc-rs/pull/1957))
- tokio: fixed stdout output getting lost when the runtime shuts down, and a hang when a waker touches the same semaphore or duplex pipe ([#8506](https://github.com/tokio-rs/tokio/pull/8506), [#8529](https://github.com/tokio-rs/tokio/pull/8529), [#8618](https://github.com/tokio-rs/tokio/pull/8618))
- mio: vectored io for windows named pipes, and reads sized to the caller's buffer instead of 4 KiB ([#2013](https://github.com/tokio-rs/mio/pull/2013), [#2022](https://github.com/tokio-rs/mio/pull/2022))
- wasm-bindgen: plain arrays for number slices in the typescript types, and debug checks for slice args ([#5373](https://github.com/wasm-bindgen/wasm-bindgen/pull/5373), [#5367](https://github.com/wasm-bindgen/wasm-bindgen/pull/5367))
- also fixes in pnpm, rolldown, oxc and svelte ([pnpm#15409](https://github.com/pnpm/pnpm/pull/15409), [rolldown#11087](https://github.com/rolldown/rolldown/pull/11087), [oxc#27082](https://github.com/oxc-project/oxc/pull/27082), [svelte#18873](https://github.com/sveltejs/svelte/pull/18873))

[all merged prs](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Awaltuov+-user%3Awaltuov&type=pullrequests)

open to the right role. waltuecom@gmail.com if you want to chat
