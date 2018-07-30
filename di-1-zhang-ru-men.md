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





