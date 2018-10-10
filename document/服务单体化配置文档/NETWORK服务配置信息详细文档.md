#NETWORK服务配置信息详细文档

```
{
  "service":{
    "serviceInfo":{
      "id":"",
      "cnName":"",
      "name":"NetWork",
      "code":"NETWORK@@@0243",
      "typeName":"NETWORK",
      "recordTime":"2018-03-07 11:25:28",
      "iscluster":1,
      "dataItem": [
                {
                    "dataSourceType": "NetworkSource",
                    "dataType": "NETWORK",
                    "dbcpId": "20170922140121ZUWp4kdrTjO8XPItjHQLgeK1231",
                    "layerName": "Graph"
                }],
       
      "settings":{
         "NETWORK.ROUTE.ENABLE":"true",
         "SERVICEPROVIDERMAP.TITLE":"",
         "SERVICEPROVIDERMAP.ABSTRACT":"",
         "SERVICEPROVIDERMAP.KEYWORDS":"",
         "SERVICEPROVIDERMAP.ONLINERESOURCE":"",
         "SERVICEPROVIDERMAP.PROVIDERNAME":"",
         "SERVICEPROVIDERMAP.PROVIDERSITE":"",
         "SERVICEPROVIDERMAP.INDIVIDUALNAME":"",
         "SERVICEPROVIDERMAP.POSITIONNAME":"",
         "SERVICEPROVIDERMAP.VOICE":"",
         "SERVICEPROVIDERMAP.FACSIMILE":"",
         "SERVICEPROVIDERMAP.DELIVERYPOINT":"",
         "SERVICEPROVIDERMAP.CITY":"",
         "SERVICEPROVIDERMAP.ADMINISTRATIVEAREA":"",
         "SERVICEPROVIDERMAP.POSTALCODE":"",
         "SERVICEPROVIDERMAP.COUNTRY":"",
         "SERVICEPROVIDERMAP.ELECTRONICMAILADDRESS":"",
         "CLUSTERNODE":"",
         "LOGCONFIG":"",
         "CONFPYRAMID":"1",
         "CACHE.EHCACHEISTRUE":"false",
         "CACHE.EHCACHEISDISK":"false",
         "CACHE.EHCACHEMEMORY":"100",
         "CACHE.EHCACHEDISK":"1",
         "CACHE.EHCACHETIME":"3600"
      }
    }
   },
   "port":"9010",
   "connpool":[
     {
   "connpoolId":"20170922140121ZUWp4kdrTjO8XPItjHQLgeK1231",
   "connpoolConfInfo":"<ConnectionPool><Pool><Name>ljfxdata</Name><NetworkFilePath>D:\\DATA\\data\\route_sy\\symx.georoute</NetworkFilePath></Pool></ConnectionPool>",
   "connpoolType":"1",
   "connpoolDbType":"10",
   "connpoolName":"route"
   }]
   
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
        <td width="100px">id</td> <td width="100px">必填</td> <td width="200px">服务ID</td>
    </tr>
        <tr>
        <td width="100px">cnName</td> <td width="100px">可选</td> <td width="200px">服务别名</td>
    </tr>
     <tr>
        <td width="100px">name</td> <td width="100px">必填</td> <td width="200px">服务名称</td>
    </tr>
        <tr>
        <td width="100px">code</td> <td width="100px">必填</td> <td width="200px">服务类型和编码（0243为路径分析服务，中间以@@@分隔，前面为服务名称NETWORK）</td>https://www.baidu.com/index.php?tn=98012088_5_dg&ch=16
    </tr>
        <tr>
        <td width="100px">iscluster</td> <td width="100px">必填</td> <td width="200px">是否是集群环境（默认值1不集群）</td>
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
   
   **NETWORK服务特有配置信息,配置服务协议信息。**
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
     <tr>
        <td width="250px">NETWORK.ROUTE.ENABLE</td> <td width="120px">必填</td> <td width="100px">ROUTE服务协议（默认值true）</td>
    </tr>
       
   </table>
##服务端口配置
>配置服务所在容器的端口信息。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
       <tr>
        <td width="250px">port</td> <td width="120px">必填</td> <td width="400px">服务所在容器的访问端口，默认9010</td>
    </tr>
    </table>
    