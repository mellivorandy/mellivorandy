<h1 align="center">Hello, I'm An-I Yu 👋</h1>
<p align="center">
  <em>🦀 Rustacean at Heart</em>
</p>

## 🐝 About Me

- 🎓 I'm a Computer Science and Information Engineering student.
- 🧵 Passionate about **system-level programming**.
- 💡 I believe in learning by **doing**, **sharing**, and **breaking things** to build better ones.
- ⚡ Fun fact: The value is immutable. Just like that one conversation you should’ve ended.
  > `` error[E0596]: cannot borrow `x` as mutable, as it is not declared as mutable ``

<br>

## 🛠️ Tech Stack

![Rust](https://img.shields.io/badge/-Rust-ffffff?style=flat&logo=rust&logoColor=000)
![Python](https://img.shields.io/badge/-Python-FFD43B?style=flat&logo=python)
![Linux](https://img.shields.io/badge/-Linux-f0f0f0?style=flat&logo=linux)

<br>

## 🏆 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=mellivorandy&show_icons=true&theme=tokyonight" width="420" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=mellivorandy&layout=compact&theme=tokyonight" width="320" />
</p>

<br>

## 📫 How to reach me

- <details>
    <summary>📧 My email</summary>
    anydoyi [at] gmail [dot] com
  </details>

<br>

---

<br>

<details>
    <summary>💭 Fun bits</summary>
        <br>
        It compiled. The borrow checker approved. But she never ran the binary. <br><br>
<details>
    <summary>💔</summary>
    Even the borrow checker can’t protect a heart from a dangling lifetime.
    Love, like memory, is best borrowed — but only if it lives long enough.
    For affection is a reference: safe, valid, but never owned.
    And like any borrow, it only lasts as long as the lifetime holds.
</details>

<br>

```rust
use std::fmt;

struct Heart<'a> {
    memory: &'a str,
}

fn main() {
    let confession = String::from("I like you, but I can't express it safely...");

    let safe_love = Heart { memory: &confession };

    // drop(confession); // error[E0505]: cannot move out of `confession` because it is borrowed

    println!("💌 Love is safe: {}", safe_love.memory);
    println!("🦀 Segfaultless in Kaohsiung. Thanks, borrow checker.");
}

impl fmt::Display for Heart<'_> {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "{}", self.memory)
    }
}

```
</details>
