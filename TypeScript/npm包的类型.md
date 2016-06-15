# NPM包的类型
TypeScript编译器处理Node模块名时使用的是Node.js模块解析算法。 TypeScript也可以同时加载与npm包绑在一起的类型声明文件。 编译通过下面的规则来查找 "foo"模块的类型信息：
  1. 尝试加载相应代码包目录下package.json文件（node_modules/foo/）。如果存在，从"typings"字段里读取类型文件的路径。比如，在下面的package.json里，编译器会认为类型文件位于node_modules/foo/lib/foo.d.ts。
  ```
  {
    "name": "foo",
    "author": "Vandelay Industries",
    "version": "1.0.0",
    "main": "./lib/foo.js",
    "typings": "./lib/foo.d.ts"
  }
  ```
  2. 尝试加载在相应代码包目录下的名字为index.d.ts的文件（node_modules/foo/） - 这个文件应该包含了这个代码包的类型信息。
