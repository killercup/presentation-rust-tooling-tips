
### rustc

Compiling Rust code:

```bash
$ rustc -O src/main.rs
```

(Don't forget `-O` if you want to enable compiler optimizations!)

---

Explain errors:

```bash
$ rustc --explain E0106
```

Can also be found on <https://doc.rust-lang.org/error-index.html>

(You can help extend those messages! See [Github Issue #24407](https://github.com/rust-lang/rust/issues/24407))

---

List built-in lints:

```bash
$ rustc -W help
```

