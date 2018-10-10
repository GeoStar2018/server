### 创建数据集
```Java
//可由其他数据集构造而来，也可以自己临时构造，目前仅支持矢量数据
DataSourceInfo dataSourceInfo = 其他数据集信息得到。
IDataSetInfo metaInfo = （AbstractVectorDataSetInfo）其他数据源得到。
MemoryDataBase mdb = new MemoryDataBase();
MemoryVectorDataSet dataset2 =mdb. createDataSet (dataSourceInfo, metaInfo);
```
### 获取数据集
```Java
DataSourceInfo dataSourceInfo = 其他数据集信息得到。
MemoryDataBase mdb = new MemoryDataBase();
MemoryVectorDataSet dataset2 =mdb. getDataSet(dataSourceInfo);
```
