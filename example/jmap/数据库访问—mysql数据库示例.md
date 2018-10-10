`
	//创建数据集
	ConnectionInfo conninfo=new ConnectionInfo();   	
    conninfo.setAddress(address);
    conninfo.setProtocol(ConnectionProtocol.MYSQL);
    conninfo.setPassword(password);
    conninfo.setUsername(userName);
    Map<String, String> properties = new HashMap<String, String>();
	properties.put("PreConnectionNum", "10");
	properties.put("MaxConnectionNum", "10");
	properties.put("TimeOut", "10");
	conninfo.setProperties(properties);
	DataSourceInfo dsinfo=new DataSourceInfo();
    dsinfo.setConnectionInfo(conninfo);
    dsinfo.setDataType(DataType.VECTOR_POLYGON);
    dsinfo.setSourceType(DataSourceType.MYSQL_SOURCE);
    dsinfo.setDataName("carete_polygon");
    	
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
    int epsg = 4326;
	ICoordRefSystem crs = CoordRefSystem.newInstance(epsg);
	datasetInfo.setCoordRef(crs);
    MySQLDataBase odb=new MySQLDataBase();
    odb.setConnectionInfo(conninfo);
    GeoMySQLSpatialVectorDataSet ds=(GeoMySQLSpatialVectorDataSet)odb.createDataSet(dsinfo, datasetInfo);
	//获取数据集
	ConnectionInfo conninfo=new ConnectionInfo();   	
    conninfo.setAddress(address);
    conninfo.setProtocol(ConnectionProtocol.MYSQL);
    conninfo.setPassword(password);
    conninfo.setUsername(userName);
    Map<String, String> properties = new HashMap<String, String>();
	properties.put("PreConnectionNum", "10");
	properties.put("MaxConnectionNum", "10");
	properties.put("TimeOut", "10");
	conninfo.setProperties(properties);
	DataSourceInfo dsinfo=new DataSourceInfo();
    dsinfo.setConnectionInfo(conninfo);
    dsinfo.setDataType(DataType.VECTOR_POLYGON);
    dsinfo.setSourceType(DataSourceType.MYSQL_SOURCE);
    dsinfo.setDataName("polygon");
    MySQLDataBase mysqldatabase=new MySQLDataBase();
    DataBaseManager dbm= DataBaseManager.getInstance();
    mysqldatabase=(MySQLDataBase)dbm.getDataBaseInstance(conninfo);
    GeoMySQLSpatialVectorDataSet mysqldataset=(GeoMySQLSpatialVectorDataSet)mysqldatabase.getDataSet(dsinfo);
	//查询数据集信息
	ConnectionInfo conninfo=new ConnectionInfo();   	
    conninfo.setAddress(address);
    conninfo.setProtocol(ConnectionProtocol.MYSQL);
    conninfo.setPassword(password);
    conninfo.setUsername(userName);
	MySQLDataBase mdb=new MySQLDataBase();
	mdb.setConnectionInfo(conninfo);
	List<DataSourceInfo> dataSourceInfoLise=
    mdb.queryDataSourceInfo(DataType. TILE_IMAGE,null);//查询瓦片数据集信息

	//删除数据集
	ConnectionInfo conninfo=new ConnectionInfo();   	
    conninfo.setAddress(address);
    conninfo.setProtocol(ConnectionProtocol.MYSQL);
    conninfo.setPassword(password);
    conninfo.setUsername(userName);
    Map<String, String> properties = new HashMap<String, String>();
	properties.put("PreConnectionNum", "10");
	properties.put("MaxConnectionNum", "10");
	properties.put("TimeOut", "10");
	conninfo.setProperties(properties);
	DataSourceInfo dsinfo=new DataSourceInfo();
    dsinfo.setConnectionInfo(conninfo);
    dsinfo.setDataType(DataType.VECTOR_POLYGON);
    dsinfo.setSourceType(DataSourceType.MYSQL_SOURCE);
    dsinfo.setDataName("delete_polygon");
    MySQLDataBase mysqldatabase=new MySQLDataBase();
    DataBaseManager dbm= DataBaseManager.getInstance();
    mysqldatabase=(MySQLDataBase)dbm.getDataBaseInstance(conninfo);
    mysqldatabase.deleteDataSet(dsinfo);
`
