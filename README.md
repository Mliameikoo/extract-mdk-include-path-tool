# extract-mdk-include-path-tool

#### 介绍
从mdk工程文件中提取出IncludePath和Define参数，以快速建立vscode编辑环境。

#### 软件架构
基于语言：Python3

#### 安装教程

1.  将该脚本放在工程目录下即可，不需要刻意放到mdk-project-file同一目录下，脚本会自动搜索当前所在路径与子路径。
2.  确保机器已经安装好了python3，工作环境推荐python3.7及以上版本。（其余版本未测试）

#### 使用说明
> WINDOWS
1.  在脚本路径下按住键盘shift并单击鼠标右键，选择`在此处打开Powershell窗口`。
2.  使用`python .\extract-mdk-include-path-tool.py`命令执行python脚本。
3.  Powershell上会显示执行结果，执行完毕后关闭即可。若执行成功，脚本会在同一路径下新建一个`IncludePath.txt`，以存放输出结果。
4.  用vscode打开mdk工程文件夹，使用`ctrl+shift+p`打开搜索框，并输入`Edit configurations`，选择`C/C++:Edit configurations(JSON)`，会在`.vscode`路径中自动创建`c_cpp_properties.json`文件，将`IncludePath.txt`中的输出结果分别复制到`"includePath"`和`"defines"`中即可大功告成。
