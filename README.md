### 布局问题
  * 圣杯布局
    ```
      //首先:浮动
      middle,left,right{
        float:left
      }
      middle{
        width:100%;
      }
      left,right{
        width:200px;
      }
      //然后:在一行显示
      left{
        margin-left:-100%;
      }
      right{
        margin-left:-200px;
      }
      //最后：解决遮盖
      box{
        padding:0 200px;
      }
      left,right{
        positon:relative;
      }
      left{
        left:-200px;
      }
      right{
        right:-200px;
      }
    ```
  * 淘宝双飞翼布局
    ```
    //最后：解决遮盖
    .middle-in{
       margin: 0 200px;
    }
    ```


> 比较
  * 圣杯布局和淘宝双飞翼布局只是解决遮盖的方式不同
    * 圣杯布局：box设置padding；left和right设置相对定位
    * 淘宝双飞翼布局：middle-in设置margin