# ipkg-build
ipk build , opkg installation is supported

#### ipk打包方法
    1、按照指定路径存放对应的文件
    2、bash ipkg-build.sh 包名

##### SOURCE目录结构体
      --control;控制指令目录，最后压缩成control.tar.gz
        -control :记录包的信息
        -preinst :在包安装前，执行脚本
        -postinst：真实安装，在包解压后执行的脚本
        -prerm：预卸载，在包删除前执行的脚本
        -postrm：卸载后，需要执行的脚本
      --data;存放更新的文件目录
      --etc;需要拷贝etc目录下的脚本
      
##### opkg指令
    opkg install xxx.ipk 
    opkg remove xxx