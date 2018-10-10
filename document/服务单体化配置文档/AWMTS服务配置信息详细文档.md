#服务配置信息详细文档

```
{
    "service": {
        "serviceInfo": {
            "cnName": "",
            "code": "AWMTS@@@0220",
            "id": "20171207104649srlbJJydqqMNkX1kgXi4Ldaakjq0",
            "iscluster": "0",
            "name": "awmts",
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
	            "AWMTSLAYERUNINAME": "awmts",
	            "AWMTS.WMTS.ENABLE": "true",
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
                "SERVICEPROVIDERMAP.VOICE": ""
            },
            "subservice": [
                {
                    "PROVCODE": "420000",
                    "TCOUNT": "3",
                    "TINTERVAL": "300",
                    "TOUT": "3",
                    "WMTSAGGTOGETHERXML": "<WMTSAggServer><ConfSubservice><Layer><Name>dg_yx1</Name><Select>true</Select><LayerDataLevel>8@9@10@11@12@13@14</LayerDataLevel><LayerSelectLevel>8@9@10@11@12@13@14</LayerSelectLevel><StartDataLevel>8</StartDataLevel><EndDataLevel>14</EndDataLevel><Extent>113.67198309216,22.9144192387309,113.790845537088,23.0429109273697</Extent></Layer><ProvCode>420000</ProvCode><CityCode></CityCode></ConfSubservice></WMTSAggServer>",
                    "WMTSSTATUS": "1",
                    "WMTSXML": "
<Capabilities xmlns='http://www.opengis.net/wmts/1.0' xmlns:ows='http://www.opengis.net/ows/1.1' xmlns:gml='http://www.opengis.net/gml' xmlns:xsi='http://www.w3.org/2001/XMLSchema-instance' xmlns:xlink='http://www.w3.org/1999/xlink' version='1.0.0' xsi:schemaLocation='http://www.opengis.net/wmts/1.0 http://schemas.opengis.net/wmts/1.0.0/wmtsGetCapabilities_response.xsd'>
    <ows:ServiceIdentification>
        <ows:Title>Web Map Tile Service</ows:Title>
        <ows:Abstract>基于瓦片的网络地图服务</ows:Abstract>
        <ows:Keywords>
            <ows:Keyword>OGC WMTS 1.0.0</ows:Keyword>
        </ows:Keywords>
        <ows:ServiceType>OGC WMTS</ows:ServiceType>
        <ows:ServiceTypeVersion>1.0.0</ows:ServiceTypeVersion>
        <ows:Fees>none</ows:Fees>
        <ows:AccessConstraints>none</ows:AccessConstraints>
    </ows:ServiceIdentification>
    <ows:ServiceProvider>
        <ows:ProviderName>武大吉奥信息技术有限公司</ows:ProviderName>
        <ows:ProviderSite xlink:href='http://www.geostar.com.cn'/>
        <ows:ServiceContact>
            <ows:IndividualName>Mr Lin</ows:IndividualName>
            <ows:PositionName>Software Engineer</ows:PositionName>
            <ows:ContactInfo>
                <ows:Phone>
                    <ows:Voice>027-87196134</ows:Voice>
                    <ows:Facsimile>800-880-9008</ows:Facsimile>
                </ows:Phone>
                <ows:Address>
                    <ows:DeliveryPoint>武汉东湖新技术开发区庙山小区武大科技园</ows:DeliveryPoint>
                    <ows:City>武汉市</ows:City>
                    <ows:AdministrativeArea>湖北省</ows:AdministrativeArea>
                    <ows:Country>中国</ows:Country>
                    <ows:PostalCode>430223</ows:PostalCode>
                    <ows:ElectronicMailAddress>linjun@geostar.com.cn</ows:ElectronicMailAddress>
                </ows:Address>
                <ows:OnlineResource xlink:type='simple' xlink:href='http://172.15.103.85:9010/map1/wmts'/>
            </ows:ContactInfo>
        </ows:ServiceContact>
        <ows:RecordTime>2018-04-23 15:25:08</ows:RecordTime>
    </ows:ServiceProvider>
    <ows:OperationsMetadata>
        <ows:Operation name='GetCapabilities'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map1/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetVersions'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map1/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetVersionInfo'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map1/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetTile'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map1/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:ExtendedCapabilities>
            <ows:Constraint name='GeoGlobeBuildVersion'>
                <ows:Value>6.5.0.17233</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='96DPIPyramidType'>
                <ows:Value>Matrix_dg_yx1_0</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='OGCPyramidType'>
                <ows:Value>Matrix_dg_yx1_1</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='ArcGISPyramidType'>
                <ows:Value>Matrix_dg_yx1_2</ows:Value>
            </ows:Constraint>
        </ows:ExtendedCapabilities>
    </ows:OperationsMetadata>
    <Contents>
        <Layer>
            <ows:Title>dg_yx1</ows:Title>
            <ows:Abstract>dg_yx1</ows:Abstract>
            <ows:Identifier>dg_yx1</ows:Identifier>
            <ows:WGS84BoundingBox>
                <ows:LowerCorner>113.67198309216 22.9144192387309</ows:LowerCorner>
                <ows:UpperCorner>113.790845537088 23.0429109273697</ows:UpperCorner>
            </ows:WGS84BoundingBox>
            <ows:BoundingBox>
                <ows:LowerCorner>113.67198309216 22.9144192387309</ows:LowerCorner>
                <ows:UpperCorner>113.790845537088 23.0429109273697</ows:UpperCorner>
            </ows:BoundingBox>
            <Style isDefault='true'>
                <ows:Identifier>dg_yx1</ows:Identifier>
            </Style>
            <Format>image/tile</Format>
            <Format>image/png</Format>
            <Format>image/jpeg</Format>
            <Format>image/gif</Format>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx1_0</TileMatrixSet>
            </TileMatrixSetLink>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx1_1</TileMatrixSet>
            </TileMatrixSetLink>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx1_2</TileMatrixSet>
            </TileMatrixSetLink>
        </Layer>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx1_0</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2311166.839488794</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1155583.419744397</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>577791.7098721985</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>288895.85493609926</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>144447.92746804963</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3343</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>72223.96373402482</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6686</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>36111.98186701241</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13371</MatrixWidth>
                <MatrixHeight>3054</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx1_1</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2183910.726031423</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1091955.3630157115</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>545977.6815078558</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>272988.8407539279</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>136494.42037696394</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3343</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>68247.21018848197</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6686</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>34123.605094240986</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13371</MatrixWidth>
                <MatrixHeight>3054</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx1_2</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2181465.880112383</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1090732.9400561915</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>545366.4700280958</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>272683.2350140479</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>136341.61750702394</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3343</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>68170.80875351197</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6686</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>34085.404376755985</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13371</MatrixWidth>
                <MatrixHeight>3054</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
    </Contents>
</Capabilities>",
                    "CODE": "0",
                    "NAME": "map1",
                    "URL": "http://172.15.103.85:9010/map1/wmts",
                    "VERSION": "1.0.0"
                },
                {
                    "PROVCODE": "430000",
                    "TCOUNT": "3",
                    "TINTERVAL": "300",
                    "TOUT": "3",
                    "WMTSAGGTOGETHERXML": "<WMTSAggServer><ConfSubservice><Layer><Name>dg_yx2</Name><Select>true</Select><LayerDataLevel>8@9@10@11@12@13@14</LayerDataLevel><LayerSelectLevel>8@9@10@11@12@13@14</LayerSelectLevel><StartDataLevel>8</StartDataLevel><EndDataLevel>14</EndDataLevel><Extent>113.72964156243201,22.9301598599023,113.84650684962,23.1063860389938</Extent></Layer><ProvCode>430000</ProvCode><CityCode></CityCode></ConfSubservice></WMTSAggServer>",
                    "WMTSSTATUS": "1",
                    "WMTSXML": "
<Capabilities xmlns='http://www.opengis.net/wmts/1.0' xmlns:ows='http://www.opengis.net/ows/1.1' xmlns:gml='http://www.opengis.net/gml' xmlns:xsi='http://www.w3.org/2001/XMLSchema-instance' xmlns:xlink='http://www.w3.org/1999/xlink' version='1.0.0' xsi:schemaLocation='http://www.opengis.net/wmts/1.0 http://schemas.opengis.net/wmts/1.0.0/wmtsGetCapabilities_response.xsd'>
    <ows:ServiceIdentification>
        <ows:Title>Web Map Tile Service</ows:Title>
        <ows:Abstract>基于瓦片的网络地图服务</ows:Abstract>
        <ows:Keywords>
            <ows:Keyword>OGC WMTS 1.0.0</ows:Keyword>
        </ows:Keywords>
        <ows:ServiceType>OGC WMTS</ows:ServiceType>
        <ows:ServiceTypeVersion>1.0.0</ows:ServiceTypeVersion>
        <ows:Fees>none</ows:Fees>
        <ows:AccessConstraints>none</ows:AccessConstraints>
    </ows:ServiceIdentification>
    <ows:ServiceProvider>
        <ows:ProviderName>武大吉奥信息技术有限公司</ows:ProviderName>
        <ows:ProviderSite xlink:href='http://www.geostar.com.cn'/>
        <ows:ServiceContact>
            <ows:IndividualName>Mr Lin</ows:IndividualName>
            <ows:PositionName>Software Engineer</ows:PositionName>
            <ows:ContactInfo>
                <ows:Phone>
                    <ows:Voice>027-87196134</ows:Voice>
                    <ows:Facsimile>800-880-9008</ows:Facsimile>
                </ows:Phone>
                <ows:Address>
                    <ows:DeliveryPoint>武汉东湖新技术开发区庙山小区武大科技园</ows:DeliveryPoint>
                    <ows:City>武汉市</ows:City>
                    <ows:AdministrativeArea>湖北省</ows:AdministrativeArea>
                    <ows:Country>中国</ows:Country>
                    <ows:PostalCode>430223</ows:PostalCode>
                    <ows:ElectronicMailAddress>linjun@geostar.com.cn</ows:ElectronicMailAddress>
                </ows:Address>
                <ows:OnlineResource xlink:type='simple' xlink:href='http://172.15.103.85:9010/map2/wmts'/>
            </ows:ContactInfo>
        </ows:ServiceContact>
        <ows:RecordTime>2018-04-23 15:24:34</ows:RecordTime>
    </ows:ServiceProvider>
    <ows:OperationsMetadata>
        <ows:Operation name='GetCapabilities'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map2/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetVersions'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map2/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetVersionInfo'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map2/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:Operation name='GetTile'>
            <ows:DCP>
                <ows:HTTP>
                    <ows:Get xlink:href='http://172.15.103.85:9010/map2/wmts?'>
                        <ows:Constraint name='GetEncoding'>
                            <ows:AllowedValues>
                                <ows:Value>KVP</ows:Value>
                            </ows:AllowedValues>
                        </ows:Constraint>
                    </ows:Get>
                </ows:HTTP>
            </ows:DCP>
        </ows:Operation>
        <ows:ExtendedCapabilities>
            <ows:Constraint name='GeoGlobeBuildVersion'>
                <ows:Value>6.5.0.17233</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='96DPIPyramidType'>
                <ows:Value>Matrix_dg_yx2_0</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='OGCPyramidType'>
                <ows:Value>Matrix_dg_yx2_1</ows:Value>
            </ows:Constraint>
            <ows:Constraint name='ArcGISPyramidType'>
                <ows:Value>Matrix_dg_yx2_2</ows:Value>
            </ows:Constraint>
        </ows:ExtendedCapabilities>
    </ows:OperationsMetadata>
    <Contents>
        <Layer>
            <ows:Title>dg_yx2</ows:Title>
            <ows:Abstract>dg_yx2</ows:Abstract>
            <ows:Identifier>dg_yx2</ows:Identifier>
            <ows:WGS84BoundingBox>
                <ows:LowerCorner>113.72964156243201 22.9301598599023</ows:LowerCorner>
                <ows:UpperCorner>113.84650684962 23.1063860389938</ows:UpperCorner>
            </ows:WGS84BoundingBox>
            <ows:BoundingBox>
                <ows:LowerCorner>113.72964156243201 22.9301598599023</ows:LowerCorner>
                <ows:UpperCorner>113.84650684962 23.1063860389938</ows:UpperCorner>
            </ows:BoundingBox>
            <Style isDefault='true'>
                <ows:Identifier>dg_yx2</ows:Identifier>
            </Style>
            <Format>image/tile</Format>
            <Format>image/png</Format>
            <Format>image/jpeg</Format>
            <Format>image/gif</Format>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx2_0</TileMatrixSet>
            </TileMatrixSetLink>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx2_1</TileMatrixSet>
            </TileMatrixSetLink>
            <TileMatrixSetLink>
                <TileMatrixSet>Matrix_dg_yx2_2</TileMatrixSet>
            </TileMatrixSetLink>
        </Layer>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx2_0</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2311166.839488794</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1155583.419744397</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>577791.7098721985</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>288895.85493609926</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>144447.92746804963</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3344</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>72223.96373402482</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6687</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>36111.98186701241</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13374</MatrixWidth>
                <MatrixHeight>3053</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx2_1</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2183910.726031423</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1091955.3630157115</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>545977.6815078558</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>272988.8407539279</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>136494.42037696394</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3344</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>68247.21018848197</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6687</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>34123.605094240986</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13374</MatrixWidth>
                <MatrixHeight>3053</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
        <TileMatrixSet>
            <ows:Identifier>Matrix_dg_yx2_2</ows:Identifier>
            <ows:SupportedCRS>urn:ogc:def:crs:EPSG::4490</ows:SupportedCRS>
            <TileMatrix>
                <ows:Identifier>8</ows:Identifier>
                <ScaleDenominator>2181465.880112383</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>209</MatrixWidth>
                <MatrixHeight>48</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>9</ows:Identifier>
                <ScaleDenominator>1090732.9400561915</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>418</MatrixWidth>
                <MatrixHeight>96</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>10</ows:Identifier>
                <ScaleDenominator>545366.4700280958</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>836</MatrixWidth>
                <MatrixHeight>191</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>11</ows:Identifier>
                <ScaleDenominator>272683.2350140479</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>1672</MatrixWidth>
                <MatrixHeight>382</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>12</ows:Identifier>
                <ScaleDenominator>136341.61750702394</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>3344</MatrixWidth>
                <MatrixHeight>764</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>13</ows:Identifier>
                <ScaleDenominator>68170.80875351197</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>6687</MatrixWidth>
                <MatrixHeight>1527</MatrixHeight>
            </TileMatrix>
            <TileMatrix>
                <ows:Identifier>14</ows:Identifier>
                <ScaleDenominator>34085.404376755985</ScaleDenominator>
                <TopLeftCorner>90.0 -180.0</TopLeftCorner>
                <TileWidth>256</TileWidth>
                <TileHeight>256</TileHeight>
                <MatrixWidth>13374</MatrixWidth>
                <MatrixHeight>3053</MatrixHeight>
            </TileMatrix>
        </TileMatrixSet>
    </Contents>
</Capabilities>",
                    "CODE": "1",
                    "NAME": "map2",
                    "URL": "http://172.15.103.85:9010/map2/wmts",
                    "VERSION": "1.0.0"
                }
            ],
            "typeName": "MAPSERVCE"
        }
    },
    "confPyramid":[{
      "pyid":"1",
      "pyramidName":"360度金字塔",
      "topLeft":"-180.0,90.0",
      "scale":"5.916587109091313E8,2.9582935545456564E8,1.4791467772728282E8,7.395733886364141E7,3.6978669431820706E7,1.8489334715910353E7,9244667.357955176,4622333.678977588,2311166.839488794,1155583.419744397,577791.7098721985,288895.85493609926,144447.92746804963,72223.96373402482,36111.98186701241,18055.990933506204,9027.995466753102,4513.997733376551,2256.9988666882755,1128.4994333441377,564.2497166720689",
      "epsg":"4490",
      "imageWidth":"256",
      "imageHeight":"256",
      "coordOrder":"latlng",
      "span":"360",
      "resolution":"96"
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
        <td width="100px">code</td> <td width="100px">必填</td> <td width="200px">服务类型和编码（0220为聚合服务服务，中间以@@@分隔，前面为服务名称AWMTS）</td>
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
   
   >VTS服务特有配置信息,配置服务协议信息。
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
     <tr>
        <td width="250px">AWMTS.WMTS.ENABLE</td> <td width="120px">必填</td> <td width="100px">AWMTS服务协议（默认值true）</td>
    </tr>
     <tr>
        <td width="250px">AWMTSLAYERUNINAME</td> <td width="120px">必填</td> <td width="100px">聚合服务名称</td>
    </tr>
   </table>
##子服务配置信息
>聚合服务需要配置子服务（地图服务WMTS接口）
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
       <tr>
        <td width="250px">subservice</td> <td width="120px">必填</td> <td width="400px">子服务节点（可以配置多个）</td>
    </tr>
       <tr>
        <td width="250px">PROVCODE</td> <td width="120px">必填</td> <td width="400px">省编号</td>
    </tr>
       <tr>
        <td width="250px">TCOUNT</td> <td width="120px">必填</td> <td width="400px">总数（3）
</td>
    </tr>
       <tr>
        <td width="250px">TINTERVAL</td> <td width="120px">必填</td> <td width="400px">间隔时间（300）</td>
    </tr>
       <tr>
        <td width="250px">WMTSSTATUS</td> <td width="120px">必填</td> <td width="400px">状态（默认1）</td>
    </tr>
       <tr>
        <td width="250px">CODE</td> <td width="120px">必填</td> <td width="400px">编号（子服务1编号为0，编号从0开始）</td>
    </tr>
       <tr>
        <td width="250px">NAME</td> <td width="120px">必填</td> <td width="400px">子服务名称</td>
    </tr>
      <tr>
        <td width="250px">URL</td> <td width="120px">必填</td> <td width="400px">子服务WMTS接口请求地址</td>
    </tr>
     <tr>
        <td width="250px">VERSION</td> <td width="120px">必填</td> <td width="400px">请求接口版本号</td>
    </tr>
    <tr>
        <td width="250px">WMTSXML</td> <td width="120px">必填</td> <td width="400px">子服务WMTS接口Capabilities信息</td>
    </tr>
    <tr>
        <td width="250px">WMTSAGGTOGETHERXML</td> <td width="120px">必填</td> <td width="400px">配置子服务基本信息（图层名称，层级，数据范围，行政编码）</td>
    </tr>
   </table>
##金字塔配置信息
>聚合服务金字塔模型数据
<table>
    <tr>
        <td width="250px">名称</td> <td width="120px">是否可选</td> <td width="400px">描述</td>
    </tr>
       <tr>
        <td width="250px">confPyramid</td> <td width="120px">必填</td> <td width="400px">金字塔节点（可以配置多个）</td>
    </tr>
       <tr>
        <td width="250px">pyid</td> <td width="120px">必填</td> <td width="400px">ID</td>
    </tr>
       <tr>
        <td width="250px">pyramidName</td> <td width="120px">必填</td> <td width="400px">名称
</td>
    </tr>
       <tr>
        <td width="250px">topLeft</td> <td width="120px">必填</td> <td width="400px">金字塔点坐标改为原点东向坐标，原点北向坐标</td>
    </tr>
       <tr>
        <td width="250px">scale</td> <td width="120px">必填</td> <td width="400px">分母比例尺</td>
    </tr>
       <tr>
        <td width="250px">imageWidth</td> <td width="120px">必填</td> <td width="400px">图片宽</td>
    </tr>
       <tr>
        <td width="250px">imageHeight</td> <td width="120px">必填</td> <td width="400px">图片高</td>
    </tr>
      <tr>
        <td width="250px">coordOrder</td> <td width="120px">必填</td> <td width="400px">坐标轴顺序 默认OGC标准（latlng）</td>
    </tr>
     <tr>
        <td width="250px">span</td> <td width="120px">必填</td> <td width="400px">顶层瓦片跨度</td>
    </tr>
    <tr>
        <td width="250px">resolution</td> <td width="120px">必填</td> <td width="400px">瓦片像素分辨率</td>
    </tr>
    </table>
    