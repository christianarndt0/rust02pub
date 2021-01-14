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

Now you should be able to run the new crate's simple executable from the project's root directory.

```console
$ cargo run
   Compiling rust-boilerplate v0.1.0 (/home/chris/Software/Rust/rust-boilerplate)
    Finished dev [unoptimized + debuginfo] target(s) in 0.97s
     Running `target/debug/rust-boilerplate`
Hello, world!
```

## More Basic Boilerplate

Cargo creates a very basic project with only the bare necessities to run an executable rust application.
However, most projects require a lot more "infrastracture". Let's provide some more basic stuff that you will generally need.

### Adding A Library

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

### Adding A Module (Or Two)

```console
chris@XPS15:~/Software/Rust/rust-boilerplate$ tree .
.
├── Cargo.lock
├── Cargo.toml
├── README.md
├── src
│   ├── config2
│   │   ├── mod.rs
│   │   └── subconfig.rs
│   ├── config.rs
│   ├── lib.rs
│   └── main.rs
```

#### Simple Modules VS Nested Module

```rust
mod subconfig;

pub struct Config2 {
    pub greeting: String,
}


impl Config2 {
    pub fn default() -> Self {
        Config2 {
            greeting: String::from("Hello, world!"),
        }
    }

    pub fn print(&self) {
        println!("Config2.greeting = {}", self.greeting);
        subconfig::subconfig_func();
    }
}
```

```rust
pub fn subconfig_func() {
    println!("called subconfig_func");
}
```

```rust
pub struct Config {
    pub greeting: String,
}


impl Config {
    pub fn default() -> Self {
        Config {
            greeting: String::from("Hello, world!"),
        }
    }

    pub fn print(&self) {
        println!("Config.greeing = {}", self.greeting);
    }
}
```

**Above is essentially the same thing, stick with "simple" config here and create _utils_ package**

### Creating A Utils Module

TODO
