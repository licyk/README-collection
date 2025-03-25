# 简介
基于 [sd-webui-all-in-one/Installer](https://github.com/licyk/sd-webui-all-in-one/tree/dev?tab=readme-ov-file#installer) 全自动构建的整合包。

整合包使用 7z 格式进行打包，若 Windows 系统不支持解压该格式，请使用 [7-Zip](https://7-zip.org/) 或者其他支持解压 7z 格式的工具进行解压，解压完成后，首次使用需要双击运行`configure_env.bat`进行环境配置，保证 PowerShell 脚本能够正常运行。

PowerShell 脚本需要右键该脚本，选择`使用 PowerShell 运行`才可以运行。目录中包含多个 PowerShell 脚本用于启动和管理文件，根据需求运行脚本。

部分 WebUI 支持使用绘世启动器进行启动和管理，运行`hanamizuki.bat`即可启动绘世启动器，如果没有这个文件说明绘世启动器不支持启动和管理该 WebUI。


# 下载
## Stable Diffusion WebUI
![sd_webui](https://github.com/user-attachments/assets/02f40729-f816-49ea-b046-67c36501dcef)

**上手简单，操作方便，适合入门使用。**

支持 SD WebUI Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/sd_webui/sd_webui_licyk_v1.0.7z)**

### SD WebUI Installer 管理方式
- configure_env.bat：首次使用 SD WebUI Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 Stable Diffusion WebUI
- update.ps1：更新 Stable Diffusion WebUI
- update_extension.ps1：更新 Stable Diffusion WebUI 扩展
- download_models.ps1：下载模型
- switch_branch.ps1：切换 Stable Diffusion WebUI 分支
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：SD WebUI Installer 设置
- terminal.ps1：打开终端并进入 Stable Diffusion WebUI 环境
- activate.ps1：激活 Stable Diffusion WebUI 环境
- launch_stable_diffusion_webui_installer.ps1：运行 SD WebUI Installer 并执行安装任务

SD WebUI Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/stable_diffusion_webui_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## Stable Diffusion WebUI Forge
![sd_webui_forge](https://github.com/user-attachments/assets/a9b92d5d-320f-4724-9194-422120bc5712)

**基于 Stable Diffusion WebUI，有更强的显存优化，多了 FLUX 模型支持。**

支持 SD WebUI Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/sd_webui_forge/sd_webui_forge_licyk_v1.0.7z)**

### SD WebUI Installer 管理方式
- configure_env.bat：首次使用 SD WebUI Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 Stable Diffusion WebUI Forge
- update.ps1：更新 Stable Diffusion WebUI Forge
- update_extension.ps1：更新 Stable Diffusion WebUI Forge 扩展
- download_models.ps1：下载模型
- switch_branch.ps1：切换 Stable Diffusion WebUI Forge 分支
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：SD WebUI Installer 设置
- terminal.ps1：打开终端并进入 Stable Diffusion WebUI Forge 环境
- activate.ps1：激活 Stable Diffusion WebUI Forge 环境
- launch_stable_diffusion_webui_installer.ps1：运行 SD WebUI Installer 并执行安装任务

详细 SD WebUI Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/stable_diffusion_webui_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## Stable Diffusion WebUI reForge
![sd_webui_reforge](https://github.com/user-attachments/assets/c177586c-cedb-47b1-86d8-8ece231eedd0)

**基于旧版 Stable Diffusion WebUI Forge 开发，插件兼容性比 Stable Diffusion WebUI Forge 好一点。**

支持 SD WebUI Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/sd_webui_reforge/sd_webui_reforge_licyk_v1.0.7z)**

### SD WebUI Installer 管理方式
- configure_env.bat：首次使用 SD WebUI Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 Stable Diffusion WebUI reForge
- update.ps1：更新 Stable Diffusion WebUI reForge
- update_extension.ps1：更新 Stable Diffusion WebUI reForge 扩展
- download_models.ps1：下载模型
- switch_branch.ps1：切换 Stable Diffusion WebUI reForge 分支
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：SD WebUI Installer 设置
- terminal.ps1：打开终端并进入 Stable Diffusion WebUI reForge 环境
- activate.ps1：激活 Stable Diffusion WebUI reForge 环境
- launch_stable_diffusion_webui_installer.ps1：运行 SD WebUI Installer 并执行安装任务

详细 SD WebUI Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/stable_diffusion_webui_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## ComfyUI
![comfyui](https://github.com/user-attachments/assets/6cd98e59-e39a-4e97-bdf8-17e79e758f0c)

**流程高度自定义，可玩性高，显存优化强，支持的模型丰富，~~除了某些插件喜欢冲突弄坏环境~~。**

支持 ComfyUI Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/comfyui/comfyui_licyk_v1.0.7z)**

### ComfyUI Installer 管理方式
- configure_env.bat：首次使用 ComfyUI Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 ComfyUI
- update.ps1：更新 ComfyUI
- update_node.ps1：更新 ComfyUI 扩展
- download_models.ps1：下载模型
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：ComfyUI Installer 设置
- terminal.ps1：打开终端并进入 ComfyUI 环境
- activate.ps1：激活 ComfyUI 环境
- launch_comfyui_installer.ps1：运行 ComfyUI Installer 并执行安装任务

详细 ComfyUI Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/comfyui_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## Fooocus
![fooocus](https://github.com/user-attachments/assets/71c11744-45a3-4dca-a34a-c69e70e06729)

**化繁为简，更专注于提示词书写。**

支持 Fooocus Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/fooocus/fooocus_licyk_v1.0.7z)**

### Fooocus Installer 管理方式
- configure_env.bat：首次使用 Fooocus Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 Fooocus
- update.ps1：更新 Fooocus
- download_models.ps1：下载模型
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：Fooocus Installer 设置
- terminal.ps1：打开终端并进入 Fooocus 环境
- activate.ps1：激活 Fooocus 环境
- launch_fooocus_installer.ps1：运行 Fooocus Installer 并执行安装任务

详细 Fooocus Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/fooocus_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## InvokeAI
![invokeai](https://github.com/user-attachments/assets/d2511de0-05c7-40c4-9c88-2d3a0417a6ec)

**拥有最强大的画布系统，更适合作为辅助绘画工具。**

仅支持 InvokeAI Installer 进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/invokeai/invokeai_licyk_v1.0.7z)**

### InvokeAI Installer 管理方式
- configure_env.bat：首次使用 InvokeAI Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 InvokeAI
- update.ps1：更新 InvokeAI
- update_node.ps1：更新 InvokeAI 扩展
- download_models.ps1：下载模型
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：InvokeAI Installer 设置
- terminal.ps1：打开终端并进入 InvokeAI 环境
- activate.ps1：激活 InvokeAI 环境
- launch_invokeai_installer.ps1：运行 InvokeAI Installer 并执行安装任务

详细 InvokeAI Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/invokeai_installer.md


## SD-Trainer
![sd_trainer](https://github.com/user-attachments/assets/0c0a7921-f1a0-4409-a518-ea1b0be5e385)

**训练模型如此简单。**

支持 SD-Trainer Installer / 绘世启动器进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/sd_trainer/sd_trainer_licyk_v1.0.7z)**

### SD-Trainer Installer 管理方式
- configure_env.bat：首次使用 SD-Trainer Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 SD-Trainer
- update.ps1：更新 SD-Trainer
- download_models.ps1：下载模型
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：SD-Trainer Installer 设置
- terminal.ps1：打开终端并进入 SD-Trainer 环境
- activate.ps1：激活 SD-Trainer 环境
- launch_fooocus_installer.ps1：运行 SD-Trainer Installer 并执行安装任务

详细 SD-Trainer Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/stable_diffusion_webui_installer.md

### 绘世启动器管理方式
- hanamizuki.bat：启动绘世启动器

详细绘世启动器使用说明可阅读：https://sdnote.netlify.app/sd_launcher


## Kohya GUI
![kohya_gui](https://github.com/user-attachments/assets/06cd3001-5d15-4b3e-aeba-3579f3159a48)

**支持训练更多种类的模型，不过操作麻烦一点。**

仅支持 SD-Trainer Installer 进行管理。

## **[>>>整合包下载<<<](https://modelscope.cn/models/licyks/sdnote/resolve/master/portable/stable/kohya_gui/kohya_gui_licyk_v1.0.7z)**

### SD-Trainer Installer 管理方式
- configure_env.bat：首次使用 SD-Trainer Installer 需要运行一次，保证能正常运行
- launch.ps1：启动 Kohya GUI
- update.ps1：更新 Kohya GUI
- download_models.ps1：下载模型
- reinstall_pytorch.ps1：切换 / 重装 PyTorch
- settings.ps1：SD-Trainer Installer 设置
- terminal.ps1：打开终端并进入 Kohya GUI 环境
- activate.ps1：激活 Kohya GUI 环境
- launch_fooocus_installer.ps1：运行 SD-Trainer Installer 并执行安装任务

详细 SD-Trainer Installer 使用说明可阅读：https://github.com/licyk/sd-webui-all-in-one/blob/dev/stable_diffusion_webui_installer.md


## 所有版本
整合包存储在 [HuggingFace](https://huggingface.co/licyk/sdnote/tree/main/portable) / [ModelScope](https://modelscope.cn/models/licyks/sdnote/files) 中。

合集链接：https://licyk.github.io/t/sd_portable

>[!NOTE]
>1. 整合包分为 Stable 和 Nightly 版本，Nightly 版本是未经测试的版本，并且使用日期进行命名，如`comfyui_licyk_20250322_nightly`，`comfyui`代表该整合包为 ComfyUI 整合包，`20250322`代表整合包在 2025.3.22 时进行构建。虽然 Nightly 版本未经过测试，但通常是可以使用的。
>2. Stable 版本为 Nightly 版本中经过测试的版本，但因为作者时间问题，Stable 版本并不会经常更新。
>3. 使用 [sd-webui-all-in-one/Installer](https://github.com/licyk/sd-webui-all-in-one/tree/dev?tab=readme-ov-file#installer) 安装的 WebUI 和使用整合包没什么区别，因为这些整合包就是使用 [sd-webui-all-in-one/Installer](https://github.com/licyk/sd-webui-all-in-one/tree/dev?tab=readme-ov-file#installer) 进行构建的。
>4. 更新 WebUI / ComfyUI / ... 通常情况下不需要重新下载整合包，使用 [sd-webui-all-in-one/Installer](https://github.com/licyk/sd-webui-all-in-one/tree/dev?tab=readme-ov-file#installer) 或者绘世启动器即可对 WebUI / ComfyUI / ... 进行更新。
