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

``` go
| break | default | func | interface | select |
| case | defer | go | map | struct |
| chan | else | goto | package | switch |
| const | fallthrough | if | range | type |
| continue | for | import | return | var |

```

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
    * 如果声明在函数内，它只在函数局部有效。
    * 如果声明在函数外，它将对包里面的所有源文件可见。
    
> 首字母大写决定其可见性是否跨包。
> 使用驼峰命名法。

## 2.2 声明
> 有4个主要声明：变量（var）、常量（const）、类型（type）、函数（func）。
> Go程序存储在一个或多个以.go为后缀的文件里。
    1. 每一个文件以package声明开头，表明文件属于哪个包。
    2. package声明后面是import声明。
    3. 然后是包级别的类型、变量、常量、函数的声明，不区分顺序。


``` go
// boiling 输出水的沸点
package main

import "fmt"

const boilingF = 212.0

func main(){
    var f = boilingF
    var c = (f - 32) * 5 / 9 
    fmt.Printf("boiling point = %g°F or %g°C\n", f, c)
    // 输出：
    // boiling porint = 212°F or 100°C
}
```



