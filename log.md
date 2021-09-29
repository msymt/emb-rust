# 作業ログ

- 2021/9/29: 環境構築
  - cargo install cargo-generate中にエラー.
    - unstableというなら，stableな書き方を教えて欲しい．
    - わからない．バージョン落す．
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