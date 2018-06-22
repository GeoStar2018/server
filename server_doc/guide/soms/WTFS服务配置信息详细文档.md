#WTFS服务配置信息详细文档

```
{
"port":"9010",
    "service": {
        "serviceInfo": {
            "cnName": "",
            "code": "WTFS@@@0207",
            "id": "20171207104649srlbJJydqqMNkX1kgXi4Ldaakjq0",
            "iscluster": "0",
            "name": "wtfs",
            "recordTime": "2018-02-01 11:25:28",
            "typeName": "WTFS",
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
                "SERVICEPROVIDERMAP.ONLINERESOURCE": "",
                "SERVICEPROVIDERMAP.POSITIONNAME": "",
                "SERVICEPROVIDERMAP.POSTALCODE": "",
                "SERVICEPROVIDERMAP.PROVIDERNAME": "",
                "SERVICEPROVIDERMAP.PROVIDERSITE": "",
                "SERVICEPROVIDERMAP.TITLE": "",
                "SERVICEPROVIDERMAP.VOICE": "",
                "WTFS.WTFS.ENABLE": "true"
            },
            "dataItem": [
                {
                    "dataSourceType": "OracleSource",
                    "dataType": "TILEPLN",
                    "dbcpId": "20180426145439TW3XCXVqGqHfsJbz6mH7YJLgBYkZ",
                    "layerName": "autotest.SWDM_XC2089"
                }
            ]
        }
    },
    "connpool":[
        {
   "connpoolId":"20180426145439TW3XCXVqGqHfsJbz6mH7YJLgBYkZ",
   "connpoolConfInfo":"<ConnectionPool><Pool><Name>oracle43</Name><Type>JDBC</Type><MetaOwner>GEOSTAR</MetaOwner><Driver>oracle.jdbc.driver.OracleDriver</Driver><URL>jdbc:oracle:thin:@172.15.103.43:1521/geoglobe</URL><User>autotest</User><Password>autotest</Password><IsCustom>2</IsCustom><PreConnectionNum>1</PreConnectionNum><MaxConnectionNum>15</MaxConnectionNum><TimeOut>300</TimeOut></Pool></ConnectionPool>",
   "connpoolType":"1",
   "connpoolDbType":"1",
   "connpoolName":"oracle43"
   }
  ],
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
        <td width="100px">id</td> <td width="100px">必填</td> <td width="200px">服务ID</td>
    </tr>
        <tr>
        <td width="100px">cnName</td> <td width="100px">可选</td> <td width="200px">服务别名</td>
    </tr>
     <tr>
        <td width="100px">name</td> <td width="100px">必填</td> <td width="200px">服务名称</td>
    </tr>
        <tr>
        <td width="100px">code</td> <td width="100px">必填</td> <td width="200px">服务类型和编码（0207为三维地名服务，中间以@@@分隔，前面为服务名称WTFS）</td>
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
   
   **WTFS服务特有配置信息,配置服务协议信息。**
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
     <tr>
        <td width="250px">WTFS.WTFS.ENABLE</td> <td width="120px">必填</td> <td width="100px">WTFS服务协议（默认值true）</td>
    </tr>
      <tr>
        <td width="250px">dataItem</td> <td width="120px">必填</td> <td width="400px">服务数据图层配置信息，可能多个图层</td>
    </tr>
    <tr>
        <td width="250px">dbcpId</td> <td width="120px">必填</td> <td width="400px">数据ID（和数据源配置信息ID关联）多个需要在dataItem中多个节点</td>
    </tr>
    <tr>
        <td width="250px">layerName</td> <td width="120px">必填</td> <td width="400px">图层名称</td>
    </tr>
      <tr>
        <td width="250px">dataSourceType</td> <td width="120px">必填</td> <td width="400px">数据源类型：<br/>
    
        1.oracle数据源OracleSpatialSource或者OracleSource<br/>
        2.mysql数据源MySQLSource<br/>
        3.DaMeng数据源DaMengSource<br/>
</td>
    </tr>
    <tr>
        <td width="250px">dataType</td> <td width="120px">必填</td> <td width="400px">矢量（VECTORPOINT/VECTORLINE/VECTORPOLYGON）</td>
    </tr>
    <tr>
        <td width="250px">LAYER.DATA</td> <td width="120px">选填</td> <td width="400px">扩展信息</td>
    </tr>
       
   </table>
##数据源信息配置
>数据源配置信息，配置服务所需数据源信息。数据源信息包括数据连接串、文件地址等等。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
       <tr>
        <td width="250px">connpool</td> <td width="120px">必填</td> <td width="400px">数据源节点（可以配置多个）</td>
    </tr>
       <tr>
        <td width="250px">connpoolConfInfo</td> <td width="120px">必填</td> <td width="400px">数据源配置基础信息（用户名、密码、连接串、文件地址）</td>
    </tr>
       <tr>
        <td width="250px">connpoolDbType</td> <td width="120px">必填</td> <td width="400px">数据库类型：<br/>
					        1, Oracle数据<br/>
					        3, MySql数据<br/>
					        12,达梦数据<br/>
</td>
    </tr>
       <tr>
        <td width="250px">connpoolId</td> <td width="120px">必填</td> <td width="400px">数据源ID</td>
    </tr>
       <tr>
        <td width="250px">connpoolName</td> <td width="120px">必填</td> <td width="400px">数据源名称</td>
    </tr>
       <tr>
        <td width="250px">connpoolType</td> <td width="120px">必填</td> <td width="400px">数据源类型(1.JDBC，2.表示其它方式)</td>
    </tr>
    </table>
    