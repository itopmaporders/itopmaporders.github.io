# 已经实现的功能

## 用户绘制完成后点击清空roi的功能

## 用户正在绘制roi点击清空roi的功能

## 用户正在绘制roi点击撤销roi的功能 

# Map.vue绘图逻辑

## 如何实现用户删除roi的功能？

  定义了一个userDrawnPolygons数组, 当每次用户绘制完一个roi时将此时的sketch(polygon)放入数组, 当用户点击删除时, source删除对应的polygon。

## 如何实现用户删除roi的同时删除对应的面积信息?

  用measureOverlayIndexArray记录下面积信息对应的overlay序号, 将其放置在数组中, 当用户执行删除roi时, 获取数组的最后一个index, 调用Map的removeOverlay函数删除对应的overlay。

## 用户在未绘制完一个roi时, 点击清除roi时没有删除对应的面积信息？

  添加一个用户判断用户是否正在绘制的标志, 如果不在绘制中，从userDrawnPolygons数组中取出一个roi删除, measureOverlayIndexArray先去除一个末尾元素, 再删除末尾元素对应的下标overlay，再删除这个元素。如果用户正在绘制状态, userDrawnPolygons不删除任何roi元素, measureOverlayIndexArray直接删除末尾元素对应的下标的overlay。

## 用户在未绘制完一个roi时, 点击撤销roi，撤销完成时，没有删除对应的面积信息？

  formatArea面积计算函数当面积为0时, 返回值为空。

## 用户清除地图上所有roi时, "单击以继续绘制多边形"没有完全删除?

 当userDrawnPolygons.length=1时，helpTooltipElement.innerHTML = '' ， helpTooltipElement = null; 即删除帮助信息。

