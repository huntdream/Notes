# $(document).ready()
页面在文档“准备”(ready)之前是不能被操作(manipulate)的。jQuery为你检测文档的准备状态。在`$(document).ready()`中的代码将只会在文档对象模型(DOM)为JavaScript代码执行准备就绪之后运行。在`$( window ).on( "load", function() { ... })`中的代码将会在整个页面，不仅仅是DOM，完全加载之后运行。
```
// A $(document).ready() block.
$(document).ready(function(){
	console.log("Ready!");
});
```
熟练的开发者有时会用`$()`简写来替代`$(document).ready()`.如果你写的代码可能会给不熟练的jQuery使用者看,那么最好使用完整形式。
```
// Shorthand for $(document).ready()
$(function(){
	console.log("Ready!");
});
```
你也可以传递一个命名函数而非一个匿名函数给`$(document).ready()`
```
// Passing a named function instead of an anoymous function

function readyFn(jQuery) {
	// Code to run when the document is ready.
}

$(document).ready(readyFn);
// or:
$(window).on("load", readyFn);
```
下面的例子展示`$(document).ready()`和`$(window).on("load")的实例。代码试图在一个iframe中加载一个网站URL并且检查两个事件
```
<html>
<head>
    <script src="https://code.jquery.com/jquery-1.9.1.min.js"></script>
    <script>
    $( document ).ready(function() {
        console.log( "document loaded" );
    });
 
    $( window ).on( "load", function() {
        console.log( "window loaded" );
    });
    </script>
</head>
<body>
    <iframe src="http://techcrunch.com"></iframe>
</body>
</html>
```