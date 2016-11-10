# Servlet生命周期与工作原理
### Servlet生命周期分为三个阶段:
> 1.初始化阶段 调用init()方法
> 2.响应客户请求阶段   调用service()方法
> 3.终止阶段   调用destroy()方法

### Servlet初始化阶段
在下列时刻Servlet容器装载Servlet:
> 1.Servlet容器启动时自动装载某些Servlet，实现它只需要在web.xml文件中<Servlet></Servlet>之间添加如下代码:
```
<loadon-startup>1</loadon-startup>
```
> 2.在Servlet容器启动后，客户首次向Servlet发送请求
> 3.Servlet类文件被更新后，重新装载Servlet
Servlet被装载后，Servlet容器创建一个Servlet实例并且调用Servlet的init()方法进行初始化。在Servlet的整个生命周期内，init()方法只能呢个被调用一次。
