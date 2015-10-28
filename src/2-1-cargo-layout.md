
### Cargo Project Layout

---

```plain
▾ src/          # source files
  lib.rs        # main entry point for libraries
  main.rs       # main entry point for executables
  ▾ bin/        # (optional) additional executables
    *.rs
▾ examples/     # (optional) examples
  *.rs
▾ tests/        # (optional) integration tests
  *.rs
▾ benches/      # (optional) benchmarks
  *.rs
```

---

```plain
▾ src/          # cargo (build|test|bench|doc)
  lib.rs        # cargo build
  main.rs       # cargo run
  ▾ bin/
    foo.rs      # cargo run --bin=foo
▾ examples/
  bar.rs        # cargo run --example=bar
▾ tests/        # cargo test
  *.rs
▾ benches/      # cargo bench (unstable)
  *.rs
```

