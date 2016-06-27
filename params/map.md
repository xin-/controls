# 地图

### 提示框

data.tooltip

    {
      "show": true,
      "style": {
        "color": "#fff",
        "backgroundColor": "#000"
      },
      "position": [ 38, 50],
      "formatter": "<div></div>"
    }


##### show
  * 参数类型: boolean
  * 参数描述: 控制提示框显示隐藏

  ###### 备注
    >  show: false

##### style
  * 参数类型: obj
  * 参数描述: 控制提示框样式(驼峰命名法)

  ###### 备注
        {
          "color": "#fff",
          "backgroundColor": "#000"
        }

##### position
  * 参数类型: array
  * 参数描述: 提示框相对于鼠标位置向左上角移动的坐标

  ###### 备注
  > [38, 40]

##### formatter
  * 参数类型: [string | function]
  * 参数描述:
    * string: 需要插入到提示框中的字符串
    * function: 函数可接收一个参数，当鼠标悬浮在地图区域上时，该参数表示画该地图的json文件中该区域信息。当鼠标悬浮在markPoint上时，该参数表示画该markPoint的数据。此函数返回需要插入到提示框中的字符串。

    ###### 备注
      ```
        string
          <div>这是地图提示框</div>
      ```

      ```
        function
          参数 param
            悬浮在地图区域上参数样例:
               {
                "type": "Feature",
                "properties": {
                  "name": "北京"
                },
                "geometry": {
                  "type": "Polygon",
                  "coordinates": [

                  ]
                }
              }
            悬浮在markPoint上参数样例:
              {
                "area": "北京",
                "geoCoord": [111, 30],
                "value": 3
              }
          返回值样例
            var html = '<div class="diaisiTooltip" style=" background-color: #0b1747;  box-sizing: border-box;border: 4px solid #dededc; border-radius:15px; padding: 10px 20px; text-align:center">' + '<span style="margin-right: 20px; color: #ffffff;"> '+ d.area+ '</span><span style="color: #ffffff;">' + d.value + '</span></div>'
              return html
              返回的字符串可以是一串html代码, 因此可以随意拼接任意html, html样式也可以随意编写, 这段字符串可以访问param中的值

      ```
