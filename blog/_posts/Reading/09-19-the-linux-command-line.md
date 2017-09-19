##the linux command line

| 目录 | comment |
|---|---|
|/bin |包含系统启动和运行所必须的二进制程序。|
|/boot|包含 Linux 内核|
|/etc|这个目录包含所有系统层面的配置文件。它也包含一系列 的 shell 脚本|
|/sbin|这个目录包含“系统”二进制文件。|


I/O 重定向允许我们可以更改输出走向和输入来向。一般地，输出送到屏幕，输入来自键 盘，但是通过 I/O 重定向，我们可以改变输入输出方向。
* 重定向标准输出
        ls -l ~/Workspace > ls-output.txt
* 重定向标准输入
        cat movie.mpeg.0* > movie.mpeg

grep全称是Global Regular Expression Print