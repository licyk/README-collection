# Tern-SD使用教程  

##  <目录>

- [Tern-SD使用教程](#tern-sd使用教程)
  - [\<目录\>](#目录)
  - [Term-SD的初始化](#term-sd的初始化)
  - [Term-SD的主界面介绍](#term-sd的主界面介绍)
  - [Term-SD配置功能](#term-sd配置功能)
    - [Term-SD更新管理](#term-sd更新管理)
    - [pip镜像源设置](#pip镜像源设置)
    - [代理设置](#代理设置)
  - [使用Term-SD安装ai软件前的准备](#使用term-sd安装ai软件前的准备)
  - [Term-SD安装功能](#term-sd安装功能)
    - [AUTOMATIC1111-stable-diffusion-webui安装](#automatic1111-stable-diffusion-webui安装)
      - [1、代理选项](#1代理选项)
      - [2、pytorch版本选择](#2pytorch版本选择)
      - [3、pip安装模式选择](#3pip安装模式选择)
      - [4、插件选择](#4插件选择)
      - [5、安装确认](#5安装确认)
    - [ComfyUI安装](#comfyui安装)
      - [1、代理选项](#1代理选项-1)
      - [2、pytorch版本选择](#2pytorch版本选择-1)
      - [3、pip安装模式选择](#3pip安装模式选择-1)
      - [4、插件安装](#4插件安装)
      - [5、自定义节点安装](#5自定义节点安装)
      - [6、安装确认](#6安装确认)
    - [InvokeAI安装](#invokeai安装)
      - [1、代理选项](#1代理选项-2)
      - [2、pytorch版本选择](#2pytorch版本选择-2)
      - [3、pip安装模式选择](#3pip安装模式选择-2)
      - [4、安装确认](#4安装确认)
    - [lora-scripts安装](#lora-scripts安装)
      - [1、代理选项](#1代理选项-3)
      - [2、pytorch版本选择](#2pytorch版本选择-3)
      - [3、pip安装模式选择](#3pip安装模式选择-3)
      - [4、安装确认](#4安装确认-1)
  - [Term-SD管理功能](#term-sd管理功能)
    - [1、更新](#1更新)
    - [2、卸载](#2卸载)
    - [3、修复更新](#3修复更新)
    - [4、自定义节点管理](#4自定义节点管理)
    - [5、插件管理](#5插件管理)
    - [6、切换版本](#6切换版本)
    - [7、更新源切换](#7更新源切换)
    - [8、启动](#8启动)
    - [9、更新依赖](#9更新依赖)
    - [10、重新安装](#10重新安装)
    - [11、重新安装pytorch](#11重新安装pytorch)
    - [12、重新生成venv虚拟环境](#12重新生成venv虚拟环境)
    - [13、重新构建venv虚拟环境](#13重新构建venv虚拟环境)
  - [Term-SD额外功能](#term-sd额外功能)
    - [扩展脚本](#扩展脚本)
    - [启动参数](#启动参数)
      - [启动参数的使用方法](#启动参数的使用方法)
      - [启动参数的功能解析](#启动参数的功能解析)
  - [绘世启动器的使用](#绘世启动器的使用)

***

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
主界面有以下选项  
1、Term-SD更新管理：管理，修复Term-SD的更新  
2、AUTOMATIC1111-stable-diffusion-webui管理：包含各种AUTOMATIC1111-stable-diffusion-webui的管理功能  
3、ComfyUI管理：包含各种ComfyUI的管理功能  
4、InvokeAI管理：包含各种InvokeAI的管理功能  
5、lora-scripts管理：包含各种lora-scripts的管理功能  
6、venv虚拟环境设置：配置Term-SD在安装。管理ai时是否使用虚拟环境，建议保持启用（默认）  
7、pip镜像源设置：配置pip在安装python软件包时使用的镜像源，减少pip直接连接官方镜像源时出现下载慢，连接不稳定的问题  
8、pip缓存清理：清理pip在下载python软件包后产生的缓存  
9、代理设置：配置网络代理，解决无法连接部分下载源导致下载失败的问题。一般在代理软件无法为Term-SD进行网络代理时使用（在使用没有TUN模式或者驱动模式的代理软件中，终端环境并不会自动使用代理，使运行在终端的Term-SD和ai软件无法使用到代理环境，导致部分下载源下载失败）  
10、空间占用分析：显示各个ai软件所占用的空间和当前目录剩余空间  
11、帮助：Term-SD的各种帮助文档  

## Term-SD配置功能

### Term-SD更新管理

该功能用于对Term-SD自身的更新等进行管理，共有以下选项  
1、更新：这个不用多说  
2、切换更新源：Term-SD有多个下载源，用于解决某些更新源更新慢或者无法更新的问题，一般来说github源的版本变化较快，其他源的版本变化会有延后（大约延迟一天）  
3、切换分支：Term-SD总共有两个分支，main和dev，一般不需要切换  
4、修复更新：当用户手动修改Term-SD的文件后，在更新Term-SD时就容易出现更新失败的问题，该功能可修复该问题  

### pip镜像源设置

该功能用于对pip的下载源进行修改，共有以下选项 
1、官方源：将pip的下载源切换成官方源，但可能会导致下载慢或者下载失败的问题  
2、国内镜像源：将pip的下载源切换成国内镜像源，解决官方源下载慢或者下载失败的问题，推荐选择  
3、删除镜像源配置：将pip的下载源设置清除  

### 代理设置

该功能为了设置下载时使用的网络代理，解决部分下载源下载失败的问题，共有以下选项  
1、http：设置http协议的代理  
2、socks：设置socks协议的代理  
3、socks5：设置socks5协议的代理  
4、删除代理参数：将设置的代理参数删除  

设置代理时，用户需要选择代理协议，具体使用什么代理协议取决于所使用的代理软件

## 使用Term-SD安装ai软件前的准备

安装前，我们需要做一些准备  
1、设置pip镜像源  
2、设置代理（没有一个质量比较好的代理时就不要设置了）  

首先我们在Term-SD主界面选择“pip镜像源设置”，进入后可选择“官方源”和“国内镜像源”，这里非常推荐设置为“国内镜像源”（如果之前为pip设置镜像源，包括pypi源、pytorch源，则不需要再次设置“pip镜像源”）  
如果用户有代理软件，并且代理的速度和稳定性较好，则先判断代理软件的代理工作模式，一般有TUN模式或者驱动模式的就不需要设置代理，因为这两种代理模式可以让终端环境走代理（其余模式不行）  
但是TUN模式或者驱动模式会让所有流量走代理，而Term-SD在安装ai软件的过程中只有部分下载源需要代理，这将会造成代理流量的浪费。所以，如果代理软件有其他代理模式，最好选这些的，并查看代理软件的代理协议、ip和端口，然后在Term-SD主界面的“代理设置”里选择代理协议，填入ip和端口，回车保存，这样Term-SD就可以决定哪些流量需要走代理  
如果代理没有TUN模式或者驱动模式，则查看代理软件的代理协议、ip和端口，然后在Term-SD主界面的“代理设置”里选择代理协议，填入ip和端口，回车保存  

>在不使用代理后，需要在“代理设置”里删除代理参数，防止在代理软件关闭后出现Term-SD无法访问网络的问题  

进行上面的步骤后就可以进行ai软件的安装

## Term-SD安装功能


Term-SD支持AUTOMATIC1111-stable-diffusion-webui，ComfyUI，InvokeAI，lora-scripts，在Term-SD的主界面对应下面的选项  
1、AUTOMATIC1111-stable-diffusion-webui管理  
2、ComfyUI管理  
3、InvokeAI管理  
4、lora-scripts管理  

需要安装哪一种就选择哪一个管理选项

### AUTOMATIC1111-stable-diffusion-webui安装

>AUTOMATIC1111-stable-diffusion-webui是一款功能丰富，社区资源丰富的ai绘画软件，支持扩展

选中AUTOMATIC1111-stable-diffusion-webui管理后，Term-SD会检测该ai是否安装，如果没有安装，Term-SD会提示用户是否进行安装  
选择“是”之后，Term-SD会进入安装准备选项  

#### 1、代理选项
第一个是代理选项，共有以下选项    
1、启用pip镜像源：Term-SD调用pip下载python软件包时使用国内镜像源进行下载  
2、启用github代理：Term-SD从github克隆源代码时使用github代理镜像站进行克隆  
3、huggingface独占代理：Term-SD安装ai软件的过程仅为huggingface下载源启用代理，减少代理流量的消耗  
4、强制使用pip：强制使用pip安装python软件包，一般只有在禁用venv虚拟环境后才需要启用    

一般这些选项保持默认即可  

>强制使用pip一般不需要启用，该选项向pip传达--break-system-packages参数进行安装，忽略系统的警告，参考https://stackoverflow.com/questions/75602063/pip-install-r-requirements-txt-is-failing-this-environment-is-externally-mana

#### 2、pytorch版本选择
第二个是pytorch版本的选择界面，有以下版本组合  
1、Torch+xformers  
2、Torch  
3、Torch 2.0.0+Torch-Directml  
4、Torch 2.0.1+CPU  
5、Torch 2.0.1+RoCM 5.4.2  
6、Torch 1.12.1(CUDA11.3)+xFormers 0.014  
7、Torch 1.13.1(CUDA11.7)+xFormers 0.016  
8、Torch 2.0.0(CUDA11.8)+xFormers 0.018  
9、Torch 2.0.1(CUDA11.8)+xFormers 0.021  
10、Torch 2.1.0(CUDA12.1)+xFormers 0.022  

选择版本时需要根据系统类型和显卡选择  
在Windows系统中，Nvidia显卡选择Torch（CUDA）+xformers的版本，AMD显卡和Intel显卡选择Torch+Torch-Directml的版本  
在Linux系统中，Nvidia显卡选择Torch（CUDA）+xformers的版本，AMD显卡选择Torch+Rocm的版本，Intel显卡选择Torch版本  
在MacOS系统中，选择Torch版本  
如果想要使用CPU进行跑图，选择Torch+CPU的版本  

#### 3、pip安装模式选择
第三个是pip包管理器的安装模式选择，共有2种模式  
1、常规安装(setup.py)：使用传统方式进行安装，默认使用二进制软件包进行安装，速度较快  
2、标准构建安装(--use-pep517)：使用标准编译安装，使用源码编译成二进制软件包再进行安装，耗时比较久，但可以解决一些python软件包安装失败的问题  

一般使用常规安装(setup.py)就行  

#### 4、插件选择  
第四个是插件选择，Term-SD默认已经勾选一些比较有用的插件，可以根据个人需求进行选择  

#### 5、安装确认
最后一个是安装确认，选择“是”开始安装  
安装时间根据网络速度和电脑性能决定  

### ComfyUI安装

>ComfyUI是一款节点式操作的ai绘画软件，上手难度较高，但是节点赋予ComfyUI更高的操作上限，且支持将节点工作流保存成文件，支持扩展。同时ComfyUI让用户更好的理解ai绘画的工作原理

选中ComfyUI管理后，Term-SD会检测该ai是否安装，如果没有安装，Term-SD会提示用户是否进行安装  
选择“是”之后，Term-SD会进入安装准备选项  

#### 1、代理选项
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 2、pytorch版本选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 3、pip安装模式选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 4、插件安装
第四个是插件选择，Term-SD默认已经勾选一些比较有用的插件，可以根据个人需求进行选择  

#### 5、自定义节点安装
第五个是自定义节点选择，Term-SD默认已经勾选一些比较有用的插件，可以根据个人需求进行选择  

#### 6、安装确认
最后一个是安装确认，选择“是”开始安装  
安装时间根据网络速度和电脑性能决定  

>在安装结束后，如果有安装插件/自定义节点的，需要在插件管理/自定义节点管理里运行安装全部插件依赖/安装全部自定义节点依赖，保证插件/自定义节点的正常运行（因为ComfyUI并没有AUTOMATIC1111-stable-diffusion-webui自动为插件安装依赖的功能）

### InvokeAI安装

>InvokeAI是一款操作界面简单的ai绘画软件，功能较少，但拥有特色功能“统一画布”，用户可以在画布上不断扩展图片的大小

选中InvokeAI管理后，Term-SD会检测该ai是否安装，如果没有安装，Term-SD会提示用户是否进行安装  
选择“是”之后，Term-SD会进入安装准备选项  

#### 1、代理选项
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 2、pytorch版本选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 3、pip安装模式选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 4、安装确认
最后一个是安装确认，选择“是”开始安装  
安装时间根据网络速度和电脑性能决定  

### lora-scripts安装

>lora-scripts是一款ai模型训练工具，支持训练lora模型。dreambooth模型

选中lora-scripts管理后，Term-SD会检测该ai是否安装，如果没有安装，Term-SD会提示用户是否进行安装  
选择“是”之后，Term-SD会进入安装准备选项  

#### 1、代理选项
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 2、pytorch版本选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 3、pip安装模式选择
和AUTOMATIC1111-stable-diffusion-webui的选择方法相同  

#### 4、安装确认
最后一个是安装确认，选择“是”开始安装  
安装时间根据网络速度和电脑性能决定  

## Term-SD管理功能

在4个ai管理界面中，包含一些功能对ai进行管理  

### 1、更新
这个不用解释了吧  

### 2、卸载
字面意思  

### 3、修复更新
修复一些版本问题导致更新失败的问题  

### 4、自定义节点管理
管理自定义节点，包含以下功能  
>仅限ComfyUI

1、安装：使用git安装自定义节点  
2、管理：对自定义节点进行管理，提供了一个自定义节点列表浏览器来选择自定义节点  
3、更新全部自定义节点：一键更新全部自定义节点    
4、安装全部自定义节点依赖：一键将所有自定义节点需要的依赖进行安装（仅限ComfyUI）  

### 5、插件管理
管理插件，包含以下功能

1、安装：使用git安装插件  
2、管理：对插件进行管理，提供了一个插件列表浏览器来选择插件  
3、更新全部插件：一键更新全部插件    
4、安装全部插件依赖：一键将所有插件需要的依赖进行安装（仅限ComfyUI）  

### 6、切换版本
根据版本hash值进行版本切换

### 7、更新源切换
使用github更新源的可以切换为github代理源加速下载，或者恢复github更新源

### 8、启动
启动ai软件  
在AUTOMATIC1111-stable-diffusion-webui、ComfyUI、InvokeAI中可以选择启动参数

### 9、更新依赖
更新ai软件的依赖，可用于解决ai软件的部分依赖版本太旧导致运行报错，一般用不上

### 10、重新安装
重新执行ai软件的安装过程

### 11、重新安装pytorch
这个功能用于切换pytorch的版本

### 12、重新生成venv虚拟环境
重新生成ai软件使用的venv虚拟环境，一般在移动ai软件的位置，ai软件运行出现问题后才用（不过这个功能不一定解决问题）

### 13、重新构建venv虚拟环境
重新构建ai软件使用的venv虚拟环境，一般用在移动ai软件的位置后、ai软件运行出现报错（有一些时候是python依赖库出现了版本错误或者损坏，或者装了一些插件后出现问题，删除插件后问题依然没有解决）、安装ai软件前禁用了venv虚拟环境，安装后启用了venv虚拟环境，需要修复虚拟环境  
这个功能一般不需要用，除非解决不了一些python库报错问题（因为该功能需要消耗比较长的时间）

## Term-SD额外功能

### 扩展脚本
Term-SD包含了一些扩展脚本，扩充Term-SD的功能  
sd-webui-extension：安装AUTOMATIC1111-stable-diffusion-webui的插件  
comfyui-extension：安装ComfyUI的插件  

### 启动参数

#### 启动参数的使用方法  
```bash
./term-sd.sh [--help] [--extra] [--multi-threaded-download] [--enable-auto-update] [--disable-auto-update] [--reinstall-term-sd] [--remove-term-sd] [--test-proxy] [--quick-cmd] [--set-python-path] [--set-pip-path] [--unset-python-path] [--unset-pip-path]
```

>中括号“[]”仅用来展示，在使用的时候不要输入进去
当使用--quick-cmd安装了快捷命令，可将“./term-sd.sh”替换成“termsd”或者“tsd”

#### 启动参数的功能解析
1、help  
显示启动参数帮助

2、extra  
启动扩展脚本显示界面，选中其中一个启动脚本后即可启动

3、multi-threaded-download  
安装过程中启用多线程下载模型，在调用aria2下载模型时设置下载线程为8

4、enable-auto-update  
启动Term-SD自动检查更新功能。启用后在启动Term-SD时将会检查一次更新，如果有更新则会提醒用户是否进行更新（该功能的触发时间间隔为一个小时）

5、disable-auto-update  
禁用Term-SD自动检查更新功能  

6、reinstall-term-sd  
重新安装Term-SD。Term-SD会提示用户如何重新安装，根据提示操作即可  

7、remove-term-sd  
卸载Term-SD，该功能将会删除Term-SD自身的所有组件和快捷启动命令，只保留已经安装的ai软件

8、test-proxy  
测试网络环境,用于测试代理是否可用。该功能将会测试网络连接是否正常，并测试google能否访问  

9、quick-cmd  
将Term-SD快捷启动指令安装到shell中,在shell中直接输入“termsd”或者“tsd”即可启动Term-SD，且不需要在Term-SD所在目录就能启动Term-SD（用“./term-sd.sh”命令启动还是需要在Term-SD所在目录里才能用）。该功能会提示用户选择安装快捷启动命令还是删除快捷启动命令，根据提示进行操作

10、set-python-path  
手动指定python解释器路径

11、set-pip-path  
手动指定pip路径

12、unset-python-path  
删除自定义python解释器路径配置

13、unset-pip-path  
删除自定义pip解释器路径配置

## 绘世启动器的使用
目前绘世启动器支持启动AUTOMATIC1111-stable-diffusion-webui、ComfyUI（目前Term-SD部署出来的ComfyUI无法正常启动，后续应该会有优化）。使用Term-SD部署AUTOMATIC1111-stable-diffusion-webui或者ComfyUI后，将绘世启动器放入stable-diffusion-webui文件夹或者ComfyUI文件夹后就可以使用绘世启动器启动对应的ai软件了