#  Node.js

- When we define a function, this function is added to **the global scope** via window object.
- So, it is possible that we have two files with the exact same name. When executing them, **window scope** will override it and which could be the problem of **the global scope**. 

```javascript
 var sayHello = function() {

 }

 window.sayHello();
```

- In order to build reliable and maintainable applications, we should avoid defining variable in global scope.

- We create small building blocks or modules where we define. Then, we create two variables and functions defined with exact same name in each modules. But, they don't override each other because they are encapsulated in each module. Now, at the core of Node, we have this concept called Module. 
- So, <u>every file in the Node application</u> is considered <u>a module</u>. The variable and functions defined in that function or module are <u>a scope to that file</u>. In Object-Oriented-Programming, terms **we say they are private scope**, they are not available outside that container, outside that module. 
-   If you want to use a variable or a function defined in a module, outside that module, <u>**you need to explicitly export it and make it public**</u>
- Every Node application has at least one file or one module which call the main module. So in this case app.js is our main module

```javascript
# app.js

console.log(module);
```

- <u>**We might think this module object may be global object, but actually it is not global because Every file is a module, and the variables and functions defined in that file are scoped in that module like private.**</u>

 

# Summary

Node.js 에서 one file 은 one module을 의미한다. 그렇기 때문에, 한 모듈에 있는 파일의 scope는 객체지향프로그래밍에서 사용하는 private의 범위를 가지고있다. 그래서 우리는 private의 범위를 가지고 있는 한 모듈을 사용하고 싶을때  module.exports 를 사용하거나 module.exports 객체를 call by reference로 바라보고 있는 exports를 사용해 module의 scope를 마치 public or global scope으로 만들어야한다.



