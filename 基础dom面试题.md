## 1、什么是Promise？我们用Promise来解决什么问题？
    Promise是承诺的意思，承诺它过一段时间会给你一个结果。
    Promise是一种解决异步操作编程的方案，相比回调函数和事件更合理和更强大。
    从语法上讲，promise是一个对象，从它可以获取异步操作的信息。
## 2、Promise有三种状态
    1、pending 初始状态也叫等待状态
    2、fulfiled成功转态
    3、rejected失败状态
## 3、$(document).ready() 是个什么函数？为什么要用它？
    ready() 函数用于在文档进入ready状态时执行代码。当DOM 完全加载（例如HTML被完全解析DOM树构建完成时），jQuery允许你执行码。使用$(document).ready()的最大好处在于它适用于所有浏览器，jQuery帮你解决了跨浏览器的难题。需要进一步了解的用户可以击 answer链接查看详细讨论。
## 4、$(this) 和 this 关键字在 jQuery 中有何不同？
    这对于很多 jQuery 初学者来说是一个棘手的问题，其实是个简单的问题。$(this) 返回一个 jQuery 对象，你可以对它调用多个jQuery 方法，比如用 text() 获取文本，用val() 获取值等等。而 this 代表当前元素，它是 JavaScript 关键词中的一个，表示上文中的当前 DOM 元素。你不能对它调用 jQuery 方法，直到它被 $() 函数包裹，例如 $(this)。
## 5、你知道那些事件修饰符
    .stop阻止事件冒泡
    .once只执行一次，一次性事件
    .self阻止事件冒泡和事件捕获
    .captrue事件捕获阶段触发
    .prevent阻止浏览器默认行为
    .native 触发原生事件
## 6、XML与JSON的区别？
    1) 数据体积方面。JSON相对于XML来讲，数据的体积小，传递的速度更快些。
    2) 数据交互方面。JSON与JavaScript的交互更加方便，更容易解析处理，更好的数据交互。
    3) 数据描述方面。JSON对数据的描述性比XML较差。
    4) 传输速度方面。JSON的速度要远远快于XML。
## 7、Promise有几种状态
    有三种状态：
    pending（进行中）
    fulfilled（已成功）
    rejected（已失败）
    Promise 是es6引入的异步编程解决方案
    可以链式调用，解决回调地狱的问题
## 8、什么是宏任务，什么是微任务
    宏任务和微任务都是异步任务在同步任务队列之后
    而宏任务一般是:包括整体代码script, setTimeout, setInterval、 setlmmediate（node 独有）。
    微任务:原生Promise(有些实现的promise将then方法放到了宏任务中)、
    process.nextTick、Object记住就行了new.promise是宏任务。
    执行顺序
    微观任务先于宏观任务  
## 9、var let 和 const三者之间的区别
    const：必须初始化，而且不能更改
    var : 定义的变量可以修改，如果不初始化会输出undefined，不会报错
    let : 块级作用域，函数内部使用let定义后，对函数外部无影响。
    var可以重复申明，let不可以 
## 10、Promise 中reject 和 catch 处理上有什么区别（三个状态）
    reject是用来抛出异常，catch 是用来处理异常
    reject是Promise的方法，而catch 是Promise 实例的方法
    reject后的东西，一定会进入then中的第二个回调，如果then中没有写第二个回调，则进入catch
    网络异常(比如断网)，会直接进入catch而不会进入then的第二个回调