+++
title = "index"
insert_anchor_links = "right"
+++

## playonbsd-rs

This a toy project I started to learn a bit of Rust. It aims
at providing some libraries or tools to interact with the 
[PlayOnBSD database](https://github.com/playonbsd/OpenBSD-Games-Database).

For now, the project provides:

* [pobsd-parser](https://crates.io/crates/pobsd-parser): a library to easely parse
the PlayOnBSD database.

* [pobsd-db](https://crates.io/crates/pobsd-parser): a library to easely query
the PlayOnBSD database. Data can be loaded using the [pobsd-parser](https://crates.io/crates/pobsd-parser).

* [pobsd-utils](https://crates.io/crates/pobsd-utils): a binary to easely check or
export the PlayOnBSD database.

* [pobsd](https://crates.io/crates/pobsd): a TUI to browse the PlayOnBSD database.

* [igdb](https://crates.io/crates/pobsd): a fork of an existing but deprecated library for 
the API of the [IGDB](https://igdb.com) database.