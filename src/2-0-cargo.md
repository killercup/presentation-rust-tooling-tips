
## Cargo

---

With Cargo, you can easily

+ compile Rust projects
+ manage dependecies
+ render documentation
+ run tests, benchmarks, examples

---

### Compiling Rust Code

---

#### Without Cargo

```bash
$ rustc -O src/main.rs
```

---

#### Let's add some external libraries!

```bash
$ rustc src/bin/add/main.rs --crate-name cargo_add --crate-type bin -C opt-level=3 --cfg feature=\"default\" --out-dir /Users/pascal/Projekte/cargo-edit/target/release --emit=dep-info,link -L dependency=/Users/pascal/Projekte/cargo-edit/target/release -L dependency=/Users/pascal/Projekte/cargo-edit/target/release/deps --extern rustc_serialize=/Users/pascal/Projekte/cargo-edit/target/release/deps/librustc_serialize-7ff5bfc027146194.rlib --extern toml=/Users/pascal/Projekte/cargo-edit/target/release/deps/libtoml-7d16d978f944b9c6.rlib --extern curl=/Users/pascal/Projekte/cargo-edit/target/release/deps/libcurl-89d04227df05c87c.rlib --extern pad=/Users/pascal/Projekte/cargo-edit/target/release/deps/libpad-8b41ff1b2f475326.rlib --extern quick_error=/Users/pascal/Projekte/cargo-edit/target/release/deps/libquick_error-f3aa3728a185a974.rlib --extern docopt=/Users/pascal/Projekte/cargo-edit/target/release/deps/libdocopt-398ed9badedc4dd3.rlib --extern semver=/Users/pascal/Projekte/cargo-edit/target/release/deps/libsemver-41b5af09b2b837dc.rlib --extern cargo_edit=/Users/pascal/Projekte/cargo-edit/target/release/libcargo_edit.rlib -L native=/usr/lib -L native=/usr/local/Cellar/openssl/1.0.2d_1/lib -L native=/Users/pascal/Projekte/cargo-edit/target/release/build/openssl-sys-f0bee5fb97afc90d/out
```

---

#### With Cargo:

```bash
$ cargo build --release
```
