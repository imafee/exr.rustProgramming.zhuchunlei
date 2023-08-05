# 《Rust 编程-入门、实战与进阶》朱春雷

ISBN 978-7-111-67910-3

## 要点

强类型静态编译语言
目标：高安全、高并发、高性能

内存安全的实现思路：

- 建立严格的内存管理模型（所有权系统和类型系统）
- 通过严格的编译器来检查代码中的每个变量和引用的每个内存指针
- 为每个变量建立了清晰的生命周期。

## 工具链

```shell
rustc - Compiler
rustup - toolchain
cargo - package manager
```

## 安装方法

[官方文档](https://www.rust-lang.org/tools/install)

```shell
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
rustc --version
rustup --version
cargo --version
```
