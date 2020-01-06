# awesome-vue-editor

## 安装
``` javascript
npm install awesome-vue-editor --save
```

## 使用

##### 全局引用

> 在Vue项目中，在main.js文件中加入以下代码
```
import VEditor from 'awesome-vue-editor'
Vue.user(VEditor)
```
> 在其它组件中就可以使用
```
  <v-editor v-model="content" 配置...></v-editor>
```

## 配置

### 属性配置

|属性|类型|默认值|是否必填项| 说明|
|:-----|:----:|:----|:-----:|:-----|
|v-model     |  String ||是|你组件中绑定的编辑器输入内容|
|height     |  Number \| String |"300px"|否|编辑器高度|
|width|Number \| String|100%|否|编辑器宽度|
|editabled|Boolean|true|否|编辑器是否可以编辑|
|countWords|Boolean|true|否|字数统计|
|autoHeightEnabled|Boolean|false|否|编辑器是否自动增加高度
|maxWord| Number |10000|否|编辑器最大字数
|options| Object |详见option项配置|否|编辑器所有配置

### options项配置

> 属性配置的优先级大于option里的配置内容

|属性|类型|默认值|说明|
|:-----|:----:|:----|:-----|
|toolbars   | Array    |  详见工具栏配置   | 可以是一维数组，也可以是2维数组，二维数组是给工具栏进行分组
|height     |  Number \| String |"300px"|编辑器高度|
|width|Number \| String|100%|编辑器宽度|
|editabled|Boolean|true|编辑器是否可以编辑|
|countWords|Boolean|true|字数统计|
|autoHeightEnabled|Boolean|false|编辑器是否自动增加高度
|fontName|Object|详见字体配置|
|fontsize|Object|详见字号配置|
|maxWord| Number |10000|编辑器最大字数

### 工具栏配置
> 可以是一维数组，也可以是2维数组，二维数组是给工具栏进行分组
```
    toolbars: [
      ['undo'],
      ['fontName', 'fontsize'],
      ['bold', 'italic', 'underline', 'strikeThrough'],
      ['justifyLeft', 'justifyCenter', 'justifyRight', 'justifyFull'],
      ['indent', 'outdent'],
      ['foreColor', 'backColor', 'removeFormat', 'lineHeight'],
      ['insertHorizontalRule', 'insertImage', 'insertHTML'],
      ['insertOrderedList', 'insertUnorderedList'],
      ['subscript', 'superscript'],
      ['createLink', 'unlink']
    ]
```
### 字体项配置
```
  fontName: {
    // 文本：值
    '宋体': 'SimSun',
    '黑体 ': 'SimHei',
    '微软雅黑': 'Microsoft YaHei',
    '仿宋 ': 'FangSong',
    '楷体': 'KaiTi',
    ......
  }
```

### 字号项配置
```
fontsize: {
    // 文本：值
    '二号': '22pt',
    '小二': '18pt',
    '三号': '16pt',
    '小三': '15pt',
    '四号': '14pt',
    '小四': '12pt',
    '五号': '10pt',
    ......
  }
```

### 代码仓库
See [github.com](https://github.com/jinying5012/Awesome-Vue-Editor).
