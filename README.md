# myWebDevEx
Web应用练习


## FastAPI  使用PyCharm
配置FastAPI，打开main.py，打开运行的edit configuration，选择FastAPI项目，选择main.py，名字随意。   

*.http 文件为测试文件

查看WebAIP:  127.0.0.1:8000/docs   

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


