<!-- Copyright © SixtyFPS GmbH <info@slint.dev> ; SPDX-License-Identifier: GPL-3.0-only OR LicenseRef-Slint-Royalty-free-2.0 OR LicenseRef-Slint-Software-3.0 -->

# Slint

[![Crates.io](https://img.shields.io/crates/v/slint)](https://crates.io/crates/slint)
[![Docs.rs](https://docs.rs/slint/badge.svg)](https://docs.rs/slint)

# A Rust UI toolkit

[Slint](https://slint.rs) is a Rust based UI toolkit to build native user interfaces on desktop platforms and for embedded devices.
This crate provides the Rust APIs to interact with the user interface implemented in Slint.

The complete Rust documentation for Slint can be viewed online at https://slint.rs/docs/rust/slint/.

## Getting Started

The [crate documentation](https://slint.dev/docs/rust/slint/) shows how to use this crate.

### Hello World

The most basic "Hello world" application can be achieved with a few lines of code:

In your `Cargo.toml` add:

```toml
[dependencies]
slint = "1.7.0"
```

And in your `main.rs`:

```rust,no_run
slint::slint!{
    export component HelloWorld {
        Text {
            text: "hello world";
            color: green;
        }
    }
}
fn main() {
    HelloWorld::new().unwrap().run().unwrap();
}
```

The [`slint` crate documentation](https://slint.dev/docs/rust/slint/)
contains more advanced examples and alternative ways to use this crate.

To quickly get started, use the [Template Repository](https://github.com/slint-ui/slint-rust-template) with
the code of a minimal application using Slint as a starting point for your program.

```bash
git clone https://github.com/slint-ui/slint-rust-template my-project
```

## More examples

You can quickly try out the [examples](/examples) by cloning this repo and running them with `cargo run`

```sh
# Runs the "printerdemo" example
cargo run --release --bin printerdemo
```
