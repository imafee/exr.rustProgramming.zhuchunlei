# 变量

rust 不同于其他编程语言：rust 的变量本质上是一种绑定语义（建立关联关系，即将一个变量名和一个值绑定在一起）。

## 变量名

- 字母（区分大小写）、数字（不能以数字开头）、下划线
- 不能仅仅是下划线（rust 的下划线是一种特殊的标识符）

## immutable 不可变性

默认声明为不可变，通过添加 mut 关键字改为可变变量

```rust
// 默认为immutable
fn main(){
  let x = 3;
  x = 5; // Error: can't assign twice to immutable variable x
}
// 手动开启mutable模式
fn main(){
  let mut x = 3; // 定义变量为可变类型
  x = 5;
  println!("x:{}",x); // 5
}
```

## 变量遮蔽

重复为变量声明同一个名字，但仍可以使用上一个同名变量

- 内层作用域定义的变量遮蔽外层
- 前面作用域定义的变量遮蔽后面

```rust
fn main(){
  let x = 3;
  let x = x+1;
  let x = x*2;
  println!("x:{}",x); // 8
  let x = "hello";
  println!("x:{}",x); // hello
}
```

## 常量

- 使用 const 来声明
- 变量名必须大写
- 必须指定值类型
- 常量不能遮蔽（不能重复定义）
- 可以在任何作用域中声明
- 赋值符右侧只能是常量表达式、数学表达式，不能接收函数返回值（不能是运行时才能确定的值，因为需要静态编译）

```rust
const MAX_NUM:u32 = 1024;
```