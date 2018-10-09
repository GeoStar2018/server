##创建数据集
`
	//数据库连接信息
	ConnectionInfo conninfo=new ConnectionInfo();   	
	conninfo.setAddress(192.168.100.1381521orcl);
	conninfo.setProtocol(ConnectionProtocol.ORACLE);
	conninfo.setPassword(sde);密码
	conninfo.setUsername(sde);用户名
	MapString, String properties = new HashMapString, String();
	properties.put(PreConnectionNum, 10);
	properties.put(MaxConnectionNum, 10);
	properties.put(TimeOut, 10);
	conninfo.setProperties(properties);
	DataSourceInfo dsinfo=new DataSourceInfo();
	dsinfo.setConnectionInfo(conninfo);
	dsinfo.setDataType(DataType.VECTOR_POLYGON);矢量面
	dsinfo.setSourceType(DataSourceType.ORACLE_SPATIAL_SOURCE);
	dsinfo.setDataName(carete_polygon);
			
	//构建属性信息
	double x1 = 180,x2 = -180,y1 = 90,y2 = -90;
	GeoEnvelope env = new GeoEnvelope(x1,x2,y1,y2); 
	AttributeInfo info = new AttributeInfo();
	AttributeItem item = new AttributeItem();
	item.setName(AREA);
	item.setType(Types.DOUBLE);
	item.setLength(38);
	info.add(item);
	AttributeItem item1 = new AttributeItem();
	item1.setName(PERIMETER);
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
`
