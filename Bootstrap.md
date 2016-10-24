# Bootstrap

### 代码需要的连接 (模板)
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <meta name="viewport" content="width=device-width,initial-scale=1.0">
      <meta http-equiv="X-UA-Compatible" content="ie=edge">
      <title></title>
      <link rel="stylesheet" href="./bootstrap-3.3.7/css/bootstrap.min.css">
      <link rel="stylesheet" href="./font-awesome-4.6.3/css/font-awesome.min.css">
      <script type="text/javascript" src="./bootstrap-3.3.7/js/bootstrap.min.js"></script>
      <script type="text/javascript" src="./bootstrap-3.3.7/js/jquery-3.1.1.min.js"></script>
      </head>
      <body>
      </body>
      <html>
### 组件列表
###### 按钮组
###### 下路菜单按钮
###### 选项卡
###### 导航栏
###### 标签
###### 徽章
###### 页头与　hero　单元
###### 缩略图
###### 警示
###### 进度条
###### 对话框
###### 下拉菜单
###### 工具提示
###### Popvers
###### 手风琴
###### 旋转木马
###### Typeahead
#### 响应式
    //确保适当的回执和屏幕缩进　需添加　viewport 元素标签
    <meta name="viewport" content="width=device-width,initial-scale=1.0">
    //在移动设备上，　viewport 设置meta属性为　user-scalable=no 　可以禁用其缩进功能。
    <meta name="viewport" content="width=device-width,initial-scale=1, maximum-scale=1,user-scalable=no">
#### 布局容器
    <div class="container">
    内容
    </div>
###### .container-fluid 类似于１００％宽度，占据全部视口（viewport）的容器。
    <div class="container-fluid">
    ...
    </div>
#### 网格参数
    超小屏幕（手机）　：<768px     　类前缀　：　.col-xs-　列数
    小屏幕（平板）　　：>=768px    　类前缀　：　.col-xs-　列数
    中等屏幕（显示器）：>=992px    　类前缀　：　.col-xs-　列数
    大屏幕（大显示器）：>=1200px     类前缀　：　.col-xs-　列数
    例子：　<div class="col-md-1">１２列中的１列</div>
#### 流式布局容器  
###### .container 修改为 .container-fluid
    <div class="container-fluid">
        <div class="row">
        ...
        </div>
    </div>
#### 移动设备和桌面屏幕（手机，平板，桌面）
    <div class="container">
          <div class="row">
            <div class="col-xs-12 col-sm-6 col-md-8">手机，平板，桌面</div>
          </div>
     </div>
#### 设置列偏移
    .col-md-offser-４　　右偏移４个列
#### 设置排列
###### .col-md-push-*是向右浮动, .col-md-pull-*是向左浮动. *是代表浮动的列等份.(1~12)
    <div class="col-md-9 col-md-push-3">右浮动３列</div>
    <div class="col-md-3 col-md-push-9">左浮动９列</div>
#### 标题
    <h1>标题 <small>标题右变得标签　</small></h1>
#### 段落
    突显某个段落添加　class='lead'.
    <p class="lead">内容</p>
#### mark 标签
    <p>内容<mark>此处内容突出标记</mark></p>
#### del 和　s 标签
    <p>内容<del>删除此处内容</del></p>
    <p>内容<s>删除此处内容</s></p>
#### ins和u标签
    <p>内容<ins>此处内容加下划线</ins></p>
    <p>内容<u>此处内容加下划线</u></p>
#### strong和b标签  
    <p>内容<strong>此处内容加粗</strong></p>
    <p>内容<b>此处内容加粗</b></p>
#### em和i标签  
    <p>内容<em>此处内容为斜体</em></p>
    <p>内容<i>此处内容为斜体</i></p>
#### 文本对齐方式 
    <p class="text-left">左对齐</p>
    <p class="text-center">居中对齐</p>
    <p class="text-right">右对齐</p>
    <p class="text-justify">两端对齐</p>
    <p class="text-nowrap">默认</p>
#### 字母大小写
    <div class="text-lowercase">LOWercased text。将字母转换成小写</div>
    <div class="text-uppercase">Uppercased text。将字母转换成大写</div>
    <div class="text-capitalize">capitalized text。将首字母大写</div>
#### 缩略语      
    <abbr title="HTML5,CSS,JS三个技术的总称">HTML5</abbr>全栈开发可能包含ＷＥＢ前端与服务器后端课程，WEB前端课程包括：<em>ＨＴＭＬ５、ＣＳＳ、ＪＳ及响应式框架、移动化等内容；</em>服务器后端课程包括：<i>服务器环境搭建。Ｐｙｔｈ，ＪＳ后端框架，数据库知识等。</i></p>
#### 引用样式
    <blockquote>
        <p>可以使用“bockquote”标签来表示引用其他来源的内容</p>
    </blockquote>
##　列表
#### 无序列表
    <ul>
        <li>H5</li>
    </ul>
#### 有序列表
    <ul>
        <li>H5</li>
    </ul>
#### 定义列表
    <ul>
        <dt>H5</dt>
        <dd>C</dd>
        <dd>C</dd>
    </ul>
#### 内联列表
    <ul　class="list-inline">
        <li>H5</li>
    </ul>
#### 代码
###### 通过 code  标签包裹内联样式的代码片段。
    <code>&lt;section&gt;</code>
###### 通过  kbd  标签标记用户通过键盘输入的内容。  
    <kbd>cd</kbd>
###### 多行代码可以使用  pre  标签。为了正确的展示代码，注意将尖括号做转义处理。
    <pre>&lt;p&gt;...&lt;/p&gt</pre>
#### 表格
###### .table 类可以为其赋予基本的样式 — 少量的内补（padding）和水平方向的分隔线
    <div class="table">
        <thead>
          <tr>
            <th>姓名</th>
            <th>年龄</th>
            <th>职业</th>
          </tr>
        </thead>
     </div>
#### 条纹状表格 
###### 通过 .table-striped 类可以给 tbody 之内的每一行增加斑马条纹样式。 (IE8 不支持)
    <div class="table table-striped">
        <thead> 
          <tr>
            <th>姓名</th>
            <th>年龄</th>
            <th>职业</th>
          </tr>
        </thead>
     </div> 
#### 表格外框
###### 添加 .table-bordered 类为表格和其中的每个单元格增加边框
    <div class="table table-striped table-bordered">
        <thead> 
          <tr>
            <th>姓名</th>
            <th>年龄</th>
            <th>职业</th>
          </tr>
        </thead>
     </div>       
#### 高亮 
###### 通过添加 .table-hover 类可以让 tbody 中的每一行对鼠标悬停状态作出响应。
    <div class="table table-striped table-bordered table-hover">
        <thead> 
          <tr>
            <th>姓名</th>
            <th>年龄</th>
            <th>职业</th>
          </tr>
        </thead>
     </div>
#### 响应式表格
###### 将任何 .table 元素包裹在 .table-responsive 元素内，即可创建响应式表格，其会在小屏幕设备上（小于768px）水平滚动。当屏幕大于 768px 宽度时，底部的水平滚动条消失。
    <div class="table-responsive">
        <div class="table table-striped table-bordered">
            <thead> 
              <tr>
                <th>姓名</th>
                <th>年龄</th>
                <th>职业</th>
              </tr>
            </thead>
         </div>
     </div>
## 表单
###### 设置了 .form-control 类的 input、textarea 和select元素都将被默认设置宽度属性为 width: 100%;。 将 label 元素和前面提到的控件包裹在.form-group 中可以获得最好的排列。
    <div class="form-group">
          <label for="exampleInputEmail1">Email address</label>
          <input type="email" class="form-control" id="exampleInputEmaik1" placeholder="Enter email">
    </div>
## 内联表单
#### 为 form 元素添加 .form-inline 类可使其内容左对齐并且表现为 inline-block 级别的控件。只适用于视口viewport至少在 768px 宽度时（视口宽度再小的话就会使表单折叠）。
###需要手动设置宽度
###### 在 Bootstrap 中，输入框和单选/多选框控件默认被设置为 width: 100%; 宽度。在内联表单，我们将这些元素的宽度设置为 width: auto;，因此，多个控件可以排列在同一行。根据你的布局需求，可能需要一些额外的定制化组件
### 一定要添加 label 标签
    如果你没有为每个输入控件设置 label 标签，屏幕阅读器将无法正确识别。对于这些内联表单，你可以通过为 label 设置 .sr-only 类将其隐藏。                   <from class="form-inline" role="form">
            <div class="form-group">
              <label class="sr-only" for="exampleInputEmail2">Eamil address</label>
              <input type="email" class="form-control" id="exampleInputEmail2" placeholder="Enter email">
            </div>
            <div class="form-group">
              <div class="input-group">
                <div class="input-group-addon">@</div>
                <input type="email" class="form-cintrol" placeholder="Enter email">
              </div>
            </div>
            <div class="form-group">
              <label for="exampleInputPassword2" class="sr-only">Password</label>
              <input type="password" class="form-control" id="exampleInputPassword2" placeholder="Password">
            </div>
            <div class="checkbox">
              <label>
                <input type="checkbox">
              </label>
            </div>
            <button type="submit" class="btn btn-default">Sign in</button>
          </from>
