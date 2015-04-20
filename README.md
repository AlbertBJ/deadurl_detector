# deadurl_detector
##要求:
设计一个系统，自动完成对于手机搜狐(http://m.sohu.com/ )系统可靠性的检测。具体要求：

1. 定时递归检测所有m.sohu.com域名的页面以及这些页面上的链接的可达性，即有没有出现不可访问情况。

2. m.sohu.com域名页面很多，从各个方面考虑性能优化。

3. 对于错误的链接记录到日志中，日志包括：连接，时间，错误状态等。

4. 考虑多线程的方式实现

##解决方案:
#### 获取链接
requests请求网页

re正则提取页面url


#### url过滤
url去重

url是否含有特点域名

url是否相似


##目前测试结果:
在特定域名(如:m.sohu.com)过滤情况下

如果判断`url是否相似`,一共能检测87个非相似链接

如果进行`url去重`,一共能检测4070个链接

