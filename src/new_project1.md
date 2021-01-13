# A Crate From Scratch

From your favorite directory, create a new crate with:

```console
$ cargo new rust-boilerplate
   Created binary (application) `rust-boilerplate` package
```

This creates some basic package boilerplate and also initializes a new git repository. Neat!

```console
$ tree rust-boilerplate/ -a
rust-boilerplate/
├── Cargo.toml
├── .git
│   ├── ...
├── .gitignore
└── src
    └── main.rs
```

```console
$ cat rust-boilerplate/src/main.rs 
fn main() {
    println!("Hello, world!");
}
```

Now you should be able to run the new crate's simple hello world function from the projects root directory.

```console
$ cargo run
   Compiling rust-boilerplate v0.1.0 (/home/chris/Software/Rust/rust-boilerplate)
    Finished dev [unoptimized + debuginfo] target(s) in 0.97s
     Running `target/debug/rust-boilerplate`
Hello, world!
```

## More Basic Boilerplate

### Adding A Placeholder Library

Create `src/lib.rs` and put

```rust
pub fn hello() {
    println!("Hello, world!");
}
```

inside.

Now use this library in the crate's entrypoint by changing `main.rs` to

```rust
extern crate rust_boilerplate as bp;


fn main() {
    bp::hello();
}
```

#### Adding A Unit Test

TODO

### Adding An Integration Test

TODO

```bash
$ mkdir tests
```