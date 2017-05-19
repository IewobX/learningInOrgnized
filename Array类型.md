##Array类型
###arguements对象：
	与数组类似，但不是Array实例，用来储存函数参数。 (修改arguments会修改参数值)
<pre>
function howManyArgs()
	alert(arguments.length);
｝
howManyArgs("string",45);                  //2
howManyArgs();                             //0
howManyArgs(12);                           //1
</pre>
###instanceof(操作符)：
	person instanceof Object                   //变量person是Object么？
###isArray():
	为确定某个值是否是数组
<pre>
if(isArray(value)){
	//执行操作
}
</pre>
###join()：
	以不用分隔符构建字符串
<pre>
var colors = ["red","green","blue"];
alert(colors.join("||"));                   //red||green||blue
</pre>
###push():
	从数组后面推入元素
###pop():
	从数组后面删除元素
###shift():
	从数组前面插入元素
###unshift():
	从数组前面删除元素
###split():
	将数组转化成字符串
###splice():
	插入，删除，替换元素
###slice():
	基于当前数组中的一个或多个项创建一个新数组
###concat():
	连接数组
###indexOf():
	从前到后查找数组元素，可以传入第二个参数，表示从那个位置开始向后查找
###lastindesOf():
	从后往前查找，传入参数同上
###every():
	对数组每一项运行给定函数，每一项都true返回true
###filter():
	对数组每一项运行给定函数，返回true项所组成的数组
###forEach():
	对数组每一项运行给定函数,无返回
###map():
	对数组每一项运行给定函数,返回每次调用结果组成的数组
###some():
	对数组每一项运行给定函数，有一项true返回true
###reduce():
###reduceRight():