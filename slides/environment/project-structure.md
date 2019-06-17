## Project structure

<pre>
app/
|── .cargo/
    └── config # Build configuration (proxy, alias)
|── src/
    ├── lib.rs # Crate root. Defines public modules
    ├── main.rs # Executable
    └── api/ # Local crate
        └── mod.rs # api crate root
            └── find.rs # find endpoint
            └── delete.rs
            └── model.rs
|── target/
    └── debug/
    └── release/
        └── app # executable (.exe for Win)
|── Cargo.lock # External crates hashes
|── Cargo.toml