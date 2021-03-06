# 位置参数
## [目录](./summary.md)
## 看看实质


- $0

- $1

- $2

- $3

- $4

- $5

- $6

- $7

- $8

- $9

看个例子
```javascript
node  index.js 3000
```
这句话什么意思呢？
这个意思?

意思也很简单，启动node服务，并且设置端口是3000

为什么可以设置端口和文件名字呢？

我们可以看出filename作为第一个参数

3000作为第二个参数

那么其实他们就是对应了`$1 $2`,如果你设置了第一个位置参数是文件名，第二个位置参数是端口的话，那么这个就可以实现了。

综上所述 `$1代表了第一个位置参数， $2代表了第二个参数，以此类推` 当然`$0`代表了这个命令（代表了命令的地址）

---

使用`$#`来获取到参数的个数。

## shift

每次 shift 命令执行的时候，变量 $2 的值会移动到变量 $1 中，变量 $3 的值会移动到变量 $2 中，依次类推。 变量 $# 的值也会相应的减1。


### 两个特殊的用法

- `$*`	展开成一个从1开始的位置参数列表。当它被用双引号引起来的时候，展开成一个由双引号引起来 的字符串，包含了所有的位置参数，每个位置参数由 shell 变量 IFS 的第一个字符（默认为一个空格）分隔开。
- `$@`	展开成一个从1开始的位置参数列表。当它被用双引号引起来的时候， 它把每一个位置参数展开成一个由双引号引起来的分开的字符串。
