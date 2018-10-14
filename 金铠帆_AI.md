#第二次任务（AI方向）
## 10月12日（周五）及以前，百度搜索资料，但并没有找到具有可执行性的指导，任务一直停滞不前
## 10月13日，14日：
*一.用Google搜索搭建深度学习环境，根据教程按部就班的进行
*遇到的问题：
*1.在安装驱动时提示我我启用了“UFEI Secure Boot”,需要禁用，在禁用后安装完毕但在重启时跳出选择框时并没有选择“Change Boot Secure State”导致开机后在终端输入命令`nvidia-smi`显示找不到命令
*解决方法：重启后进入BIOS禁用了“UFEI Secure Boot”，启动后再次输入命令成功
*2.在安装CUDA过程中，无法打开.run文件
*解决方法：根据百度的指引对文件进行授权`chmod +x file`;执行文件`./file`
*3.执行.run文件时，显示X服务正在运行导致安装失败，在百度的指引下尝试关闭X服务器
*第一次尝试：输入`sudo /etc/init.d/lightdm stop`后，黑屏并出现一串看不懂的代码，不管敲什么键都没反应，以为玩崩了，无奈重启
*第二次尝试：输入`service gdm3 stop`，但却显示：
Failed to stop gdm3.service: Unit gdm3.service not loaded
*在多方百度无果后，搜索CUDA安装教程，终于找到解决方案，知道需要进入文本模式，但在输入帐号密码时因各种大小写错误或副键盘输入失败了数次，最后终于成功，重输入`sudo /etc/init.d/lightdm stop`后关闭了图形界面，开始安装
*4.在安装CUDA时因重复安装驱动导致失败
*解决方法：按照百度的指引在选择选项时进行调整，成功安装
*5.安装tensorflow后，打开python输入中`import tensorflow`失败，重新安装了一次tensorflow后解决问题，但一旦`source activate tensorflow`后打开python又无法成功导入tensorflow,最后也没有解决这个问题
*二.处理MINST
*由于本人的懒惰以及各种意外的发生（下载时因疏忽导致文件损坏），做完时间第一步时间就没了，很抱歉这一步进展几乎为0









