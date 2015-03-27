四次元（原微次元） weiciyuan
=========
Sina Weibo Android App, require Android 4.1+, GPL v3 License

感谢开源的世界，只是原程序是android studio编译的，而在eclipse上会出现一些错误，
在此，我将自己在eclipse上调试成功后的源码再发上来，以便大家参考。

截图
--------------
<img width="30%" height="30%" src="http://img.blog.csdn.net/20150327200907773"/>


文档
--------------
https://github.com/qii/weiciyuan/wiki

Gradle 构建
--------------
- 版本
    - 最新 Android SDK
    - Gradle
- 环境变量
    - ANDROID_HOME
    - GRADLE_HOME，同时把bin放入path变量
- Android SDK 安装，都更新到最新
    - Android SDK Build-tools
    - Google Repository
    - Android Support Repository
    - Android Support Library
- 移除配置
    - 移除AndroidManifest.xml里面`com.crashlytics.ApiKey`和GlobalContext的`Crashlytics.start(this)`，以免影响四次元的崩溃统计数据
- 编译
    - `./gradlew assembleDebug`，编译好的apk在build/outputs/apk下面，默认用的是 debug.keystore 签名，可与Google Play上的正式版共存

