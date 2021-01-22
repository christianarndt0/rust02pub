# Installing Rust

Starting from 0 means installing the *Rust* programming language in the first place. Fortunately, it couldn't be easier:

## Unix-like (Linux, MacOS)

On Unix, run

```console
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh 
```

in your shell. This downloads and runs `rustup-init.sh`, which in turn downloads and runs the correct version
of the `rustup-init` executable for your platform.

## Windows

On Windows, download and run [rustup-init.exe](https://win.rustup.rs/x86_64).

## Updating Rust

```console
rustup update
```
