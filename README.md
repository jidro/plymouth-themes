# `plymouth-themes`

## 中文说明：

该仓库为搜集的各`Linux`发行版或下载后默认的`plymouth`主题。

该仓库中主题均由`/usr/share/plymouth/themes/`文件夹复制。

> **注意：**</br>
> `deepin-logo`为`deepin`的默认`Plymouth`主题（开机动画）</br>
> `elementary`为`elementary OS`的默认`Plymouth`主题（开机动画）</br>
> `elegant-linen-grey`为`MX Linux`的默认`Plymouth`主题（开机动画）</br>
> `ubuntukylin-logo`为优麒麟的默认`Plymouth`主题（开机动画）

### 如何使用

- ① 使用软件安装工具（不同发行版工具不同，例如`Debian`中使用`apt`、`ArchLinux`中使用`pacman`、`Red Hat`/`CentOS`/`Fedora`中使用`yum`或`dnf`、……）安装`plymouth`，必要时将`plymouth-themes`一并安装。

    > `Plymouth`自带了一些主题：</br>
    > `Fade-in`: "简单的有淡出淡入的星星的主题"</br>
    > `Glow`: "伴随着新兴标志的饼状引导进度条的企业主题"</br>
    > `Script`: "脚本案例插件" (漂亮的`Logo`主题)</br>
    > `Solar`: "带有燃烧的蓝色星球的空间主题"</br>
    > `Spinner`: "带有加载框的简单主题"</br>
    > `Spinfinity`: "显示旋转的无穷大标志的主题"</br>
    > `Text`: "三种颜色的进度条(默认白、浅蓝、蓝启动进度条)"</br>
    > `Details`: "详细的启动信息滚动输出"

- ② 复制该仓库中想用的`plymouth`主题（即开机动画）至`/usr/share/plymouth/themes/`文件夹中。

- ③ 使用如下命令获得已安装的主题列表：

    ```shell
    $ plymouth-set-default-theme -l
    ```

- ④ 按 `Ctrl+Alt+F6` 切换终端，使用`root`登陆，使用如下命令以预览主题：

    ```shell
    # plymouthd
    # plymouth --show-splash
    ```

    再按`Ctrl+Alt+F6`并输入如下命令退出预览：

    ```shell
    # plymouthd
    # plymouth --show-splash
    ```

- ⑤ 使用如下命令设置喜欢的主题： 

    ```shell
    # plymouth-set-default-theme -R <theme name>
    ```

- ⑥ 设置后重启

> **注意：**
>
> ① 安装设置过程中可能会遇到提示缺少固件的问题，可选择无视，亦可[下载缺失固件](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/)，导入到`/lib/firmware/<固件>`文件夹（若没有该文件夹，请先创建该文件夹）解决该问题。</br>
>
> ② 若希望为显卡添加模式设置，可在`/etc/initramfs-tools/modules`文件中添加如下内容：
> 
> ```shell
> # 英特尔显卡
> # KMS
> intel_agp
> drm
> i915 modeset=1
> 
> # NVidia显卡
> # KMS
> drm
> nouveau modeset=1
> 
> # ATI显卡
> # KMS
> drm
> radeon modeset=1
> ```

## English description:

The repository is a `plymouth` theme that I am using or extracting Linux boot animation.</br>

This repository is my collection of various Linux distributions I have used before or the default plymouth theme after downloading.</br>

Themes in this warehouse are copied from the `/usr/share/plymouth/themes/` folder.

> **Note:**</br>
> `deep logo `is the default` Plymouth `theme of` deep `(boot animation)</br>
> `elementary` is the default `Plymouth` theme of `elementary OS` (boot animation)</br>
> `elegant-linnen-gray` is the default `Plymouth` theme of `MX Linux` (boot animation)</br>
> `ubuntukylin logo` is the default `Plymouth` theme of Youqilin (boot animation)

### How to use

- ① Use the software installation tools (different tools for different distributions, such as` apt `in` Debian `,` pacman `in` ArchLinux `,` yum `or` dnf `in` Red Hat `/` CentOS`/`Fedora`,... ) to install `plymouth`. If necessary, install `plymouth themes` together.

>`Plymouth` comes with some themes:</br>
>`Fade in`: "Simple theme with fading stars"</br>
>`Glow`: "The enterprise theme of pie shaped progress bar with emerging signs"</br>
>`Script`: "Script Case Plug in" (beautiful `Logo` theme)</br>
>`Solar`: "Space theme with burning blue stars"</br>
>`Spinner`: "Simple theme with load box"</br>
>`Spinfinity`: "Display the theme of the rotated infinity flag"</br>
>`Text`: "Progress bars in three colors (default: white, light blue, blue)"</br>
>`Details`: "Detailed startup information scrolling output"

- ② Copy the `ploymouth` theme (i.e. startup animation) you want to use in the warehouse to the `/usr/share/plymouth/themes/` folder.

- ③ Use the following command to get the list of installed topics:

```shell
$ plymouth-set-default-theme -l
```

- ④ Press` Ctrl+Alt+F6 `to switch terminals, use` root `to log in, and use the following command to preview the theme:

```shell
# plymouthd
# plymouth --show-splash
```

Press Ctrl+Alt+F6 again and enter the following command to exit the preview:

```shell
# plymouthd
# plymouth --show-splash
```

- ⑤ Use the following command to set your favorite theme:

```shell
# plymouth-set-default-theme -R <theme name>
```

- ⑥ Restart after setting

>**Note:**
>
>① During installation and setting, you may encounter the problem of missing firmware. You can either ignore it or [Download Missing Firmware](https://git.kernel.org/pub/scm/linux/kernel/git/firmware/linux-firmware.git/tree/), import to the `/lib/firmware/<firmware>` folder (if there is no such folder, please create it first) to solve the problem</ br>
>
>② If you want to add mode settings for the video card, you can add the following contents to the file `/etc/initramfs tools/modules`:
> 
> ```shell
># Intel Graphics Card
> # KMS
> intel_ agp
> drm
> i915 modeset=1
> 
># NVidia graphics card
> # KMS
> drm
> nouveau modeset=1
> 
># ATI Graphics Card
> # KMS
> drm
> radeon modeset=1
> ```