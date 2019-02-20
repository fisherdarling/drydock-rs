# drydock-rs
An alternate crates registry for the Rust programming language.

## Alternative Crates Documentation:
https://github.com/rust-lang/cargo/blob/master/src/doc/src/reference/registries.md

// Tentative Example Usage, not neccessarily how the final api will look.
# Example Usage (Local Registry):
- Create a folder for local-storage:
> `$ mkdir my-registry`
- Create an empty index in the folder:
> `$ drydock init --local ./my-registry`
- Start drydock in the folder:
> `$ drydock serve --local ./my-registry`
## Publish an existing repo to the local-registry:
> `$ drydock add --local ./my-registry`
- Publish the current repo to the local registry
> `$ drydock publish --registry my-registry`
## Use the local registry in another crate:
> `$ drydock add --local ./my-registry`
- Edit your `Cargo.toml`:
```
[dependencies]
my-other-crate = { version = "*", registry = "my-registry" }
```
