## let const   
**let**为 JavaScript 新增了块级作用域。    
**const**声明一个只读的常量（必须赋值）。一旦声明，常量的值就不能改变。    
let const声明的常量，不可重复声明。     

## 解构赋值    
```  
不完全解构       
let [x, y] = [1, 2, 3];      //x =1 ,y = 2    
let [a, [b], d] = [1, [2, 3], 4];       //a = 1,b = 2,d = 4    
```

```    
let [a,b]=[1];   //a=1,b=undefined     
如果解构赋值没有在结构上成功配对，未配对的变量默认值为undefined 
```

``` 
数组解构赋值
 let obj = {
  p: [
    'Hello',
    { y: 'World' }
  ]
};

let { p, p: [x, { y }] } = obj;
x // "Hello"
y // "World"
p // ["Hello", {y: "World"}]
```

## 正则扩展

## 字符串扩展   
**codePointAt**处理 4 个字节储存的字符，返回一个字符的码点。(从0开始返回第一个字符码点，如果第一个字符有四个字节，则codePointAt(1)返回后两个字节码点) 
```
let s = '𠮷a';
s.codePointAt(0)  // 134071    
s.codePointAt(1)  // 57271   
s.codePointAt(2)  // 97   
```
**String.fromCodePoint()** 码点返回对应字符    
```
String.fromCodePoint(0x20BB7)   // "𠮷"    
```
**includes()**：返回布尔值，表示是否找到了参数字符串。   
**startsWith()**：返回布尔值，表示参数字符串是否在原字符串的头部。   
**endsWith()**：返回布尔值，表示参数字符串是否在原字符串的尾部     