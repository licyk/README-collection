# 在 Linux 上使用 Python 版本管理器安装 Python

这里介绍使用不同的 Python 版本管理器安装指定版本的 Python，以下使用 Linux mint （基于 Debian）进行演示。


## 目录

- [在 Linux 上使用 Python 版本管理器安装 Python](#在-linux-上使用-python-版本管理器安装-python)
  - [目录](#目录)
  - [安装 Python](#安装-python)
    - [使用 Pyenv](#使用-pyenv)
    - [使用 MicroMamba](#使用-micromamba)
    - [使用 MiniConda](#使用-miniconda)
  - [为 Term-SD 指定 Python 路径](#为-term-sd-指定-python-路径)


## 安装 Python

### 使用 Pyenv
1. 安装 Pyenv 所需的依赖

```bash
sudo apt update; sudo apt install build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev curl git \
libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev -y
```

2. 安装 Pyenv

```bash
curl https://pyenv.run | bash
```

如果 Pyenv 安装成功，Pyenv 安装程序会输出下面的内容。

```
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   270  100   270    0     0     79      0  0:00:03  0:00:03 --:--:--    79
正克隆到 '/home/licyk/.pyenv'...
remote: Enumerating objects: 1259, done.
remote: Counting objects: 100% (1259/1259), done.
remote: Compressing objects: 100% (696/696), done.
remote: Total 1259 (delta 743), reused 714 (delta 430), pack-reused 0
接收对象中: 100% (1259/1259), 623.93 KiB | 150.00 KiB/s, 完成.
处理 delta 中: 100% (743/743), 完成.
正克隆到 '/home/licyk/.pyenv/plugins/pyenv-doctor'...
remote: Enumerating objects: 11, done.
remote: Counting objects: 100% (11/11), done.
remote: Compressing objects: 100% (9/9), done.
remote: Total 11 (delta 1), reused 5 (delta 0), pack-reused 0
接收对象中: 100% (11/11), 38.72 KiB | 922.00 KiB/s, 完成.
处理 delta 中: 100% (1/1), 完成.
正克隆到 '/home/licyk/.pyenv/plugins/pyenv-update'...
remote: Enumerating objects: 10, done.
remote: Counting objects: 100% (10/10), done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 10 (delta 1), reused 5 (delta 0), pack-reused 0
接收对象中: 100% (10/10), 完成.
处理 delta 中: 100% (1/1), 完成.
正克隆到 '/home/licyk/.pyenv/plugins/pyenv-virtualenv'...
remote: Enumerating objects: 64, done.
remote: Counting objects: 100% (64/64), done.
remote: Compressing objects: 100% (56/56), done.
remote: Total 64 (delta 10), reused 30 (delta 1), pack-reused 0
接收对象中: 100% (64/64), 42.50 KiB | 1.63 MiB/s, 完成.
处理 delta 中: 100% (10/10), 完成.

WARNING: seems you still have not added 'pyenv' to the load path.

# Load pyenv automatically by appending
# the following to 
# ~/.bash_profile if it exists, otherwise ~/.profile (for login shells)
# and ~/.bashrc (for interactive shells) :

export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"

# Restart your shell for the changes to take effect.

# Load pyenv-virtualenv automatically by adding
# the following to ~/.bashrc:

eval "$(pyenv virtualenv-init -)"
```

这里提示需要将 Pyenv 命令添加到环境变量，而当前的 Shell 为 Zsh，所以使用下面的命令将 Pyenv 添加到环境变量。

```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```
重载 Shell 配置让配置生效。

```bash
source ~/.zshrc
```

>[!NOTE]
>其他的 Shell 可参考该文档说明：[pyenv/pyenv - Set up your shell environment for Pyenv](https://github.com/pyenv/pyenv?tab=readme-ov-file#set-up-your-shell-environment-for-pyenv)

重载配置后就可以使用 Pyenv 安装指定版本的 Python。

```bash
pyenv install 3.10.14
```

安装完成后将会显示下面的内容。

```
Downloading Python-3.10.14.tar.xz...
-> https://www.python.org/ftp/python/3.10.14/Python-3.10.14.tar.xz
Installing Python-3.10.14...
Installed Python-3.10.14 to /home/licyk/.pyenv/versions/3.10.14
```

这里显示了 Python 安装在`/home/licyk/.pyenv/versions/3.10.14`，这时候可以运行 Python 命令查看 Python 是否正常使用。

```bash
/home/licyk/.pyenv/versions/3.10.14/bin/python --version
```

能够正常显示版本信息说明 Python 可用，而`/home/licyk/.pyenv/versions/3.10.14/bin/python`就是 Python 解释器的路径。

>[!NOTE]
>参考：[pyenv/pyenv: - Automatic installer](https://github.com/pyenv/pyenv?tab=readme-ov-file#automatic-installer)


### 使用 MicroMamba
1. 安装 Micromamba

```bash
"${SHELL}" <(curl -L micro.mamba.pm/install.sh)
```

接下来会有几个安装提示。

```
Micromamba binary folder? [~/.local/bin]
```

这里提示 MicroMamba 的安装路径，直接回车。

```
Init shell (zsh)? [Y/n]
```

这里提示是否要初始化 Shell，输入`y`后回车。

```
Configure conda-forge? [Y/n]
```

这里提示是否配置 Conda 源，输入`y`后回车。

```
Prefix location? [~/micromamba]
```

这里提示软件包存储的路径，直接回车，接下来等待安装完成。

安装完成后将会有以下提示。

```
Micromamba binary folder? [~/.local/bin] 
Init shell (zsh)? [Y/n] y
Configure conda-forge? [Y/n] y
Prefix location? [~/micromamba] 
Modifying RC file "/home/licyk/.zshrc"
Generating config for root prefix "/home/licyk/micromamba"
Setting mamba executable to: "/home/licyk/.local/bin/micromamba"
Adding (or replacing) the following in your "/home/licyk/.zshrc" file

# >>> mamba initialize >>>
# !! Contents within this block are managed by 'mamba init' !!
export MAMBA_EXE='/home/licyk/.local/bin/micromamba';
export MAMBA_ROOT_PREFIX='/home/licyk/micromamba';
__mamba_setup="$("$MAMBA_EXE" shell hook --shell zsh --root-prefix "$MAMBA_ROOT_PREFIX" 2> /dev/null)"
if [ $? -eq 0 ]; then
    eval "$__mamba_setup"
else
    alias micromamba="$MAMBA_EXE"  # Fallback on help from mamba activate
fi
unset __mamba_setup
# <<< mamba initialize <<<

Please restart your shell to activate micromamba or run the following:

  source ~/.bashrc (or ~/.zshrc, ~/.xonshrc, ~/.config/fish/config.fish, ...)
```

这里提示需要重启 Shell 来重载 Shell 配置文件，使 MicroMamba 生效，而当前的 Shell 为 Zsh，所以使用下面的命令重载 Shell 的配置文件。

```bash
source ~/.zshrc
```

>[!NOTE]
>需要根据当前使用的 Shell 来使用不同的重载 Shell 配置文件的命令。

使用 MicroMamba 创建一个虚拟环境并安装指定版本的 Python。

```bash
micromamba create --name python310 python=3.10.14 -y
```

安装完成可以查看 Python 的安装路径。

```bash
micromamba run -n python310 which python
```

下面将输出 Python 解释器的路径。

```
/home/licyk/micromamba/bin/python
```

这里的`/home/licyk/micromamba/bin/python`就是 Python 解释器的路径。

>[!NOTE]
>参考：[Micromamba Installation — documentation](https://mamba.readthedocs.io/en/latest/installation/micromamba-installation.html)


### 使用 MiniConda
1. 安装 MiniConda

```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm -rf ~/miniconda3/miniconda.sh
```

显示下面的内容说明安装成功。

```bash
正在保存至: “/home/licyk/miniconda3/miniconda.sh”

/home/licyk/miniconda3/minicond 100%[=====================================================>] 137.15M  3.90MB/s  用时 34s     

2024-06-25 00:25:58 (3.98 MB/s) - 已保存 “/home/licyk/miniconda3/miniconda.sh” [143808873/143808873])

PREFIX=/home/licyk/miniconda3
Unpacking payload ...

Installing base environment...

Preparing transaction: ...working... done
Executing transaction: ...working... done
installation finished.
```

当前使用的 Shell 为 Zsh，所以使用下面的命令将 MiniConda 的配置文件添加到 Shell 的配置文件中。

```bash
~/miniconda3/bin/conda init zsh
```

运行后将显示下面的内容。

```
no change     /home/licyk/miniconda3/condabin/conda
no change     /home/licyk/miniconda3/bin/conda
no change     /home/licyk/miniconda3/bin/conda-env
no change     /home/licyk/miniconda3/bin/activate
no change     /home/licyk/miniconda3/bin/deactivate
no change     /home/licyk/miniconda3/etc/profile.d/conda.sh
no change     /home/licyk/miniconda3/etc/fish/conf.d/conda.fish
no change     /home/licyk/miniconda3/shell/condabin/Conda.psm1
no change     /home/licyk/miniconda3/shell/condabin/conda-hook.ps1
no change     /home/licyk/miniconda3/lib/python3.12/site-packages/xontrib/conda.xsh
no change     /home/licyk/miniconda3/etc/profile.d/conda.csh
modified      /home/licyk/.zshrc

==> For changes to take effect, close and re-open your current shell. <==
```

这里提示需要重启 Shell 使 Shell 的配置文件生效，使用下面的命令来重载 Shell 的配置文件。

```bash
source ~/.zshrc
```

重载 Shell 的配置文件后默认进入了 MiniConda 默认的虚拟环境中，需要新建一个虚拟环境并安装 Python。

```bash
conda create --name python310 python=3.10.14 -y
```

安装完成可以查看 Python 的安装路径。

```bash
conda run -n python310 which python
```

这时将显示 Python 解释器的路径。

```
/home/licyk/miniconda3/envs/python310/bin/python
```
这里的`/home/licyk/miniconda3/envs/python310/bin/python`就是 Python 解释器的路径。

>[!NOTE]
>参考：[Miniconda — Anaconda documentation](https://docs.anaconda.com/miniconda/index.html)


## 为 Term-SD 指定 Python 路径
知道 Python 解释器的路径后，这时就可以为 Term-SD 指定要使用的 Python，这里我的 Python 解释器的路径为`/home/licyk/.pyenv/versions/3.10.14/bin/python`，在启动 Term-SD 时使用启动参数来指定。

```bash
./term-sd.sh --set-python-path "/home/licyk/.pyenv/versions/3.10.14/bin/python"
```

这时 Term-SD 将会把 Python 解释器的路径写入到 Term-SD 的配置文件中并使用该路径的 Python 解释器，在下次启动 Term-SD 时就不需要再使用`--set-python-path`启动参数来指定 Python 解释器的路径。

如果要修改 Python 解释器的路径，再次使用`--set-python-path`启动参数指定 Python 解释器的路径。

如果需要删除 Python 解释器的路径，则使用`--unset-python-path`启动参数删除 Python 解释器的路径配置文件。