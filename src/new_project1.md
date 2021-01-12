# A Crate From Scratch

```bash
$ cargo new rust-boilerplate
   Created binary (application) `rust-boilerplate` package

$ tree rust-boilerplate/
rust-boilerplate/
├── Cargo.toml
└── src
    └── main.rs

$ cd rust-boilerplate/

$ cat src/main.rs 
fn main() {
    println!("Hello, world!");
}

$ cargo run
   Compiling rust-boilerplate v0.1.0 (/home/chris/Software/Rust/rust-boilerplate)
    Finished dev [unoptimized + debuginfo] target(s) in 0.97s
     Running `target/debug/rust-boilerplate`
Hello, world!

```
