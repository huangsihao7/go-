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