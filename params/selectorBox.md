# 选择框

### 参数配置

    {
	    selected:[//已选择的选项索引号和value值
	    	{index:0,value:2015-10-4},
	    	{index:0,value:2015-10-4}
	    ],
	    mainType:"checkbox",// checkbox radio 单选/多选
	    // boxPosition:"bottom",//input和dropdownbox的上下位置---暂未实现
	    inputStyle:{//输入框样式
	        height:30,
	        background:"rgba(0,0,0,0)",
	        borderColor:"#333",
	        borderWidth:2,
	        color:"rgb(0,0,0)",
	        fontSize:"18px",
	        fontFamily:"微软雅黑",
	        fontStyle:"Regular"
	    },
	    selectBox:{//弹出框样式
	        background:"rgba(0,0,0,0)",
	        border:"1px solid rgba(0,0,0,0)",
	        borderColor:"rgba(0,0,0,0)",
	    },
	    series:{//弹出框中列表样式及数据
	        name:"year",
	        minHeight:20,
	        radioColor:'#333',       
	        itemStyle:{
	            normal:{
	                background:"rgba(0,0,0,0)",
	                border:"1px solid #333",
	                borderColor:"#333",
	                color:"rgb(0,0,0)",
	                fontSize:"25px",
	                fontFamily:"微软雅黑",
	                fontStyle:"Regular",
	                minHeight:"40px"
	            },
	            mouse:{

	            },
	            emphasis:{

	            }
	        },
	        data:[{
	            "name": "2015年10月4日",
	            "value": "2015-10-4"
	        }, {
	            "name": "2015年10月3日",
	            "value": "2015-10-3"
	        },{
	            "name": "2015年10月2日",
	            "value": "2015-10-2"
	        }]
	    }
	}

### 参数说明

  * selected
    * 参数类型: array
    * 参数说明: 选中的选项集合
  * mainType
    * 参数类型: string
    * 参数说明: 选项列表的类型，可选项 radio/checkbox
  * inputStyle
    * 参数类型: object
    * 参数说明: 显示选中项的input样式
  * selectBox
    * 参数类型: object
    * 参数说明: 弹出的选择列表容器的样式
  * series
    * 参数类型: object
    * 参数说明: 弹出的选择列表的样式和数据
  * series.radioColor
    * 参数类型: string //-color
    * 参数说明: radio 选中状态的颜色
  * series.itemStyle
    * 参数类型: object
    * 参数说明: 弹出列表中每行的样式
  * series.data
    * 参数类型: array
    * 参数说明: 需要灌入的数据//不可以有重复项，否则会报错




### 开放接口
 onChange
  * 接口描述: 接收选中项
  * 参数: arr
    * 参数类型: array
    * 参数描述: 当前选中项的集合
