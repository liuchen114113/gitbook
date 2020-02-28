# src属性和href属性
#### href（hypertext reference）：
表示超文本引用，用来建立当前元素和文档间的链接。常用的有link，a 当CSS使用href引用，浏览器会识别该文档问CSS，并行下载，不会停止对当前文档的加载。

#### src（source）：
src指向的内容会嵌入到文档中当前标签的位置,常用的有img, script, iframe 浏览器解析到该元素时会停止对文档的渲染，直到该资源加载完成。这也是将script放底部而不是头部的原因。
