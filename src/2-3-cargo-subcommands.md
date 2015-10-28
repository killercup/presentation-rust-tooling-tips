
### Add More Cargo Subcommands!

----

#### Count line numbers

[github.com/kbknapp/cargo-count](https://github.com/kbknapp/cargo-count)

```bash
$ cargo count -e target -s ,
```

```plain
Gathering information...
         Language  Files  Lines  Blanks  Comments  Code
         --------  -----  -----  ------  --------  ----
         TOML      5      104    19      0         85
         Rust      17     1,832  279     144       1,409
         --------  -----  -----  ------  --------  ----
Totals:            22     1,936  298     144       1,494
```

---

#### Outdated dependencies

Before you `cargo update`: [github.com/kbknapp/cargo-outdated](https://github.com/kbknapp/cargo-outdated)

```bash
$ cargo outdated
```

```plain
Checking for SemVer compatible updates...Done
Checking for the latest updates...Done
All dependencies are up to date, yay!
```

---

#### List dependencies

```bash
$ cargo list
```

```plain
libc  0.1.2
regex 0.1.41
```

(Part of [cargo-edit][cargo-edit].)

---

```bash
$ cargo list --tree
```

```plain
├── libc (0.1.10)
└── regex (0.1.41)
    ├── aho-corasick (0.3.4)
    │   └── memchr (0.1.6)
    │       └── libc (0.1.10)
    ├── memchr (0.1.6)
    │   └── libc (0.1.10)
    └── regex-syntax (0.2.2)
```

---

#### Add, remove dependencies

```bash
$ cargo add regex
```

Automatically adds the latest available version of `regex`.

Part [github.com/killercup/cargo-edit][cargo-edit] by yours truly.

Also contains `cargo rm`.


[cargo-edit]: https://github.com/killercup/cargo-edit

