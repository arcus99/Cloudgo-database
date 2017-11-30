# Cloudgo-io

老师的课程博客地址：  [这里写链接内容](http://blog.csdn.net/pmlpml/article/details/78602290)

使用xorm来改写提供的代码

## 安装docker并建立数据库
 这里按照老师给出的教程完成即可：
 
 ![这里写图片描述](http://img.blog.csdn.net/20171130224210242?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![这里写图片描述](http://img.blog.csdn.net/20171130224257253?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

![这里写图片描述](http://img.blog.csdn.net/20171130224525379?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

这里建立数据库时要特别注意与老师给出的保持一致，否则后面插入数据等操作会报错。

## 插入数据

![这里写图片描述](http://img.blog.csdn.net/20171130225002849?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

此时监听窗口：

![这里写图片描述](http://img.blog.csdn.net/20171130225102012?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## 查询数据
 
 连续插入两个数据后：
 
 ![这里写图片描述](http://img.blog.csdn.net/20171130225030780?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

## 压力测试

首先是对sql：

![这里写图片描述](http://img.blog.csdn.net/20171130225209737?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

注意time per request为5.145ms
接着是对orm:

![这里写图片描述](http://img.blog.csdn.net/20171130225358205?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvbGVwcmVjaGF1bl8=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

注意time per request为8.111ms。

显然，虽然xorm形式上比较简洁，但是性能并没有sql好。