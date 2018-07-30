## 1.1 hello,world

```go
package main

import "fmt"

func main(){

    fmt.Println("Hello,world!")

}
```

> Go是编译型的语言。go命令配合其子命令，可以将源文件转变成机器相关的原生二进制指令。
>
> 子命令：run
>
> 它将一个或多个以.go为后缀的源文件进行编译、链接，然后运行生成的可执行文件。

```bash
$ go run helloworld.go
```

> 输出：

```bash
$ Hello,world!
```

> 子命令：build
>
> 生成一个可复用的二进制程序，它可以不用处理，随时执行。

```bash
$ go build helloworld.go
$ ./helloworld
```

> 输出：

```bash
$ Hello,world!
```

> Go代码是使用**包**来组织的。
>
> **包**类似于其他语言的**库**和**模块**的概念。
> 
> 一个包由一个或多个**.go源文件**组成，放在一个文件夹中，该文件夹名字描述了包的作用。
>
> 每一个源文件开始都用**package声明**，指明这个文件属于哪个包。
> 
> 后面跟着它导入的其他包的列表，然后是存储在文件中的程序声明。

## 1.2 命令行参数





