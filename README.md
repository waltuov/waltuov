hi, i'm waltu. i'm self-employed and have been making and running my own projects in different niches since i was a teen. one of them is [Bloxsmith](https://bloxsmith.net): ai ui generation for roblox studio, ~20k signups so far.

on the open source side i work on rust and typescript build tooling and fix bugs upstream, mostly in [cc-rs](https://github.com/rust-lang/cc-rs) right now, plus tokio and mio on windows. i build with ai. also web, ecommerce and security stuff.

### some merged prs

- cc-rs: `compile_commands.json` output ([#1990](https://github.com/rust-lang/cc-rs/pull/1990))
- cc-rs: masm falls back to `llvm-ml`, so x86 windows targets cross compile from linux and macos ([#1975](https://github.com/rust-lang/cc-rs/pull/1975))
- cc-rs: links libc++ when clang uses it, and the static c++ stdlib works with mingw ([#1978](https://github.com/rust-lang/cc-rs/pull/1978), [#1955](https://github.com/rust-lang/cc-rs/pull/1955), [#1957](https://github.com/rust-lang/cc-rs/pull/1957))
- mio: vectored io for windows named pipes, and reads sized to the caller's buffer instead of 4 KiB ([#2013](https://github.com/tokio-rs/mio/pull/2013), [#2022](https://github.com/tokio-rs/mio/pull/2022))
- tokio: fixed stdout output getting lost when the runtime shuts down ([#8506](https://github.com/tokio-rs/tokio/pull/8506))
- tokio: fixed a hang when a waker touches the same semaphore or duplex pipe ([#8529](https://github.com/tokio-rs/tokio/pull/8529), [#8618](https://github.com/tokio-rs/tokio/pull/8618))
- wasm-bindgen: plain arrays for number slices in the typescript types, and debug checks for slice args ([#5373](https://github.com/wasm-bindgen/wasm-bindgen/pull/5373), [#5367](https://github.com/wasm-bindgen/wasm-bindgen/pull/5367))
- wasm-bindgen: fixed two `inline_js` snippets with the same import sharing one binding ([#5352](https://github.com/wasm-bindgen/wasm-bindgen/pull/5352))
- pnpm: package removal waits out windows file locks ([#15409](https://github.com/pnpm/pnpm/pull/15409))
- rolldown: fixed `preserveModules` chunk names that broke vue library builds on windows ([#11087](https://github.com/rolldown/rolldown/pull/11087))
- oxc: fixed the minifier changing `this` in calls like `(0, o?.f)()` ([#27082](https://github.com/oxc-project/oxc/pull/27082))
- svelte: `let:` next to a `children` snippet is a compile error now instead of a runtime crash ([#18873](https://github.com/sveltejs/svelte/pull/18873))

[all of them](https://github.com/search?q=is%3Apr+is%3Amerged+author%3Awaltuov+-user%3Awaltuov&type=pullrequests)

### local inference

deployed and tuned big open-weight moe models on 4x pro 6000 blackwell gpus (sglang, quantization, speculative decoding, long context).

waltuecom@gmail.com if you want to chat
