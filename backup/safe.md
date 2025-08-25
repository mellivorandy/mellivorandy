<details>
    <summary>💔</summary>
    Even the borrow checker can’t protect a heart from a dangling lifetime.
    Love, like memory, is best borrowed — but only if it lives long enough.
    For affection is a reference: safe, valid, but never owned.
    And like any borrow, it only lasts as long as the lifetime holds.
</details>

<br>

It compiled. The borrow checker approved. But she never ran the binary. ⚡

```rust
use std::fmt;

struct Heart<'a> {
    memory: &'a str,
}

fn main() {
    let confession = String::from("I like you, but I can't express it safely...");

    let safe_love = Heart { memory: &confession };

    // drop(confession); // error[E0505]: cannot move out of `confession` because it is borrowed

    println!("💌 Love is safe: {}", safe_love);
    println!("🦀 Segfaultless in Kaohsiung. Thanks, borrow checker.");
}

impl fmt::Display for Heart<'_> {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "{}", self.memory)
    }
}

```
