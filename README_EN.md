# extract-mdk-include-path-tool

#### Introduction
Extract the IncludePath and Define parameters from the mdk project file to quickly establish a vscode editing environment.

#### Software Architecture
Based on language: Python3

#### Installation tutorial

1. Just put the script in the project directory, you don't need to put it in the same directory of mdk-project-file, the script will automatically search the current path and sub-path.
2. Make sure that python3 has been installed on the machine, and python3.7 and above are recommended for the working environment. (The remaining versions are not tested) 

#### Instructions for use
> WINDOWS
1. In the script path, hold down the keyboard shift and click the right mouse button, and select `Open Powershell window here`.
2. Use the `python .\extract-mdk-include-path-tool.py` command to execute the python script.
3. The execution result will be displayed on Powershell, and it can be closed after execution. If the execution is successful, the script will create a new `IncludePath.txt` in the same path to store the output result.
4. Open the mdk project folder with vscode, use `ctrl+shift+p` to open the search box, and enter `Edit configurations`, select `C/C++:Edit configurations(JSON)`, it will be in the path of `.vscode` The `c_cpp_properties.json` file is automatically created, and the output results in `IncludePath.txt` are copied to `"includePath"` and `"defines"`, and you are done. 