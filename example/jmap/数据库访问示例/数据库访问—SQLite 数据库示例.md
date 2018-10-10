### 创建数据集
```Java
//数据库连接信息
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("192.168.100.138:1521:orcl");
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword("sde");//密码
conninfo.setUsername("sde");//用户名
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);
DataSourceInfo dsinfo=new DataSourceInfo();
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);//矢量面
dsinfo.setSourceType(DataSourceType.ORACLE_SPATIAL_SOURCE);
dsinfo.setDataName("carete_polygon");

//构建属性信息
double x1 = 180,x2 = -180,y1 = 90,y2 = -90;
GeoEnvelope env = new GeoEnvelope(x1,x2,y1,y2);
AttributeInfo info = new AttributeInfo();
AttributeItem item = new AttributeItem();
item.setName("AREA");
item.setType(Types.DOUBLE);
item.setLength(38);
info.add(item);
AttributeItem item1 = new AttributeItem();
item1.setName("PERIMETER");
item1.setType(Types.DOUBLE);		
item1.setLength(38);
info.add(item1);
VectorDataSetInfo datasetInfo = new VectorDataSetInfo();   	
datasetInfo.setGeometryType(GeometryType.POLYGON);
datasetInfo.setEnvelope(env);
datasetInfo.setAttributeInfo(info);

OracleDataBase odb=new OracleDataBase();
odb.setConnectionInfo(conninfo);

//创建新的数据集
GeoOracleSpatialVectorDataSet ds=(GeoOracleSpatialVectorDataSet)odb.createDataSet(dsinfo, datasetInfo);
```

### 获取数据集
```Java
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("192.168.100.138:1521:orcl");
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword("sde");
conninfo.setUsername("sde");
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);
DataSourceInfo dsinfo=new DataSourceInfo();
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);
dsinfo.setSourceType(DataSourceType.ORACLE_SOURCE);
dsinfo.setDataName("test_polygon");//数据集名称

OracleDataBase odb=new OracleDataBase();
odb.setConnectionInfo(conninfo);
OracleSpatialVectorDataSet ds=(OracleSpatialVectorDataSet)odb.getDataSet(dsinfo);
```
### 查询数据集信息
```Java
//查询某个库所有的数据集信息
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress(address);
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword(password);
conninfo.setUsername(userName);
OracleDataBase odb=new OracleDataBase();
odb.setConnectionInfo(conninfo);
List<DataSourceInfo> dataSourceInfoLise=odb.queryDataSourceInfo();

//查询某一类的数据集信息
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress(address);
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword(password);
conninfo.setUsername(userName);
OracleDataBase odb=new OracleDataBase();
odb.setConnectionInfo(conninfo);
//查询矢量点
List<DataSourceInfo> dataSourceInfoLise=odb.queryDataSourceInfo(DataType.VECTOR_POINT,null);

//查询某一类的包含某个字符的数据集信息
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress(address);
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword(password);
conninfo.setUsername(userName);
OracleDataBase odb=new OracleDataBase();
odb.setConnectionInfo(conninfo);
//查询名称中包含test的矢量点数据集
List<DataSourceInfo> dataSourceInfoLise=odb.queryDataSourceInfo(DataType.VECTOR_POINT,"test");
```

### 删除数据集
```Java
ConnectionInfo conninfo=new ConnectionInfo();  //创建 数据连接资源对象
conninfo.setAddress("192.168.100.138:1521:orcl");
conninfo.setProtocol(ConnectionProtocol.ORACLE);
conninfo.setPassword("sde");
conninfo.setUsername("sde");
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);

DataSourceInfo dsinfo=new DataSourceInfo(); //数据源信息对象
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);
dsinfo.setSourceType(DataSourceType.ORACLE_SOURCE);
dsinfo.setDataName("delete_oracleSpatial_polygon");

OracleDataBase oracledatabase=new OracleDataBase();
DataBaseManager dbm= DataBaseManager.getInstance();
oracledatabase=(OracleDataBase)dbm.getDataBaseInstance(conninfo);
//删除指定的数据集
oracledatabase.deleteDataSet(dsinfo);
```
