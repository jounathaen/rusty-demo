# rusty-demo

Small *Hello World* demo based on the unikernel [RustyHermit](https://github.com/hermitcore/libhermit-rs).
Please install the latest Rust compiler from the [official webpage](https://www.rust-lang.org/).

Further requirements are the source code of the Rust runtime, [cargo-download](https://crates.io/crates/cargo-download), and llvm-tools.
Please install these tools with following commands:

```sh
$ cargo install cargo-download
$ cargo install uhyve
$ rustup component add rust-src
$ rustup component add llvm-tools-preview
```

You can then create and start the demo application as follows:

```sh
$ cargo build -Z build-std=std,core,alloc,panic_abort --target x86_64-unknown-hermit
$ cargo run -Z build-std=std,core,alloc,panic_abort --target x86_64-unknown-hermit
```

Please read the README of [RustyHermit](https://github.com/hermitcore/libhermit-rs) for more information.

## License

Licensed under either of

* Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
* MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.
