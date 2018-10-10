### 创建数据集
```Java
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("172.15.103.42:10001:geoglobe ");
conninfo.setProtocol(ConnectionProtocol. MONGO);
conninfo.setPassword("data ");//密码
conninfo.setUsername("data");//用户名
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);
DataSourceInfo dsinfo=new DataSourceInfo();
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);//矢量面
dsinfo.setSourceType(DataSourceType. MONGO_SOURCE);
dsinfo.setDataName("BOU2_4M_S ");

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

MongoDataBase mdb=new MongoDataBase();
mdb.setConnectionInfo(conninfo);

//创建新的数据集
MongoVectorDataSet ds=( MongoVectorDataSet) mdb.createDataSet(dsinfo, datasetInfo);
```

### 获取数据集
```Java
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("172.15.103.42:10001:geoglobe");
conninfo.setProtocol(ConnectionProtocol.MONGO);
conninfo.setPassword("data");
conninfo.setUsername("data");
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);
DataSourceInfo dsinfo=new DataSourceInfo();
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);
dsinfo.setSourceType(DataSourceType.MONGO_SOURCE);
dsinfo.setDataName("BOU2_4M_S");

MongoDataBase mdb=new MongoDataBase();
mdb.setConnectionInfo(conninfo);
MongoVectorDataSet ds=(MongoVectorDataSet)mdb.getDataSet(dsinfo);
```

### 查询数据集信息
```Java
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("172.15.103.42:10001:geoglobe");
conninfo.setProtocol(ConnectionProtocol.MONGO);
conninfo.setPassword("data");
conninfo.setUsername("data");
MongoDataBase mdb=new MongoDataBase();
mdb.setConnectionInfo(conninfo);
//查询矢量点
List<DataSourceInfo> dataSourceInfoList = mdb.queryDataSourceInfo(DataType.VECTOR_POINT,null);
```

### 删除数据集
```Java
ConnectionInfo conninfo=new ConnectionInfo();   	
conninfo.setAddress("172.15.103.42:10001:geoglobe");
conninfo.setProtocol(ConnectionProtocol.MONGO);
conninfo.setPassword("data");
conninfo.setUsername("data");
Map<String, String> properties = new HashMap<String, String>();
properties.put("PreConnectionNum", "10");
properties.put("MaxConnectionNum", "10");
properties.put("TimeOut", "10");
conninfo.setProperties(properties);
DataSourceInfo dsinfo=new DataSourceInfo();
dsinfo.setConnectionInfo(conninfo);
dsinfo.setDataType(DataType.VECTOR_POLYGON);
dsinfo.setSourceType(DataSourceType.MONGO_SOURCE);
dsinfo.setDataName("BOU2_4M_S");

MongoDataBase mdb=new MongoDataBase();
mdb.setConnectionInfo(conninfo);
MongoVectorDataSet ds=(MongoVectorDataSet)mdb.deleteDataSet(dsinfo);
```
