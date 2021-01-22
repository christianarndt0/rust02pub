# Rust: From 0 To Publish

As software projects grow in size and/or time, organization and documentation of code becomes increasingly important. We humans tend to forget things and keeping track of an entire program structure naturally becomes more and more difficult as the project evolves.

By grouping related functionality and separating code with distinct features, it is easier to find particular features and where to change how something works. Additionally, especially if other developers are also supposed to work with your code and/or modify it, good documentation is just as important.

To do all of this in a standardized and consistent way in Rust, there is Cargo.

Cargo is the Rust package manager which downloads your package’s dependencies, compiles your packages, builds documentation, makes distributable packages, and uploads them to crates.io, the Rust community’s package registry.
