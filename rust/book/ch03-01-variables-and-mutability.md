原文：[https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html](https://doc.rust-lang.org/book/ch03-01-variables-and-mutability.html)

# 变量和可变性

就好像在"Storing Values with Variables"（将值存入变量）这一部分提到的，默认`Rust`变量是不可变的(immutable)。这也是`Rust`让你编写更加安全和更容易并发代码的一种方式。当然，你还是可以让你的变量可以变化的。让我们来看看`Rust`是如何以及为什么鼓励你使用不可变的变量，以及在什么时候我们需要使用正常可变的变量。

所谓变量不可变(immutable)，就是一旦一个值和一个变量名绑定，你就不能更改这个值了。为了说明这个，让我们创建一个名叫*variables*的项目，可以使用`cargo new variables`命令。

然后进入新创建的*variables*目录，打开`src/main.rs`文件，将文件内容替换为下面的代码。这代码是不能正常编译的，主要是来解释默认变量是不可变的。

Filename: *src/main.rs*

```
fn main() {
    let x = 5;
    println!("The value of x is: {x}");
    x = 6;
    println!("The value of x is: {x}");
}
```

保存，然后运行程序。使用`cargo run`命令。你就可以看到一下出错信息了：

![mutability error](./images/ch03-01-immutable.png)



