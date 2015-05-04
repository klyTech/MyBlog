## 我感受到的函数式编程functional programming

不记得从什么时候函数式编程fp开始在业界热起来。fp也不是什么新概念，在流行之前的几十年前就有了。但是一直比较小众，我在学校里学专业课程的时候，也没接触过。有些概念在实践中不知不觉地在使用，但是不知道这些做法就是fp提倡的概念。譬如，递归就是fp常会用到的做法。


### Guava的引导
几年前，在偶然的情况下，用了google的Guava库。由于这个Guava库确实好用，所以它成为我工具库里的必备选项。我成了Guava重度用户。那时候，我还没关注fp。直到后来看到fp的文章，我才意识到自己在使用Guava的过程中，fp的观念潜移默化地植入我的编程思路里。

### fp的实用性
纯fp的语言，其实不符合人的直观思维。譬如，有人说递归是很直观的算法。我不得不说，递归是比较高级的算法，是有点反直觉的。循环才是正常人类的思维。递归的代码会比较简洁，但是代码简洁不代表思路简单。
举个求整型数组之和的例子，用循环做：
```java
int sum = 0;
for(Integer i : list)
  sum += i;
```
就这么简单。
但是fp里的递归可不是这么做，它要做个函数：
```java
int sum(List<Integer> list) {
  if(list.isEmpty()) {
    return 0;
  }
  return list.get(0) + sum(list.subList(1));
}
```

Java8的功能和Guava是有重叠的，Java8从语言级别更好地支持了fp。

### functional programming VS object-oriented
虽说我觉得fp特别cool。编程中有一种特别的乐趣，但是我还是认为OO的影响大绝对大于fp。

