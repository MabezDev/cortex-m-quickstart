# Corrupted backtrace example

1. Configure `memory.x` and default target for your board
2. `cargo run`
3. Continue until `Breakpoint 3, rust_begin_unwind`
4. Run `bt` in GDB:
  ```
    (gdb) bt
    #0  rust_begin_unwind (_info=0x2000ff18)
        at /home/mabez/.cargo/registry/src/github.com-1ecc6299db9ec823/panic-halt-0.2.0/src/lib.rs:32
    #1  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #2  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #3  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #4  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #5  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #6  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #7  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #8  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #9  0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #10 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #11 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #12 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #13 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #14 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    #15 0x08000640 in core::panicking::panic_fmt () at src/libcore/panicking.rs:84
    --Type <RET> for more, q to quit, c to continue without paging--
  ```