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

##### style
  * 参数类型: obj
  * 参数描述: 控制提示框样式

##### position
  * 参数类型: array
  * 参数描述: 提示框相对于鼠标位置向左上角移动的坐标

##### formatter
  * 参数类型: [string | function]
  * 参数描述:
    * string: 需要插入到提示框中的字符串
    * function: 函数可接收一个参数，当鼠标悬浮在地图区域上时，该参数表示画该地图的json文件中该区域信息。当鼠标悬浮在markPoint上时，该参数表示画该markPoint的数据。此函数返回需要插入到提示框中的字符串。
