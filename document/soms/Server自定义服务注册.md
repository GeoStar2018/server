运维支持自定义服务按照固定模板进行注册，注册成功后被运维管理。自定义注册服务已zip形式上传注册，目录结构如下DQS.zip为服务包，格式同war包格式一样。

1.1 自定义服务结构
下图为注册服务zip包结构：主要分为三部分CustomConfig主要配置运维发布服务时加载自定义服务配置界面，用于配置服务基础信息。DQS.zip为服务包实体，注册服务会把服务包加载到运维中进行管理，用于服务发布。Config.txt配置服务名称，服务名称和服务zip包名一样。

![image](/uploads/8a1001422d49b05e9c7b6416291288ed/image.png)

1.1.1 服务配置界面和lib包
CustomConfig目录配置服务配置界面和协议界面
目录结构如下

![image](/uploads/95a0d78ecfae1ea931d90101379de29e/image.png)

服务同名目录DQS为jsp界面

![image](/uploads/2f6e2e81aef71d58869821e116e9ca89/image.png)

数据信息配置界面必写在已服务名命名的jsp中（DQS.jsp），协议配置界面写在DQS.js中，如无协议配置可以不用写。
lib目录存放jar包扩展jar包放在lib目录下注册服务时会加载到运维中。在配置界面中使用运维无法提供的能力，只能在jsp中引入自己需要的jar来实现功能。

1.1.2 服务名称配置
Config.txt文件中配置服务名称和模板包名称，两着名称和ZIP包名称统一。
`
{
  "serviceName": "DQS",
  "serTempleteName":"DQS"
}
`
serviceName为服务名称：DQS，serTempleteName为服务模板名称：DQS

1.1.3 服务模板包
DQS.zip服务包中添加以下文件，配置服务请求接口和数据源等信息。服务请求接口配置在使用服务模板框架开发服务时可以实现运维监控功能，没有则无服监控信息。注册使用GeoGlobe服务模板框架开发，可以使用服务扩展功能HTTP头设置等，不使用服务模板框架也能做服务模板包发布服务。

![image](/uploads/13ac8dbbde675a8dabc5dd0f89120299/image.png)

WEB-INF/geoglobe/signup.txt

`{
    "name": "DQS",
    "shortName": "DQS",
    "cfgMode": [
        "CUSTOM" 
    ],
    "dataSource": [
        "ORACLE_SOURCE",
        "DAMENG_SOURCE",
        "MYSQL_SOURCE"
    ],
    "protocol": [
        {
            "name": "DQS",
            "data": [
                "",
                ""
            ],
            "operation": [
                "GetCapabilities",
                "GetDataSetList",
                "DescribeDataSet",
                "Query"
            ]
        }
],
    "cachable": false,
    "version": "3.1.0"
}`

| 参数 | 说明 | 
| ------ | ------ |
| name | 服务名称 | 
| shortName | 协议名称 | 
| cfgMode   | 配置模型（扩展服务CUSTOM） | 
| dataSource| 服务支持数据源 | 
| protocol  | 服务支持请求接口 | 
| cachable  | 服是否支持缓存（默认false） | 
| version   | 版本 | 

1.2 运维服务注册
在运维管理系统中系统管理模块，选择服务类型管理，点击新增按钮添加注册服务。
![image](/uploads/1c1ca8c38d00a7c51d2a409613cc1bf1/image.png)

点击上传服务模板包，选择上传的服务注册ZIP包。
![image](/uploads/e6ca2a58d412d33e9f47464a4b96f82f/image.png)

服务注册成功，可以通过服务发布界面发布注册服务。
![image](/uploads/61ac0c0dc297cc44558fab1ba65a817c/image.png)