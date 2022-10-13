# Geoserver相关设置区分

- workspace

两个不同的layer可以具有相同的名称，只要它们属于不同的workspace（例如，sf:states和topp:state）。

添加一个workspace时通常需要提供两个参数：一是名称，不能超过10个字符，也不能包含空格;二是url，url不必指向一个实际的网络位置，但需要被唯一区分。