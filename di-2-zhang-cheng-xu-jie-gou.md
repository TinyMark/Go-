> 任何大程序，都是从小的基本组件构建而来：
* 变量存储值；
* 简单表达式通过各种操作合并成大的；
* 基本类型通过数组和结构体进行聚合；
* 表达式通过 if 和 for 等语句来决定执行顺序；
* 语句被组织成函数用于隔离和复用；
* 函数被组织成源文件和包。

## 2.1 名称
> 规则：
1. 名称的开头是字母或下划线。
2. 后面可以跟任意数量的字符、数字、下划线，区分大小写。
3. 不能使用 **关键字**。

* Go有25个关键字

| | | | | |
| ------ | ------ | ------ | ------ | ------ |
| break | default | func | interface | select |
| case | defer | go | map | struct |
| chan | else | goto | package | switch |
| const | fallthrough | if | range | type |
| continue | for | import | return | var |

* 30+内置的预声明的常量、类型和函数：
    

    
``` go
常量：
true        false        iota        nil
类型：
int         int8         int16         int32         int64
uint        uint8        uint16        uint32        uint64         uintptr
float32     float64      complex128    complex64
bool        byte         rune          string        error
函数：
make        len          cap           new           append         copy         close        delete
complex     real         imag
panic       recover
```



     
> 这些名称不是预留的，可以使用它们。**但是有冲突的风险。**