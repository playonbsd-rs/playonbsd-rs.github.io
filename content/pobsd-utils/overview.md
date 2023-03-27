+++
title = "Overview"
weight = 1
+++
## pobsd-utils
pobsd-utils is a tool written in Rust designed to interact with the PlayOnBSD
database that can be find [here](https://github.com/playonbsd/OpenBSD-Games-Database)

It makes use of both `plege(2)` and `unveil(2)`.

At the moment, it provides two functionalities:
- checking the database integrity (at the moment, in a minimal way)
- exporting the database in a different format (at the moment, only json)


### Installing
You can install it using `cargo` with `cargo install pobsd-utils`.
Make sure to update to your `$PATH` to be able to use 
it (usually by adding `$HOME/.cargo/bin`).

### Checking the database integrity
For now, it boils down to checking if the parser can
parse the database and tells where the parser found
errors. 
```
$ pobsd-utils check games.db 
> 356 games parsed without error
$ pobsd-utils check faulty-games.db
> 356 games parsed
> Errors occured at lines 15, 24.
```
If there is an error, it should be fixed before using the
other functions of pobsd since this could lead to wrong
data being displayed or exported.

### Exporting the database
At the moment, the only format available is json.
```
$ pobsd-utils export games.db games.json 
```
