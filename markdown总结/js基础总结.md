###01圆的周长和面积
```
return 2 * Math.PI * r;
```
/*  return 后直接接方法梭哈 */
###02求两个数的最大值
>三元运算符
return a > b ? a : b;
###03求一组数中的最大值和最小值  
>一组数中的元素比较,变量i只需 <arr.length - 1即可. 
i+1做为最后一个比较对象,i+1<length,
i<length - 1;
声明一个新变量,与后边元素进行比较.
###04反转数组
- 1.unshift方法:
   创建新数组
   (声明新变量newArr可放在全局变量中,创建的变量都作为window对象的属性保存)
- 2.push方法
   新建一个空数组
    令i = arr.length-1从后遍历数组,push最后一个元素到新数组的第一个元素.
```
  for(i =arr.length - 1; i>=0;i--){
                var newArr = [];
                newArr.push(arr[i]);
            }
```
- 3.直接原数组交换
>交换次数为数组长度的一半
最中间的元素自己和自己交换
```
 for(var i =0; i < arr.length/2; i++){
            var temp = arr[i];
            arr[i] = arr[arr.length-1-i]
            arr[arr.length-1-i] = temp;
```
###05豆瓣
- 1.将对象movies.subjects取出
- 2.for遍历电影名title
- 3.声明新dirStr
   for遍历导演名(1人/2人)
- 4.subjects数组中存放了20个对象,每个对象中又存放了(title:电影名)属性-值对,对象
```
 var dirStr = '';
 for(var j = 0; j < directorsArr.length; j++){
 dirStr = dirStr + directorsArr[j].name + '/'
 }
```
- 4.subStr(0,.length -1)去掉/
###06对象
var obj = {
   key : value   键(属性)值对
}
函数属性称为对象的方法

####一:创建对象的三种方式
- 1.var obj = new Object();
- 2.字面量:var obj2 = {}
- 3.自定义构造函数:
```
function Person() {
            this.name = '张三';
            this.age = 19;  
            this.child = {
                name: '小明'
            }
             this.say = function () {
                alert(this.name)
            }
}
var zs = new Person();
```
- 3.1 this是一个指针 指向在调用前不确定,this指向new出来的实例对象:zs;
- 3.2 new:
   构造函数new创建了空对象 zs;
   将this指向zs
- 3.3 zs.say();     /*alert(this.name)指向调用者zs*/
- 3.4 person();     不通过new实例对象,this指向window
####二:对象的遍历
```
for (var key in movieJson) {
   console.log(movieJson[key]);
   }
```
>属性名是变量,需要"对象[变量名]"来获取属性

###07数组的高级方法(驼峰命名)
####1一.sort:排序
```
arr.sort(function (a,b){
   return a - b;
   if(a.age ===b.age){
      return a.weight - b.weight;     /*二次比较*/
   }
})
console.log(arr)
```
   1.1带参:必为函数(匿名函数),计算a-b,根据正负决定大小排序
   1.2无参:
```
   var months = ['March', 'Jan', 'Feb', 'Dec'];
   months.sort();
```
####二.toString:数组转变字符串
####三.reverse:翻转数组
####四.indexOf/lastIndexOf:查找元素并返回下标
   4.1找到停止,没有找到返回-1;
   >判断指定元素在不在数组中
####五.slice:获取新数组
   >获取参数:[开始值(0),end(1)),前开后闭
   >start从0开始,end从1开始,返回一个新数组,包含start不包含end.
   >arr.slice(0)复制数组
###六.splice()删除//替换
   6.1获取参数(开始值(0),删除/替换个数,替换值)不写替换项目(第三个)就是删除;
   **删除下标为i的元素splice(i,1)**
   6.2清空数组:arr=[];
####七.concat:合并数组 
####八.unshift/push:从前/后添加一个元素
   var temp = arr.push('张三');
   >都会改变原数组,返回值是新数组的长度.
####九.shift/pop:前/后删除一个元素
####十.split:数组转字符串(分隔符';'/字符长度)
   arr.split(';')
####十一.join:字符串转数组 
   arr.join('-')
   >也会改变原数组,返回值是删除元素.
###08string的高级方法
####一.charAt:获取字符(单个)
   charCodeAt(返回指定位置字符的Unicode编码);
####二.indexof/lastIndexOf查找元素并返回下标
####三.concat:合并字符
####四.slice:提取字符串的某部分[开始下标,结束下标) 
   >获取参数:[开始值(0),end(1)),前开后闭
   >start从0开始,end从1开始,返回一个新数组,包含start不包含end.
   >arr.slice(0)复制字符串
####五.substr:提取字符串[开始下标(0),取的个数]
   start与slice一样都是从零开始,结束为**取的字符个数,能取到**
####六.toUpperCase/toLowerCase:大/小写;
####七.toFixed:保留小数


   






