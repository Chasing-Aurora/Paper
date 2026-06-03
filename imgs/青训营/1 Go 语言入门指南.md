
## 实践篇：Go 语言入门指南:基础语法和常用特性解析｜青训营
[toc]
### 混乱
#### 回首
`Go语言` 语法格式类似于`c`，比如`struct,printf,&取值符`,但不同点也突出。

1. 删除了for，if的小括号，但强制添加大括号。只有for循环一种循环。

2. switch没有（），也没有break。 

3. 数组，map，slice也可以直接打印。

4. range有点类似于python中的enumerate函数。split返回列表类似python。

5. 函数更多时候有两个返回值，第二个是error。 

6. 函数定义可以放在调用之后。

7. Go的rune和byte代表字符。

#### 数组 切片 字典
```
var number1 [5]int
var number = [5]int{1, 2}
numbers := [5]int{1, 2, 3, 4, 5}

var slice []int
var slice1 = []int{1, 2}
slice2 := []int{1, 3}
var slice4 = make([]int, 3)
slice5 := make([]int, 4) 

var a map[string]int
var a1 = map[string]int{"one": 1, "two": 2}
d1 := map[string]int 
var b = make(map[string]int)
c := make(map[string]int)
```		
#### 输出函数
- Print将它的参数显示在命令窗口，并将输出光标定位在所显示的最后一个字符之后。
- Print: 输出到控制台(不接受任何格式化，它等价于对每一个操作数都应用 %v)
- Println 将它的参数显示在命令窗口，并在结尾加上换行符，将输出光标定位在下一行的开始。
- 当需要格式化输出信息时一般选择 Printf，其他时候用 Println 就可以了。
- 在 Go 中，字符串格式化通常使用 `fmt` 包提供的 `Printf / Sprintf / Fprintf` 函数。
	- Sprintf() 是把格式化字符串输出到指定的字符串中，可以用一个变量来接受，然后在打印。
	- Fprintf() 是把格式字符串输出到指定的文件设备中，所以参数比Printf 多一个文件指针*File。
### 并发
- go中的多线程编程称为goroutine，目前统一译为协程。
- go语言里的并发指的是能让某个函数独立于其他函数运行的能力。当一个函数创建goroutine时，go语言会将其视为一个独立的工作单元，这个单元会被调度到可用的逻辑处理器上执行。
- go语言提供的消息通信机制称为channel，go语言在设计上强调不要通过共享内存来通信，而应该通过通信来共享内存。
### 结构体
1. 定义 `type user struct`结构体是一种用户自定义的数据类型，用于封装一组相关的字段（属性）和方法（行为）。可以将结构体看作是一个包含多个字段的记录，每个字段可以是不同的数据类型。
2. 实现---用：=
	- 字典键值对
	- 集合只有值
	- 字典+属性
3. 结构体方法---把函数的第一个实体的参数提到前边然后加上括号。
### 字符串格式化
|占位符|说明|
|--|--|
| %v | 以默认的方式打印变量的值--占位符,go语言会自动为你识别|
| %T|打印变量的类型|
|%+d|带符号的整型|
|%q|字符串带双引号，字符串中的引号带转义符,对于数字打印单引号|
|%t|打印True或False|
- 对于结构体
	- `%+v`  显示结构体的字段名。
	- `%#v`  更加详细，显示生成该值的包名和字段名
### 解析时间字符串
- `rand.Seed(time.Now().Unix())` 和 `rand.Seed(time.Now().UnixNano())` 作为种子是不一样的：

	-  前者使用当前时间的 Unix 时间戳（秒数）作为种子。这意味着在同一秒内调用得到的种子是相同的，它们会生成相同的随机序列。
    
	- 后者 使用当前时间的 Unix 时间戳的纳秒部分作为种子。由于纳秒的值比秒更精确，所以这种方式生成种子的时间间隔更短，可以得到更不同的随机序列。在同一秒内调用 得到的种子是不同的，它们会生成不同的随机序列。

- 因此，如果需要使用更相对独立且不同的随机序列，建议使用后者作为种子，因为纳秒级的时间戳提供了更高的精度。

- GMT是前世界标准时，UTC是现世界标准时。
UTC 比 GMT更精准，以原子时计时，适应现代社会的精确计时。但在不需要精确到秒的情况下，二者可以视为等同。

```

t.Format("2006-01-02 15:04:05") t3, err := time.Parse("2006-01-02 15:04:05", "2022-03-27 01:25:36")    if err != nil {   panic(err)   }

```


### 解析数字字符串
- `n2, _ := strconv.Atoi("123")`
- `n, _ := strconv.ParseInt("111", 10, 64)`
- `f, _ := strconv.ParseFloat("1.234", 64)`

![forthebadge](https://forthebadge.com/images/badges/built-by-developers.svg)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTgwOTkwODgxMV19
-->