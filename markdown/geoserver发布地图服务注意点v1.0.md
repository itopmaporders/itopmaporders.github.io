# geoserver发布地图服务注意点v1.0

- 发布PNG格式的地图

选择栅格数据源下的**ImageMosaic格式**发布

- 连接参数(指选择对应数据源文件)

**文件应当先上传至服务器**, 无法通过在线传输形式上传(windows使用远程桌面和共享文件夹的方式)

- SRS处理

选择**强制声明**

- 瓦片加载方式

最新版本geoserver生成瓦片直接加载至内存中, 可以自定义瓦片生成路径

- 缩放级别的设置

根据数据本身特点而定, 级别设置过高产生的级别属于假的缩放级别, 会导致生产瓦片时间长, cpu占用率高等问题

***

**相关链接**

[如何用geoserver发布shp文件]()[第三课 使用GeoServer发布shapefile文件_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1tK4y1g7dW/?spm_id_from=333.788)

[如何用geoserver发布tiff文件]([第四课 使用GeoServer发布GeoTIFF影像_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1nX4y1P7s7/?spm_id_from=333.788))

[如何生产瓦片]([第七课 使用geoserver生产wmts瓦片_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1kT4y197h6/?spm_id_from=333.788))

[修改图层样式]([qgis修改geoserver图层样式_yuqizzp的博客-CSDN博客_geoserver修改样式](https://blog.csdn.net/qq_45697944/article/details/122187152))

