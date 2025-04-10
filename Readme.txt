基本介绍：
在open-vela基础上，制作了高级计算器支持以下功能：
1.基本四则运算：支持加、减、乘、除。
	运算支持double精度，仅显示有效数字，不显示多余的0
	如显示 1.5，而不是1.50000000

2.高级计算支持：
    取余（%）：仅限正整数间操作，错误输入返回 ERROR!。
    开平方（√）：负数输入将显示错误。
    小数支持：支持浮点输入与计算，防止重复输入多个小数点。
    删除功能（Del）：逐字符删除，支持纠正输入错误。
    清除（C）与结果计算（=）：
  C：一键清屏；
  =：计算表达式，语法错误输出"ERROR!"

3.结果后输入智能处理：
    在运算结果显示后，再次输入新数字会自动清屏；
    但如果输入的是运算符，则保留结果并继续运算。



原存放路径vela-opensource/apps/packages/demos/calculator/

常用指令：
# 清理构建产物
./build.sh vendor/openvela/boards/vela/configs/goldfish-armeabi-v7a-ap distclean -j$(nproc)

# 开始构建
./build.sh vendor/openvela/boards/vela/configs/goldfish-armeabi-v7a-ap -j$(nproc)

启动模拟器：
./emulator.sh vela

启动音乐播放器
calculator &

配置文件
./build.sh vendor/openvela/boards/vela/configs/goldfish-armeabi-v7a-ap menuconfig
