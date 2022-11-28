## myWebDevEx
Web应用练习

## 案例：Demo论文
1) FastAPI + Vue + Bootstrap  
UKP-SQuARE: An Online Platform for Question Answering Research   ACL22Demo
2) Flask/Python + Exrpress/NodeJS  + Bootstrap  
ParaQG: A System for Generating Questions and Answers from Paragraphs, EMNLP19  

## 案例：FastAPI/Python + Electron  
1) 启动FastAPI，
2) 启动Electron Fiddle，Show me，Web contents
3) 修改代码，去掉定时超时任务，改为
```JavaScript
const contents = webContents.getAllWebContents()[0]
const options = { extraHeaders: 'pragma: no-cache\n' }
contents.loadURL('http://127.0.0.1:8000', options)
```
4) HTTP命令，启动Electron Fiddle，Show me，Net
可以看到如何从WebAPI获得数据
5) 把BrowserWindow和Net结合，生成可视化结果。

## FastAPI  使用PyCharm
配置FastAPI，打开main.py，打开运行的edit configuration，选择FastAPI项目，选择main.py，名字随意。   

*.http 文件为测试文件

查看WebAPI:  127.0.0.1:8000/docs   

概念普及：https://blog.csdn.net/weixin_53906838/article/details/123185879  

web部分参考：Starlette  
数据部分参考：Pydantic  

Pydantic提供:  
ujson - 更快的JSON  
email_validator - 电子邮件的验证   

Starlette提供:  
requests - 如果你想要使用TestClient, 需要导入requests.  
aiofiles - 如果你想使用FileResponseor StaticFiles, 需要导入aiofiles.  
jinja2 - 如果你想使用默认的模板配置，需要导入jinjia2.  
python-multipart -如果要使用request.form（）支持表单“解析”，则为必需。  
itsdangerous -“SessionMiddleware”支持需要。   
pyyaml - 如果需要 SchemaGenerator 支持, 则为必要.  
graphene -如果需要 GraphQLApp 支持, 则为必要.   
ujson - 如果你想使用 UJSONResponse, 则为必要.  

###  其他
Hugo：根据Markdown，template等文件生成HTML静态页面。  
非常适合博客，文档等等网站的生成。Bootstrap的文档就是Hugo生成的。  

ESLint：  代码检查工具，用来检查你的代码是否符合指定的规范（例如： = 的前后必须有一个空格）。  

Masonry样式：对多个大小各异区域进行瀑布排列的方法。

less, sass, scss都是css预处理语言（也是对应的文件后缀名）   
开发时用预处理语言，在打包上线时，用webpack再配合loader工具给转成css（Cascading Style Sheets）给浏览器使用。
SASS（Syntactically Awesome StyleSheets）版本3.0之前的后缀名为.sass，而版本3.0之后的后缀名.scss

nuget .NET的包管理仓库，类似于Python的pip。

artifact：从源代码构建好的产品，类似于distribution，release，exe等。

Code scaffolding：Wizard

compiled and minified CSS and JS ：编译并压缩的CSS和JS

https://popper.js.org/：Positioning tooltips and popovers  控件的tooltips？


### 原型设计工具
Axure：  
Sketch：  
Figma：  
Dreamweaver：？？  



