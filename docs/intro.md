# TypeScript 语言简介

## 概述

TypeScript（简称 TS）是微软公司开发的一种基于 JavaScript （简称 JS）语言的编程语言。

它的目的并不是创造一种全新语言，而是增强 JavaScript 的功能，使其更适合多人合作的企业级项目。

TypeScript 可以看成是 JavaScript 的超集（superset），即它继承了后者的全部语法，所有 JavaScript 脚本都可以当作 TypeScript 脚本（但是可能会报错），此外它再增加了一些自己的语法。

TypeScript 对 JavaScript 添加的最主要部分，就是一个独立的类型系统。

## 类型的概念

类型（type）指的是一组具有相同特征的值。如果两个值具有某种共同的特征，就可以说，它们属于同一种类型。

举例来说，`123`和`456`这两个值，共同特征是都能进行数值运算，所以都属于“数值”（number）这个类型。

一旦确定某个值的类型，就意味着，这个值具有该类型的所有特征，可以进行该类型的所有运算。凡是适用该类型的地方，都可以使用这个值；凡是不适用该类型的地方，使用这个值都会报错。

可以这样理解，**类型是人为添加的一种编程约束和用法提示。** 主要目的是在软件开发过程中，为编译器和开发工具提供更多的验证和帮助，帮助提高代码质量，减少错误。

下面是一段简单的 TypeScript 代码，演示一下类型系统的作用。

```typescript
function addOne(n:number) {
  return n + 1;
}
```

上面示例中，函数`addOne()`有一个参数`n`，类型为数值（number），表示这个位置只能使用数值，传入其他类型的值就会报错。

```typescript
addOne('hello') // 报错
```

上面示例中，函数`addOne()`传入了一个字符串`hello`，TypeScript 发现类型不对，就报错了，指出这个位置只能传入数值，不能传入字符串。

JavaScript 语言就没有这个功能，不会检查类型对不对。开发阶段很可能发现不了这个问题，代码也许就会原样发布，导致用户在使用时遇到错误。

作为比较，TypeScript 是在开发阶段报错，这样有利于提早发现错误，避免使用时报错。另一方面，函数定义里面加入类型，具有提示作用，可以告诉开发者这个函数怎么用。


下面简要介绍 TypeScript 的发展历史。

2012年，微软公司宣布推出 TypeScript 语言，设计者是著名的编程语言设计大师 Anders Hejlsberg，他也是 C# 和 .Net 的设计师。

微软推出这门语言的主要目的，是让 JavaScript 程序员可以参与 Windows 8 应用程序的开发。

当时，Windows 8 即将发布，它的应用程序开发除了使用 C# 和 Visual Basic，还可以使用 HTML + JavaScript。微软希望，TypeScript 既能让 JavaScript 程序员快速上手，也能让 .Net 程序员感到熟悉。

这就是说，TypeScript 的最初动机是减少 .Net 程序员的转移和学习成本。所以，它的很多语法概念跟 .Net 很类似。

另外，TypeScript 是一个开源项目，接受社区的参与，核心的编译器采用 Apache 2.0 许可证。微软希望通过这种做法，迅速提高这门语言在社区的接受度。

2013年，微软的 Visual Studio 2013 开始内置支持 TypeScript 语言。

2014年，TypeScript 1.0 版本发布。同年，代码仓库搬到了 GitHub。

2016年，TypeScript 2.0 版本发布，引入了很多重大的语法功能。

2018年，TypeScript 3.0 版本发布。

2020年，TypeScript 4.0 版本发布。

2023年，TypeScript 5.0 版本发布。

## 如何学习

学习 TypeScript，必须先了解 JavaScript 的语法。因为真正的实际功能都是 JavaScript 引擎完成的，TypeScript 只是添加了一个类型系统。

本书假定读者已经了解 JavaScript 语言，就不再介绍它的语法了，只介绍 TypeScript 引入的新语法，主要是类型系统。

如果你对 JavaScript 还不熟悉，建议先阅读[《JavaScript 教程》](https://wangdoc.com/javascript)和[《ES6 教程》](https://wangdoc.com/es6)，再来阅读本书。

