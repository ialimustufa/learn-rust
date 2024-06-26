# Getting Started with Rust

Learn to use Rust, a systems programming language known for its performance and safety, especially in concurrent environments.

## Install Rust

Follow these steps to install Rust on your system:

1. **Open your terminal.**
2. **Run the Rust installation script** by pasting the following command:
    ```sh
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```
    This script will install `rustup`, which is a toolchain manager for Rust.

3. **Follow the on-screen instructions** to complete the installation.

## Verify Installation

Check that Rust is installed correctly:
```sh
rustc --version
```

This command should display the installed version of Rust.

## Writing Your First Rust Program

Create a new project and write your first program:

1. **Create a new project using Cargo** (Rust’s package manager and build system):
    ```sh
    cargo new hello_world
    cd hello_world
    ```

2. **Edit `src/main.rs`** to contain the following code:
    ```rust
    fn main() {
        println!("Hello, world!");
    }
    ```

3. **Build and run your program**:
    ```sh
    cargo run
    ```

## Important Rust Concepts

- **Ownership:** Unique feature of Rust that makes it possible to manage memory safely without a garbage collector.
- **Borrowing:** Mechanism by which ownership of a resource can be temporarily transferred.
- **Lifetimes:** A way of describing the scope for which a reference is valid.
- **Concurrency:** Rust provides powerful tools to handle concurrent programming safely.

## Learning Resources

to be added.

## Community Resources

to be added.

## Sample Rust Code

Here’s a simple example of reading user input and printing it:
```rust
use std::io;

fn main() {
    println!("Enter your name:");

    let mut name = String::new();

    io::stdin()
        .read_line(&mut name)
        .expect("Failed to read line");

    println!("Hello, {}!", name.trim());
}