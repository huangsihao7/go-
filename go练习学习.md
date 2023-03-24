# go练习学习

## cap()的使用

```
package main

import "fmt"

func main() {
	// 创建一个长度为 5，容量为 10 的整数切片
	s := make([]int, 5, 10)

	// 打印切片长度和容量
	fmt.Printf("slice length: %d, capacity: %d\n", len(s), cap(s))

	// 创建一个长度为 5 的整数映射
	m := make(map[int]int, 5)

	// 添加 5 个键值对到映射中
	for i := 0; i < 5; i++ {
		m[i] = i * 10
	}

	// 打印映射长度和容量
	fmt.Printf("map length: %d, capacity: %d\n", len(m), cap(m))
}

```

![image-20230323222339761](C:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20230323222339761.png)

这段代码中对于map数组会报错

## make()

- 内置的make函数只能用于创建slice、map、chan
- 第二个参数指长度是必须的，第三个参数指容量是可选的。如果没有指定第三个参数，默认与第二个参数一致（即长度和容量相等）。

## go语言指针类型

## json 在序列化遇到管道/函数等无法被序列化的情况时，会发生 error 错误。 

## go声明数组的方法

```go
package main

import (
	"fmt"
)

var arr [2]int
var arr0 [5]int = [5]int{1, 2, 3}
var arr1 = [5]int{1, 2, 3, 4, 5}
var arr2 = [...]int{1, 2, 3, 4, 5, 6}
var str = [5]string{3: "hello world", 4: "tom"}

func main() {
	a := [3]int{1, 2}           // 未初始化元素值为 0。
	b := [...]int{1, 2, 3, 4}   // 通过初始化值确定数组长度。
	c := [5]int{2: 100, 4: 200} // 使用引号初始化元素。
	d := [...]struct {
		name string
		age  uint8
	}{
		{"user1", 10}, // 可省略元素类型。
		{"user2", 20}, // 别忘了最后一行的逗号。
	}
	fmt.Printf("%T", arr)
	fmt.Println()
	fmt.Println(arr0, arr1, arr2, str)
	fmt.Println(a, b, c, d)
}

```

