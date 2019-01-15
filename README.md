Here we go
==========
1. 由于运算是先转换成二进制之后再进行运算，所以会产生精度的问题
-------------------------------------------------------------
    ```javascript
      0.1+0.2
      0.30000000000000004
      0.2*6
      1.2000000000000002
    // 所以小数的运算可以使用固定位数之后再转换成浮点数的方法进行四舍五入
        parseFloat((0.2+0.1).toPrecision(12))
        0.3
        parseFloat((0.2*6).toPrecision(12))
        1.2
    ```
2. 根据数组对象中的某一个元素修改指定元素
---------------------------------------
    ```javascript
        var arr = [{answer:'',id:1},{answer:'',id:2},{answer:'',id:3}];
        arr.map(item=>{
            if(item.id === 2){
                item.answer = 'banana';
            }
            return item;
        })
    // 用到了js中的map()方法
    // map()方法返回一个新数组，数组中的元素为原始数组元素调用函数处理后的值,方法会以此按照原始数组的顺序处理元素;
    // map()方法的参数
    arr.map(functino(currentValue,index,arr){ })
    ```
3. 当前页跳转指定位置的几种方法
-----------------------------------------
    ```javascript
    // 根据ID获取需要跳转的元素，使用`scrollIntoView()`方法滚动到显示处
    let element = document.getElementById("id");
    element.scrollIntoView();
    // 这种方法会在url加上`#id`
    window.location.href = "#id";
    // 使用animate()会在滚动时加上动画的过度效果
    $("html,body").animate({scrollTop: $("#jys").offset().top}, 100);
    ```
4. 受控表单
---------------------------
    this.forceUpdate();//强制渲染
