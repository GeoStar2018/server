### 创建并保存shape
```Java
ShapeDataBase sdb = new ShapeDataBase();
String filename = "F:\\testdata\\政区面\\xuzhou20180201\\new\\new";
IFeatureDataSet dataSet = 其他数据集得到。
sdb.save(filename, dataSet, new ShapeListener());
```

### 读取shape
```Java
ConnectionInfo cInfo = new ConnectionInfo();
cInfo.setProtocol(ConnectionProtocol.FILE);
String url = "E:\\testdata\\shp\\shapefile";
cInfo.setAddress(url);
DataSourceInfo dsInfo = new DataSourceInfo();
dsInfo.setSourceType(DataSourceType.SHPFILE_SOURCE);
dsInfo.setDataName("BOU2_4M");
dsInfo.setConnectionInfo(cInfo);
dsInfo.setDataType(DataType.VECTOR);
ShapeDataBase sdb =
(ShapeDataBase) DataBaseManager.getInstance().getDataBaseInstance(cInfo);
ShapeVectorDataSet shapeDataSet = (ShapeVectorDataSet) sdb.getDataSet(dsInfo) (
shapeCInfo, shapeDataSource);
```
