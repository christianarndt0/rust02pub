# Installation

## Unix-like (Linux, MacOS)

On Unix, run

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh 
```

in your shell. This downloads and runs `rustup-init.sh`, which in turn downloads and runs the correct version
of the `rustup-init` executable for your platform.

### Update

```bash
rustup update
```

## Windows

On Windows, download and run [rustup-init.exe](https://win.rustup.rs/x86_64).
