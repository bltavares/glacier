# Glacier

A big ‘ol pile of ICE.

[![Build Status](https://travis-ci.org/steveklabnik/glacier.svg?branch=master)](https://travis-ci.org/steveklabnik/glacier)

This repository is used to test internal compiler errors (also known as ICEs)
in [Rust]. An ICE means that something went wrong, something unexpected. As
such, sometimes, ICEs get randomly fixed. A compiler refactoring will remove
the odd code path, even if the point of the change wasn’t to fix the bug.

[Rust]: https://github.com/rust-lang/rust

As such, this repository is a collection of these bugs, and it runs on Rust
nightly, once a day, on Travis. If any of the ICEs stop happening, the build
will fail, and I can close the associated bug.

## Helping out

Contributing to Glacier is fairly easy:

1. Check out [this list][ices] of bugs on the Rust issue tracker.
2. Pick one.
3. Create a file in `src/` with the same digit as the bug. ([like this][29161])
4. Copy the code that causes the ICE into your new file. ([like this][file])
5. (optional) Verify it works by running `./test.sh` to run the tests.
6. Send a pull request! ([like this][pr])

[ices]: https://github.com/rust-lang/rust/issues/29249
[29161]: https://github.com/rust-lang/rust/issues/29161
[file]: https://github.com/steveklabnik/glacier/blob/master/src/29161.rs
[pr]: https://github.com/steveklabnik/glacier/pull/1

## License

MIT/Apache2, just like Rust.
