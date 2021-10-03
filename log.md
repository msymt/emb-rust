# 作業ログ

- 2021/10/03: 環境構築と文法
  - 結局`#[doc = include_str!("../README.md")]`をコメントアウトして済ませた．多分よくない
    - 参考になりそう：https://giters.com/clap-rs/clap/issues/2618?amp=1
  - p71まで進めた
    - 2つの違い何
    ```Rust
    fn main() {
      let mut array = [1, 2, 3, 4, 5];
      let slice = &mut array[1..3];
      println!("slice = {:?}", slice);
      println!("array = {:?}", array);
    }
    ```

    ```Rust
    fn main() {
      let mut array = [1, 2, 3, 4, 5];
      let slice = &mut array[1..3];
      println!("array = {:?}", array);
      println!("slice = {:?}", slice);
    }
    ```
- 2021/9/29: 環境構築
  - cargo install cargo-generate中にエラー.
    - unstableというなら，stableな書き方を教えて欲しい．
    - わからない．バージョン落す．
    - https://github.com/rust-lang/rust/pull/83366
    - rustよくわからないのに文法エラーと言われても対処法がよくわからない
    - ```
      error[E0658]: arbitrary expressions in key-value attributes are unstable
      --> $HOME/.cargo/registry/src/github.com-1ecc6299db9ec823/cargo-generate-0.10.1/src/lib.rs:1:9
      |
      | #[doc = include_str!("../README.md")]
      |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
      |
      = note: see issue #78835 <https://github.com/rust-lang/rust/issues/78835> for more information
      error: aborting due to previous error
      ```
  - rustup default 1.51.0