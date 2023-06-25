### 问题
下载了 ffplay 的 snapshot 并且解压到 Downloads 目录下，但是为什么从 Terminal 进到 Downloads 后，调用不了 ffplay ?

<img width="769" alt="Screen Shot 2023-06-25 at 7 42 14 PM" src="https://github.com/qifeibro/ffmpeg_video_cut/assets/87322305/59a1729b-e73a-489c-93e8-832793cc5a1a">

当我使用 `ffplay -version` 查看版本

返回

zsh: command not found: ffplay

### 解决方案

如果您已经下载并解压了 FFmpeg 的快照版本，但在终端中使用 ffplay 命令时出现"zsh: command not found: ffplay"的错误提示，可能是因为 ffplay 可执行文件的路径没有被正确添加到系统的 PATH 环境变量中。

您可以尝试使用以下方法解决这个问题：

1.  确保您已经解压了FFmpeg的快照版本，并且知道ffplay可执行文件的路径。假设您将FFmpeg解压到了`/path/to/ffmpeg`目录下。
    
2.  打开终端应用程序。
    
3.  输入以下命令来编辑您的zsh配置文件（如果您使用的是bash，则应相应编辑bash配置文件）：

    ```bash
    nano ~/.zshrc
    ```
    
    这将使用nano编辑器打开您的zsh配置文件。
    
4.  在配置文件中，找到以`export PATH=`开头的行（可能在文件的最后），这是设置系统PATH环境变量的地方。
    
5.  在该行的末尾添加FFmpeg的快照版本中ffplay可执行文件所在的目录路径。在我们的假设中，应该是：
    
    ```bash
    export PATH="/path/to/ffmpeg:$PATH"
    ```
    
    确保将`/path/to/ffmpeg`替换为您实际解压FFmpeg快照版本的目录路径。
    
6.  保存文件并退出nano编辑器。在nano中，按下Ctrl+O，然后按下Enter键保存文件，再按下Ctrl+X退出编辑器。
    
7.  在终端中输入以下命令以使更改生效：
    
    ```bash
    
    source ~/.zshrc
    ```
    
    这将重新加载您的zsh配置文件。
    

现在，您应该能够在终端中正常使用ffplay命令了。您可以尝试在终端中输入`ffplay -version`来验证是否成功解决了问题。如果仍然遇到困难，请确保您正确编辑了配置文件，并检查FFmpeg快照版本中ffplay可执行文件的路径是否正确。
