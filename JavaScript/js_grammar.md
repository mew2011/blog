# JS Grammar
## export default
```
// 将一个对象、函数、类或值作为模块的默认导出，供其他文件引入使用
// 导出对象
export default { a: 1 };
// 导出函数
export default function() {};
// 导出类
export default class {};
// 导出原始值
export default 42;
```

|特性	|export default|命名导出 (export)|
|:--|--|--|
|每个模块的数量|只能有一个|可以有多个|
|导出示例|export default obj	|export const obj = {}|
|导入语法|import x from './file.js'	|import { x } from './file.js'|
|导入限制|不能加花括号|	必须加花括号|
|导入命名|任意变量名（自定义）	|固定名|

```
// module.js
export const PI = 3.14;
export function square(x) { return x * x; }

// main.js
import { PI, square } from './module.js'; // 名称必须匹配
console.log(PI); // 3.14
square(2); // 4
```

## constructor()
```
// JS使用类似JAVA OOP方式编程
class Polygon {
  constructor() {
    this.name = "Polygon";
  }
}
// new 实例时会执行constructor方法
const poly1 = new Polygon();
console.log(poly1.name);
```
