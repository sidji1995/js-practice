###01圆的周长和面积
```
return 2 * Math.PI * r;
```
/*  return 后接方法 */
###02求两个数的最大值
>三元运算符
return a > b ? a : b;
###03求一组数中的最大值和最小值  
>一组数中的元素比较,变量i只需 <arr.length - 1即可. 
- 1.元素个数等于arr.length
i+1做为最后一个比较对象,i+1<length,
i<length - 1;
- 2. 声明一个新变量,与后边元素进行比较.
###04反转数组
- 1.unshift方法:
   创建新数组
   (声明新变量newArr可放在全局变量中,创建的变量都hi作为window对象的属性保存)
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
