#服务配置信息详细文档

```
{
    "service": {
        "serviceInfo": {
            "cnName": "",
            "code": "TEXT@@@0241",
            "id": "20171207104649srlbJJydqqMNkX1kgXi4Ldaakjq0",
            "iscluster": "0",
            "name": "text",
            "recordTime": "2018-02-01 11:25:28",
            "settings": {
                "CACHE.EHCACHEDISK": "1",
                "CACHE.EHCACHEISDISK": "false",
                "CACHE.EHCACHEISTRUE": "false",
                "CACHE.EHCACHEMEMORY": "100",
                "CACHE.EHCACHETIME": "3600",
                "CLUSTERNODE": "",
                "CONFPYRAMID": "1",
                "LOGCONFIG": "",
                "SERVICEPROVIDERMAP.ABSTRACT": "",
                "SERVICEPROVIDERMAP.ADMINISTRATIVEAREA": "",
                "SERVICEPROVIDERMAP.CITY": "",
                "SERVICEPROVIDERMAP.COUNTRY": "",
                "SERVICEPROVIDERMAP.DELIVERYPOINT": "",
                "SERVICEPROVIDERMAP.ELECTRONICMAILADDRESS": "",
                "SERVICEPROVIDERMAP.FACSIMILE": "",
                "SERVICEPROVIDERMAP.INDIVIDUALNAME": "",
                "SERVICEPROVIDERMAP.KEYWORDS": "",
                "SERVICEPROVIDERMAP.ONLINERESOURCE": " ",
                "SERVICEPROVIDERMAP.POSITIONNAME": "",
                "SERVICEPROVIDERMAP.POSTALCODE": "",
                "SERVICEPROVIDERMAP.PROVIDERNAME": "",
                "SERVICEPROVIDERMAP.PROVIDERSITE": " ",
                "SERVICEPROVIDERMAP.TITLE": "",
                "SERVICEPROVIDERMAP.VOICE": "",
                "TEXT.TEXT.ENABLE": "true",
                "ADDR": "",
                "PATH": "C:\\Users\\shubangjie\\Desktop\\data\\wenzi_mysql.GMAPX",
                "PWD": "1",
                "REMOUTE": "1",
                "USR": "admin" 
            },
            "typeName": "TEXT"
        }
    },
    "port":"9010"
}
```

##服务基本配置
     

 >服务配置
 >service节点下serviceInfo配置服务基础信息，配置服务类型、名称、创建时间等。
<table>
    <tr>
        <td width="150px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
        <tr>
        <td width="100px">cnName</td> <td width="100px">可选</td> <td width="200px">服务别名</td>
    </tr>
        <tr>
        <td width="100px">code</td> <td width="100px">必填</td> <td width="200px">服务类型和编码（0239为文字服务，中间以@@@分隔，前面为服务名称TEXT）</td>
    </tr>
    <tr>
        <td width="100px">id</td> <td width="100px">必填</td> <td width="200px">服务ID</td>
    </tr>
        <tr>
        <td width="100px">iscluster</td> <td width="100px">必填</td> <td width="200px">是否是集群环境（默认值1不集群）</td>
    </tr>
        <tr>
        <td width="100px">name</td> <td width="100px">必填</td> <td width="200px">服务名称</td>
    </tr>
     <tr>
        <td width="100px">recordTime</td> <td width="100px">必填</td> <td width="200px">服务创建时间</td>
    </tr>
     <tr>
        <td width="100px">typeName</td> <td width="100px">必填</td> <td width="200px">服务类型</td>
    </tr>
     <tr>
        <td width="100px">settings</td> <td width="100px">必填</td> <td width="200px">服务扩展字段</td>
    </tr>
       <tr>
        <td width="100px">port</td> <td width="100px">必填</td> <td width="200px">服务容器端口号</td>
    </tr>
</table>


##服务扩展信息配置
>服务扩展信息，主要配置服务需要的扩展配置，如服务配置数据源、服务配置图层、服务协议参数等等。SERVICEPROVIDERMAP为服务提供者信息，可以根据情况填写，以下数据是所有服务公用配置。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="80px">描述</td>
    </tr>
        <tr>
        <td width="250px">CACHE.EHCACHEDISK</td> <td width="120px">必填</td> <td width="80px">默认值（1）</td>
    </tr>
       <tr>
        <td width="250px">CACHE.EHCACHEISDISK</td> <td width="120px">必填</td> <td width="20px">默认值（false）</td>
    </tr>
       <tr>
        <td width="250px">CACHE.EHCACHEISTRUE</td> <td width="120px">必填</td> <td width="20px">默认值（false）</td>
    </tr>
       <tr>
        <td width="250px">CACHE.EHCACHEMEMORY</td> <td width="120px">必填</td> <td width="20px">默认值（100）</td>
    </tr>
       <tr>
        <td width="250px">CACHE.EHCACHETIME</td> <td width="120px">必填</td> <td width="20px">默认值（3600）</td>
    </tr>
       <tr>
        <td width="250px">CONFPYRAMID</td> <td width="120px">必填</td> <td width="300px">默认值（1）</td>
    </tr>  
     <tr>
        <td width="250px">SERVICEPROVIDERMAP.ABSTRACT</td> <td width="120px">可选</td> <td width="300px">摘要</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.ADMINISTRATIVEAREA</td> <td width="120px">可选</td> <td width="300px">省份</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.CITY</td> <td width="120px">可选</td> <td width="300px">城市</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.COUNTRY</td> <td width="120px">可选</td> <td width="300px">国家</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.DELIVERYPOINT</td> <td width="120px">可选</td> <td width="300px">地址</td>
    </tr>
       <tr>
        <td width="250px">"SERVICEPROVIDERMAP.ELECTRONICMAILADDRESS</td> <td width="120px">可选</td> <td width="300px">邮箱</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.FACSIMILE</td> <td width="120px">可选</td> <td width="300px">传真</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.INDIVIDUALNAME</td> <td width="120px">可选</td> <td width="300px">联系人</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.KEYWORDS/td> <td width="120px">可选</td> <td width="300px">关键字</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.ONLINERESOURCE</td> <td width="120px">可选</td> <td width="300px">在线资源</td>
    </tr>
       <tr>
        <td width="250px">SERVICEPROVIDERMAP.POSITIONNAME</td> <td width="120px">可选</td> <td width="300px">职位</td>
    </tr>
      <tr>
        <td width="250px">SERVICEPROVIDERMAP.POSTALCODE</td> <td width="120px">可选</td> <td width="300px">邮编</td>
    </tr>
      <tr>
        <td width="250px">SERVICEPROVIDERMAP.PROVIDERNAME</td> <td width="120px">可选</td> <td width="300px">单位</td>
    </tr>
      <tr>
        <td width="250px">SERVICEPROVIDERMAP.PROVIDERSITE</td> <td width="120px">可选</td> <td width="300px">网站</td>
    </tr>
      <tr>
        <td width="250px">SERVICEPROVIDERMAP.TITLE</td> <td width="120px">可选</td> <td width="300px">标题</td>
    </tr>
        <tr>
        <td width="250px">SERVICEPROVIDERMAP.VOICE</td> <td width="120px">可选</td> <td width="300px">电话</td>
    </tr>
   </table>
   
   >TEXT服务特有配置信息,配置服务协议信息。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
     <tr>
        <td width="250px">TEXT.TEXT.ENABLE</td> <td width="120px">必填</td> <td width="100px">TEXT服务协议（默认值true）</td>
    </tr>              
      <tr>
        <td width="250px">ADDR</td> <td width="120px">必填</td> <td width="400px"></td>
    </tr>
    <tr>
        <td width="250px">PATH</td> <td width="120px">必填</td> <td width="400px">数据文件地址</td>
    </tr>
    <tr>
        <td width="250px">PWD</td> <td width="120px">必填</td> <td width="400px">密码</td>
    </tr>
    <tr>
        <td width="250px">REMOUTE</td> <td width="120px">必填</td> <td width="400px">默认值1</td>
    </tr>
      <tr>
        <td width="250px">USR</td> <td width="120px">必填</td> <td width="400px">用户名</td>
    </tr>
   </table>
