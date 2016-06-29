# 分页

### 配置参数

    {
      curPage: 3,
      totalPages: 20,
      displayLinks: 7,
      showPre: true,
      firstText: '首页',
      lastText: '尾页',
      preText: '<<',
      nextText: '>>',
      firstStyle: {
        normal: {
          width: 50,
          height: '100%',
          marginLeft: 10,
          marginRight: 10,
          color: '#fff',
          backgroundColor: '#000',
          fontSize: 18,
          fontFamily: '微软雅黑'
        },
        emphasis: {

        }
      },
      preStyle: {
        normal: {
          width: 50,
          height: '100%',
          marginLeft: 10,
          marginRight: 10,
          color: '#fff',
          backgroundColor: '#000',
          fontSize: 18,
          fontFamily: '微软雅黑'
        },
        emphasis: {}
      },
      itemStyle: {
        normal: {
          marginLeft: 10,
          marginRight: 10,
          textAlign: 'center',
          color: '#fff',
          backgroundColor: '#000',
          fontSize: 18,
          fontFamily: '微软雅黑'
        },
        emphasis: {
          backgroundColor: '#ccc',
          color: '#000'
        }
      }
    }

### 参数说明
  * curPage
    * 参数类型: number
    * 参数描述: 表示当前选中第几页
  * totalPages
    * 参数类型: number
    * 参数描述: 总共有多少页
  * displayLinks
    * 参数类型: number
    * 参数描述: 可视区域可显示多少页
  * showPre
    * 参数类型: boolean
    * 参数描述: 是否显示上一页，下一页按钮
  * firstText; lastText; preText; nextText
    * 参数类型: string
    * 参数描述: 首页, 尾页, 上页, 下页功能按钮显示文本
  * firstStyle
    * 参数类型: object
    * firstStyle.normal
      * 参数类型: object(`css对象`, 采用驼峰命名)
      * 参数描述: 首页, 尾页按钮默认样式
    * firstStyle.emphasis
    * 参数类型: object(`css对象`, 采用驼峰命名)
    * 参数描述: 首页, 尾页按钮鼠标悬浮样式
  * preStyle
    * 参数类型以及值同firstStyle
    * 参数描述： 控制上一页, 下一页按钮的样式
  * itemStyle
    * 参数类型: object
      * itemStyle.normal
        * 参数类型: object(`css对象`, 采用驼峰命名)
        * 参数描述: 显示页数按钮的默认样式
      * itemStyle.emphasis
        * 参数类型: object(`css对象`, 采用驼峰命名)
        * 参数描述: 选中页的样式

#### 备注
    > firstStyle和preStyle需要设置宽高，高通常设为100%，控件会根据这两个的宽来计算出显示页码数的按钮的宽度

### 开放接口
 onChange
  * 接口描述: 切换选中页时触发
  * 参数: value
    * 参数类型: number
    * 参数描述: 当前选中的第几页
