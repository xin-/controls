# 导航

### 配置参数

    {
    	"currentSelect": 3,
    	"orient": "horizontal",
    	"series": [{
    		"key": "map",
    		"name": "创业地图"
    	}, {
    		"key": "layout",
    		"name": "投资格局"
    	}, {
    		"key": "company",
    		"name": "BAT"
    	}, {
    		"key": "person",
    		"name": "创业者"
    	}],
    	"itemGap": "24",
    	"a": {

    	},
    	"span": {
    		"normal": {
    			"fontSize": "24px",
    			"color": "#fff",
    			"background": "#606060"
    		},
    		"emphasis": {
    			"background": "#FF7C24"
    		}
    	}
    }

### 参数说明
  * currentSelect
    * 参数类型: number
    * 参数描述: 选中项在导航栏中的索引
  * orient
    * 参数类型: string
    * 参数值: [vertical | horizontal]
    * 参数描述: 表示导航控件排列方向是垂直排列还是水平排列
  * series
    * 参数类型: array
    * 参数描述: 参数值为一个数组，数组项为对象形式，对象属性key表示导航关键字，name表示显示在导航中的文字
  * itemGap
    * 参数类型: number
      * 参数描述: 控制导航中每项的距离
    * a
      * 参数类型: object(`css对象`， 驼峰命名)
      * 参数描述: 用于控制导航项宽高以及行高, 默认通过容器宽高以及itemGap计算所得, 也可以手动填写
    * span
      * 参数类型: object
      * 参数描述: 导航项的两种状态的样式，默认样式和选中样式
      * span.normal
        * 参数类型: object(`css对象`, 驼峰命名)
        * 参数描述: 导航项的默认样式
      * span.emphasis
        * 参数类型: object(`css对象`, 驼峰命名)
        * 参数描述: 导航项的选中样式

### 开放接口
  onChange
    * 接口描述: 点击导航项时触发
    * 参数: value
      * 参数类型：object
      * 参数描述: 返回选中的导航项
