1、查看apk包名

2、修改inject.c文件中倒数第二行的包名target_pid = find_pid_of("包名");

3、最后一行确定libhello.so的文件位置，默认/data/libhello.so

4、使用ndk进行编译
ndk-build.cmd NDK_PROJECT_PATH=. NDK_APPLICATION_MK=Application.mk APP_BUILD_SCRIPT=Android.mk

5、使用adb将libhello.so、inject传到指定目录

6、chmod 777 libhell	o.so
   chmod 777 inject
7、另起一个终端 adb logcat

8、./inject  如果执行成功有日志输出

