#服务配置信息详细文档

```
{
    "service": {
        "serviceInfo": {
            "cnName": "",
            "code": "MAPSERVICE@@@0234",
            "id": "20171207104649srlbJJydqqMNkX1kgXi4Ldaakjq0",
            "iscluster": "0",
            "name": "mapserver",
            "recordTime": "2018-02-01 11:25:28",
            "typeName": "MAPSERVCE",
            "settings": {
                "CACHE.EHCACHEDISK": "1",
                "CACHE.EHCACHEISDISK": "false",
                "CACHE.EHCACHEISTRUE": "false",
                "CACHE.EHCACHEMEMORY": "100",
                "CACHE.EHCACHETIME": "3600",
                "CLUSTERNODE": "",
                "CONFPYRAMID": "1",
                "LOGCONFIG": "",
                "MAPSERVICE.GEOMAPSERVICE.ENABLE": "true",
                "MAPSERVICE.GEOMAPSERVICE.LAYER": "xz_yx",
                "MAPSERVICE.GEOMAPSERVICE.MAXHEIGHT": "500",
                "MAPSERVICE.GEOMAPSERVICE.MAXWIDTH": "500",
                "MAPSERVICE.GEOMAPSERVICE.PAGENUMBER": "100",
                "MAPSERVICE.TILE.ENABLE": "true",
                "MAPSERVICE.TILE.LAYER": "xz_sl",
                "MAPSERVICE.WCS.ENABLE": "true",
                "MAPSERVICE.WCS.MAXHEIGHT": "500",
                "MAPSERVICE.WCS.MAXWIDTH": "500",
                "MAPSERVICE.WFS.ENABLE": "true",
                "MAPSERVICE.WFS.PAGENUMBER": "100",
                "MAPSERVICE.WFS.WFS_COORD_ORDER": "latlng",
                "MAPSERVICE.WMS.ENABLE": "true",
                "MAPSERVICE.WMS.ISTRANS": "true",
                "MAPSERVICE.WMS.MAXHEIGHT": "500",
                "MAPSERVICE.WMS.MAXWIDTH": "500",
                "MAPSERVICE.WMS.WMS_COORD_ORDER": "latlng",
                "MAPSERVICE.WMTS.ENABLE": "true",
                "MAPSERVICE.WMTS.WMTS_COORD_ORDER": "latlng",
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
                "LAYER.DATA": "xz_vec_pick11:10-15",
            },
            "dataItem": [
                {
                    "dataSourceType": "OracleSource",
                    "dataType": "VECTORTILE",
                    "dbcpId": "20171024105227Lz8XfunP66QpuYxvOU0s6TPUs0eW",
                    "layerName": "xz_sl"
                },
                {
                    "dataSourceType": "OracleSource",
                    "dataType": "IMAGETILE",
                    "dbcpId": "20171024105227Lz8XfunP66QpuYxvOU0s6TPUs0eW",
                    "layerName": "xz_yx"
                },
                {
                    "dataSourceType": "OracleSpatialSource",
                    "dataType": "VECTORPOLYGON",
                    "dbcpId": "20171024105227Lz8XfunP66QpuYxvOU0s6TPUs0eW",
                    "layerName": "data.BOU1_4M_S"
                },
                {
                    "dataSourceType": "GeoGlobeFileSource",
                    "dataType": "VECTORTILE",
                    "dbcpId": "20170922140121ZUWp4kdrTjO8XPItjHQLgeKpi41",
                    "layerName": "xz_vec_pick11"
                }
            ]
        }
    },
    "connpool":[
     {
	   "connpoolId":"20171024105227Lz8XfunP66QpuYxvOU0s6TPUs0eW",
	   "connpoolConfInfo":"<ConnectionPool><Pool><Name>29</Name><Type>JDBC</Type><MetaOwner>GEOSTAR</MetaOwner><Driver>oracle.jdbc.driver.OracleDriver</Driver><URL>jdbc:oracle:thin:@192.168.30.29:1521/geoglobe</URL><User>data</User><Password>data</Password><IsCustom>2</IsCustom><PreConnectionNum>1</PreConnectionNum><MaxConnectionNum>15</MaxConnectionNum><TimeOut>300</TimeOut></Pool></ConnectionPool>",
	   "connpoolType":"1",
	   "connpoolDbType":"1",
	   "connpoolName":"29"
     },
     {
            "connpoolConfInfo": "<ConnectionPool><Pool><Name>tile</Name><isTraverseFolder>false</isTraverseFolder><PreConnectionNum>1</PreConnectionNum><MaxConnectionNum>15</MaxConnectionNum><URL>C:\\Users\\shubangjie\\Desktop\\tile\\</URL><isMemoryDB>false</isMemoryDB><Max_Page_Count>0</Max_Page_Count></Pool></ConnectionPool>",
            "connpoolDbType": "2",
            "connpoolId": "20170922140121ZUWp4kdrTjO8XPItjHQLgeKpi41",
            "connpoolName": "tile",
            "connpoolType": "2"
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
        <td width="100px">cnName</td> <td width="100px">可选</td> <td width="200px">服务别名</td>
    </tr>
        <tr>
        <td width="100px">code</td> <td width="100px">必填</td> <td width="200px">服务类型和编码（0234为地图服务，中间以@@@分隔，前面为服务名称MAPSERVICE）</td>
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


##服务提供者信息配置
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
   
   >MAPSERVICE服务特有配置信息,配置服务协议信息。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
     <tr>
        <td width="250px">MAPSERVICE.GEOMAPSERVICE.ENABLE</td> <td width="120px">必填</td> <td width="100px">MAPSERVICE协议（默认值true）</td>
    </tr>
     <tr>
        <td width="250px">MAPSERVICE.GEOMAPSERVICE.LAYER</td> <td width="120px">必填</td> <td width="100px">缓存图层（地图服务rest接口缓存图层数据）</td>
    </tr>
         <tr>
        <td width="250px">MAPSERVICE.GEOMAPSERVICE.MAXHEIGHT</td> <td width="120px">可选</td> <td width="100px">图片最大像素高</td>
    </tr>
      <tr>
        <td width="250px">MAPSERVICE.GEOMAPSERVICE.MAXWIDTH</td> <td width="120px">可选</td> <td width="100px">图片最大像素宽</td>
    </tr>
      <tr>
        <td width="250px">MAPSERVICE.GEOMAPSERVICE.PAGENUMBER</td> <td width="120px">可选</td> <td width="400px">响应限制条数</td>
    </tr>
      <tr>
        <td width="250px">MAPSERVICE.TILE.ENABLE</td> <td width="120px">必填</td> <td width="400px">地图服务TILE接口协议（默认值true）</td>
    </tr>
      <tr>
        <td width="250px">MAPSERVICE.TILE.LAYER</td> <td width="120px">必填</td> <td width="400px">TILE接口选择发布图层</td>
    </tr>
      <tr>
        <td width="250px">MAPSERVICE.WCS.ENABLE</td> <td width="120px">必填</td> <td width="400px">地图服务WCS接口协议（默认值true）</td>
    </tr>
    <tr>
        <td width="250px">MAPSERVICE.WCS.MAXHEIGHT</td> <td width="120px">可选</td> <td width="400px">图片最大像素高</td>
    </tr>
    <tr>
        <td width="250px">MAPSERVICE.WCS.MAXWIDTH</td> <td width="120px">可选</td> <td width="400px">图片最大像素宽</td>
    </tr>
    <tr>
        <td width="250px">MAPSERVICE.WFS.ENABLE</td> <td width="120px">必填</td> <td width="400px">地图服务WFS接口协议（默认值true）</td>
    </tr>
       <tr>
        <td width="250px">MAPSERVICE.WFS.PAGENUMBER</td> <td width="120px">可选</td> <td width="400px">响应限制条数</td>
    </tr>
    <tr>
        <td width="250px">MAPSERVICE.WFS.WFS_COORD_ORDER</td> <td width="120px">必填</td> <td width="400px">矢量瓦片配置样式信息</td>
    </tr>
     <tr>
        <td width="250px">MAPSERVICE.WMTS.ENABLE</td> <td width="120px">必填</td> <td width="400px">地图服务WMTS接口协议（默认值true）</td>
    </tr>
    <tr>
        <td width="250px">MAPSERVICE.WMTS.WMTS_COORD_ORDER</td> <td width="120px">必填</td> <td width="400px">坐标轴顺序（OGC标准:latlng/强制东西向在前:lnglat/强制南北向在前:northfirst）</td>
    </tr>
     <tr>
        <td width="250px">LAYER.DATA</td> <td width="120px">必填</td> <td width="400px">服务数据层级信息（按照格式图层名称:顶层-底层）</td>
    </tr>
    <tr>
        <td width="250px">dataItem</td> <td width="120px">必填</td> <td width="400px">服务配置数据源信息</td>
    </tr>
             <tr>
        <td width="250px">dataSourceType</td> <td width="120px">必填</td> <td width="400px">数据源类型（多个以逗号分隔）：<br/>
        
        1.文件数据源GeoGlobeFileSource<br/>
        2.oracle数据源OracleSpatialSource或者OracleSource<br/>
        3.mysql数据源MySQLSource<br/>
        4.DaMeng数据源DaMengSource<br/>
</td>
    </tr>
        <tr>
        <td width="250px">dataType</td> <td width="120px">必填</td> <td width="400px">数据类型</td>
    </tr>
    <tr>
        <td width="250px">dbcpId</td> <td width="120px">必填</td> <td width="400px">数据源名称ID</td>
    </tr>
        <tr>
        <td width="250px">layerName</td> <td width="120px">必填</td> <td width="400px">配置图层名称</td>
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
        <td width="250px">connpoolConfInfo</td> <td width="120px">必填</td> <td width="400px">数据源配置基础信息（JDBC连接串、文件地址）</td>
    </tr>
       <tr>
        <td width="250px">connpoolDbType</td> <td width="120px">必填</td> <td width="400px">数据库类型：<br/>
					        1, Oracle数据<br/>
					        2, GeoGlobe文件数据<br/>
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
    