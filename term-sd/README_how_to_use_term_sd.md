# Tern-SD使用教程  

- [Tern-SD使用教程](#tern-sd使用教程)
  - [Term-SD的初始化](#term-sd的初始化)
  - [Term-SD的主界面介绍](#term-sd的主界面介绍)
  - [Term-SD配置功能](#term-sd配置功能)
    - [Term-SD](#term-sd)
  - [Term-SD安装功能](#term-sd安装功能)
  - [Term-SD管理功能](#term-sd管理功能)
  - [Term-SD额外功能](#term-sd额外功能)

## Term-SD的初始化

Term-SD在下载好后，只会有一个基础的配置脚本“term-sd.sh”，当运行这个配置脚本时，Term-SD会检测运行所需依赖。当检测到缺少依赖时，Term-SD会提示用户需要去安装的依赖，并自动退出，这时候需要用户检查这些依赖是否安装，并且把缺失的依赖装上  
当检测到依赖都安装时，脚本会提示用户安装Term-SD的完整组件  

这时候输入“y”即可进行下载  

在下载前。Term-SD会询问选择哪个下载源  
总共有以下下载源：  
1、github源  
2、gitee源  
3、gitlab源  
4、代理源(使用代理站连接github源)  

一般情况选择任意一种都可以进行下载，但是如果用户无法在浏览器访问github官网，则不建议选第一个  
如果下载失败，Term-SD将会自动退出，这时再次运行Term-SD重新下载，选择其他下载源  
当成功下载时，Term-SD将会自动初始化模块，并启动  

## Term-SD的主界面介绍

Term-SD在成功启动后，首先显示的是各个组件的版本信息，选择确定后就进入Term-SD的主界面  
主界面有以下功能  
1、Term-SD更新管理：管理，修复Term-SD的更新  
2、AUTOMATIC1111-stable-diffusion-webui管理：包含各种AUTOMATIC1111-stable-diffusion-webui的管理功能  
3、ComfyUI管理：包含各种ComfyUI的管理功能  
4、InvokeAI管理：包含各种InvokeAI的管理功能  
5、lora-scripts管理：包含各种lora-scripts的管理功能  
6、venv虚拟环境设置：配置Term-SD在安装。管理ai时是否使用虚拟环境，建议保持启用（默认）  
7、pip镜像源设置：配置pip在安装python软件包时使用的镜像源，减少pip直接连接官方镜像源时出现下载慢，连接不稳定的问题  
8、pip缓存清理：清理pip在下载python软件包后产生的缓存  
9、代理设置：配置
10、空间占用分析
11、帮助
12、退出

## Term-SD配置功能

### Term-SD

## Term-SD安装功能

## Term-SD管理功能

## Term-SD额外功能