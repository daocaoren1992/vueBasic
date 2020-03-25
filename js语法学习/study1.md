1. js中const,var,let区别 https://www.cnblogs.com/ksl666/p/5944718.html
    1.const定义的变量不可以修改，而且必须初始化。
    
    1 const b = 2;//正确
    2 // const b;//错误，必须初始化 
    3 console.log('函数外const定义b：' + b);//有输出值
    4 // b = 5;
    5 // console.log('函数外修改const定义b：' + b);//无法输出 
    2.var定义的变量可以修改，如果不初始化会输出undefined，不会报错。
    
    1 var a = 1;
    2 // var a;//不会报错
    3 console.log('函数外var定义a：' + a);//可以输出a=1
    4 function change(){
    5 a = 4;
    6 console.log('函数内var定义a：' + a);//可以输出a=4
    7 } 
    8 change();
    9 console.log('函数调用后var定义a为函数内部修改值：' + a);//可以输出a=4
    
    3.let是块级作用域，函数内部使用let定义后，对函数外部无影响。
    
    1 let c = 3;
    2 console.log('函数外let定义c：' + c);//输出c=3
    3 function change(){
    4 let c = 6;
    5 console.log('函数内let定义c：' + c);//输出c=6
    6 } 
    7 change();
    8 console.log('函数调用后let定义c不受函数内部定义影响：' + c);//输出c=3


2. array相关
filter 06目录
sort   06目录

3. computed计算属性
https://segmentfault.com/a/1190000010408657

4. 快速构建对象
 let name = "tome";
 let age = 29;
 const comment = {name, age};
 
 5. reduce
 var todos=  [
   {title:'吃饭',complete:true},
   {title:'睡觉',complete:true},
   {title:'coding',complete:false}
 ];
 var cnt = todos.reduce((pre,current) => pre += (current.complete?1:0),0)
 
 6.unshift() 方法可向数组的开头添加一个或更多元素，并返回新的长度
 var arr = new Array()
 arr[0] = "George"
 arr[1] = "John"
 arr[2] = "Thomas"
 arr.unshift("William")
 
 7. import import default的区别
 https://blog.51cto.com/11871779/2348288
 
 8. 
 let rawObject = [
   {
   name : "zhangsan",
   age : 29,
   hobby: "basketball"
   },
   {
     name : "lisi",
     age : 30,
     hobby: "pingpang"
   }
 ]
 
9.

 const personArray = rawObject.map(item=>({
   myName : item.name,
   myAge : item.age
 }))