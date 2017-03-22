  # Cordova-WebApp-
  Cordova配置（WebApp混合开发环境）
    必备环境安装
    ====
    1.配置JDK环境
    -------
    ###  用的是1.8的版本，网上很多地方可以下载，这里不上链接了
    ###  在本地配置sdk变量，如图，点击桌面(计算机)->右键属性->高级系统设置->系统属性面板高级->点击环境变量->在下面框中的系统变量中新建

    这里写图片描述

        JAVA_HOME   D:\Program Files\Java\jdk1.8.0_112//这个路径根据你安装JDK的环境对应其地址
        PATH %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
        CLASSPATH .;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar
    2.下载Android SDK
    -------

        推荐国内的android-studio下载
        然后配置Android SDK环境，ANDROID_HOME定位到你的SDK文件夹的根目录

        ANDROID_HOME D://android-sdk-windows     //对应你的SDK文件夹的目录
        重启电脑

    Cordova安装
    =======

        下载Node.js

        节点官网

    2.在mac终端运行下面​​命令，输入密码安装cordova
    -------
        sudo npm install －g cordova
        这里写图片描述
        sudo是因为需要管理员权限，-g是全局安装
        cordvoa官网命令行帮助

    3.执行以下代码创建一个cordvoa应用
    -------
          cordova create hello com.example.hello HelloWorld
          第一个参数是文件目录，第二个参数是app id，第三个参数是显示的标题
          这里写图片描述

    IOS打包
    -------
    4.定位到hello目录文件夹，为项目安装平台模块
    -------
        cd hello
        cordova platform add ios
        这里写图片描述

    5.打开xcodeproj项目的文件位置双击打开，如已安装Xcode就绪顺利的打开项目了
    -------
        hello/platform/ios/
        这里写图片描述

    6.可以用编写html项目的IDE打开www下的index.html查看效果，在浏览器中打开即可
    -------
        这里写图片描述

    在Xcode中打开iOS模拟器如果看到以下效果说明环境已经搭建成功

        这里写图片描述

    ANDROID打包

    续前面三步

    4.定位到hello目录文件夹，为项目安装平台模块
    -------
        cd hello
        cordova platform add android
        生成APK文件

        cordova build android
    图片
    遇到这个问题就是gradle下载失败了，可以尝试拿图中的链接手动下载然后把它放到对应的系统文件下，如下，注意版本一定要对应上

        C:\Users\Administrator\.gradle\wrapper\dists\gradle-2.14.1-all\4cj8p00t3e5ni9e8iofg8ghvk7
        图片
        gradle-2.14.1-all.zip下载地址
        或者android-studio下载
    成功就会显示如下 apk的目录如下：
    图片

          项目路径\test\platforms\android\build\outputs\apk
