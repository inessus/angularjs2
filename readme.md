# helloworld 三步走
1. 引入Angular2预订类型
```javascript
import {Component,View,bootstrap} from "angular2/angular2";
```
import是ES6的关键字，用来从模块中引入类型定义。在这里，我们从angular2模块库中引入了三个类型： Component类、View类和bootstrap函数。
2. 实现一个Angular2组件
实现一个Angular2组件也很简单，定义一个类，然后给这个类添加注解：
```javasciript
[@Component](/user/Component)({selector:"ez-app"})
[@View](/user/View)({template:"<h1>Hello,Angular2</h1>"})
class EzApp{}
```
class也是ES6的关键字，用来定义一个类。@Component和@View都是给类EzApp附加的元信息， 被称为注解/Annotation。
@Component最重要的作用是通过selector属性（值为CSS选择符），指定这个组件渲染到哪个DOM对象上。 @View最重要的作用是通过template属性，指定渲染的模板。
3. 渲染组件到DOM
将组件渲染到DOM上，需要使用自举/bootstrap函数：
```javaxript
bootstrap(EzApp);
```
这个函数的作用就是通知Angular2框架将EzApp组件渲染到DOM树上。
简单吗？我知道你一定还有疑问，别着急，我们慢慢把缺失的知识点补上！
