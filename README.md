* [文章1](https://juntao.gitbooks.io/fun-with-underscore/content/fp/index.html)
* [文章2](https://www.gitbook.com/book/llh911001/mostly-adequate-guide-chinese/details)

#### 函数是一等公民
* 你可以像对待任何其他数据类型一样对待函数——把它们存在数组里，当作参数传递，赋值给变量。

#### 纯函数定义
* 纯函数是这样一种函数，即相同的输入，永远会得到相同的输出，而且没有任何可观察的副作用。
* 追求纯函数理由: 1.可缓存 2.可移植 3.可测试 4.合理

* 缓存函数demo
``` 
var memoize = function(f) {
  var cache = {};
  return function() {
    var arg = JSON.stringify(arguments);
    cache[arg] = cache[arg] || f.apply(f, arguments);
    return cache[arg];
  };
};
```

#### curry
* curry 的概念很简单：只传递给函数一部分参数来调用它，让它返回一个函数去处理剩下的参数。

