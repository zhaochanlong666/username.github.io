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
## 11、列举工作中常用的几个git命令?
    新增文件的命令：git add file或者git add .
    提交文件的命令：git commit –m或者git commit –a
    查看工作区状况：git status –s
    拉取合并远程分支的操作：git fetch/git merge或者git pull
    查看提交记录命令：git reflog
## 12、请描述什么是工作区、暂存区和本地仓库？
    git的工作区：在当前仓库中，新增，更改，删除文件这些动作，都发生在工作区里面。
    git的暂存区：英文叫stage, 或index。在版本库.git）目录下，有一个index文件。它实际上就是一个包含文件索引的目录树，像是一个虚拟的工作区。在这个虚拟工作区的目录树中，记录了文件名、文件的状态信息（时间戳、文件长度等），文件的内容并不存储其中，而是保存在Git对象库（.git/objects）中，文件索引建立了文件和对象库中对象实体之间的对应。如果当前仓库，有文件更新，并且使用git add 命令，那么这些更新就会出现在暂存区中。
    版本库：当前仓库下，如果没有任何的提交，那么版本库就是对应上次提交后的内容。
## 13、Echarts切换其他组件统计图时，出现卡顿问题如何解决
    原因：每一个图例在没有数据的时候它会创建一个定时器去渲染气泡，页面切换后，echarts图例是销毁了，但是这个echarts的实例还在内存当中，同时它的气泡渲染定时器还在运行。这就导致Echarts占用CPU高，导致浏览器卡顿，当数据量比较大时甚至浏览器崩溃

    解决方法：在mounted()方法和destroy()方法之间加一个beforeDestroy()方法释放该页面的chart资源，clear()方法则是清空图例数据，不影响图例的resize，而且能够释放内存，切换的时候就很顺畅了
## 14、什么时候应使用 “git stash”？
    git stash 命令把你未提交的修改（已暂存（staged）和未暂存的（unstaged））保存以供后续使用，以后就可以从工作副本中进行还原。
## 15、iframe 是什么？有什么缺点？
    定义：iframe 元素会创建包含另一个文档的内联框架
    提示：可以将提示文字放在标签之间，来提示某些不支持 iframe 的浏览器
    缺点：
    会阻塞主页面的 onload 事件
    搜索引擎无法解读这种页面，不利于 SEO
    iframe 和主页面共享连接池，而浏览器对相同区域有限制所以会影响性能。
## 16、addEventListener 参数
    addEventListener(event, function, useCapture)
    其中，event 指定事件名；function 指定要事件触发时执行的函数；useCapture 指定
    事件是否在捕获或冒泡阶段执行。
## 17、简述ajax 流程
    1客户端产生js的事件
    2创建XMLHttpRequest对象
    3对XMLHttpRequest进行配置
    4通过AJAX引擎发送异步请求
    5服务器端接收请求并且处理请求，返回html或者xml内容
    6.XML调用一个callback()处理响应回来的内容
    7页面局部刷新。
## 18、什么是Promise？我们用Promise来解决什么问题？
    Promise是承诺的意思，承诺它过一段时间会给你一个结果。
    Promise是一种解决异步操作编程的方案，相比回调函数和事件更合理和更强大。
    从语法上讲，promise是一个对象，从它可以获取异步操作的信息。
## 19、Promise有三种状态
    1、pending 初始状态也叫等待状态
    2、fulfiled成功转态
    3、rejected失败状态
## 20、什么时候使用git status
    git status命令用于显示工作目录和暂存区的状态。
    可以在任何时候使用 git status 来检查当前 Git 仓库的状态。它可以告诉你哪些文件已更改但尚未提交到仓库，哪些文件已暂存并准备提交，以及哪些文件尚未跟踪。这对于确保你提交的内容是正确和最新的非常有用。

    
