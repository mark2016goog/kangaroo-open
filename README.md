# kangaroo-open
Automatically exported from code.google.com/p/kangaroo-open



kangaroo-open 是一个在线视频播放、直播平台。

kangaroo-open 是基于red5服务器和ffmpeg 视频格式转换，前端应用bootstrap3 集成用户账号管理，支付管理，视频管理，教师管理为一体的在线播放平台。满足广大教育机构、院校的管理在线视频播放、在线直播的需求。 适用于： * 1.在线影院 * 2.大、中、小学在线教育平台 * 3.培训机构在线教育平台 * 4.在线直播 * 5.基于付费的在线观看



##################################################################
新手部署说明

新手kangaroo-open 部署环境、相关事项

基本部署所需要软、硬件环境

1G 以上内存
1G以上硬盘空间
网络连通

>

Linux 或者 windows 操作系统服务器
服务器 安装有jdk （Java运行环境）
mysql 数据库（其他数据库也支持）
tomcat 6.0 以上
部署步骤

到 https://kangaroo-open.googlecode.com/svn/trunk/release 下载安装包 * 解压 两个rar 到tomcat 的webapps 目录 * 新建mysql 数据库kangaroo，这这个数据库上面运行 kangaroo-0.1.sql * 修改 application.properties 文件里面数据库连接等配置 * 修改 videoEngine 目录下面的red5-common.xml

<bean id="streamFilenameGenerator" class="com.shshilan.red5.CustomFilenameGenerator">

<property name="recordPath" value="E:\test\">

</property>

<property name="playbackPath" value="E:\test\">

</property>

</bean>

###############################################################
关于使用

本开源项目使用授权协议请参考项目详情

相关组件和jar包引用请参考组件jar 授权

视频图片logo 上传组件授权：http://www.hdfu.net
*
#############################################################

kangaroo-open 使用帮助

项目 kangaroo

修改application.properties 数据库配置和视频上传路径
默认帐号 admin/admin
*
项目 videoEngine

修改red5-common.xml 文件中的bean 为kangaroo 项目flv视频 存放路径

<bean id="streamFilenameGenerator" class="com.shshilan.red5.CustomFilenameGenerator">

<property name="recordPath" value="E:\test\"/>

<property name="playbackPath" value="E:\test\"/>

</bean>

tomcat 部署

如果是新手 可以将kangaroo 和 videoEngine同时部署的同个tomcat下面。 如果高手。。。。可以自己设计部署

###################################################################


