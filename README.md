# ffmpeg_video_cut
使用ffmpeg剪辑合并视频

ffmpeg : an open source command line tool for processing audio and video files

created by Fabrice Ballard in the year 2000

FFMPEG stands for Fast Forward Moving Picture Experts Group

It's used in a wide variety of tools like Google Chrome and Blender, as well as video platforms like Youtbe and Vimeo.

It's able to decode, encode, transcode, multiplex, d multiplex, stream, filter and play virtually any multimedia file in the world, with over one hundred different codecs supported.

<img width="722" alt="Screen Shot 2023-06-25 at 6 06 39 PM" src="https://github.com/qifeibro/ffmpeg_video_cut/assets/87322305/c5898f98-8db3-4ced-98d0-57865723cd4b">

It works by taking an input file, then passes it to a demultiplexer that splits the audio and video tracks into separate encoded data packets. These packets are then decoded into uncompressed frames, which can be further processed and filtered. You might modify the brightness and contrast, add subtitles, or visualize the audio as a waveform. Then, finally, these frames are encoded and multiplexed back into the output file.

In addition, it also comes with the ffplay tool to easily play media from the command line, and ffprobe to extract metadata from a file. In addition to tons of low-level libraries for developers building their own multimedia processing software.

To get started, install it, then open up the terminal. Use the "ffmpeg" command followed by "-i" to supply one or more input files to convert that file to a different format. Simply provide the name of the output; it will automatically detect the file extension and convert it to the proper codec. The "-c" flag can be used to specify an explicit codec, like MPEG-4 for the video track and MP3 for the audio.

You may also want to change the quality of the output file. The "-b" flag can change the bit rate, while the "-r" flag can change the frame rate, and "-s" can change the resolution.

In some cases, you may have multiple video clips that need to be combined together. These clips can be listed in their own text file, then combined together by specifying the format as "concat" and the codec as "copy". "Copy" can also be used to make modifications to a video, like when used with "-t" to trim a certain number of seconds off of the video footage.

But the most powerful option might be "-vf", which creates a filter graph that can handle transformations like rotation and scaling, and color modifications like brightness and contrast, in addition to many other effects.

If you have an SRT file for captions in your video, ffmpeg is able to convert it to an ASS file, which can then be used with the "-vf" option to easily add subtitles to your video.

它的工作原理是通过接收一个输入文件，然后将其传递给一个解复用器，将音频和视频轨道分开成独立的编码数据包。这些数据包随后被解码成无压缩帧，可以进行进一步的处理和过滤。你可以修改亮度和对比度，添加字幕，或将音频可视化为波形。最后，这些帧被重新编码和复用到输出文件中。

此外，它还配备了ffplay工具，可以通过命令行轻松播放媒体，以及ffprobe工具，用于从文件中提取元数据。还有许多面向开发人员的低级库，用于构建自己的多媒体处理软件。

要开始使用，安装它，然后打开终端。使用"ffmpeg"命令，后跟"i"，以便提供一个或多个输入文件，将其转换为不同的格式。只需提供输出文件的名称，它将自动检测文件扩展名并将其转换为适当的编解码器。"-c"标志可用于指定显式编解码器，例如视频轨道使用MPEG-4，音频使用MP3。

您可能还想更改输出文件的质量。"-b"标志可更改比特率，"-r"标志可更改帧率，"-s"可更改分辨率。

在某些情况下，您可能有多个需要合并的视频片段。这些片段可以在自己的文本文件中列出，然后通过指定格式为"concat"，编解码器为"copy"将它们合并在一起。"copy"也可用于对视频进行修改，例如与"-to"一起使用，从视频镜头中剪切指定秒数的片段。

但最强大的选项可能是"-vf"，它创建了一个滤镜图形，可以处理旋转、缩放等转换，以及亮度、对比度等颜色修改，还有许多其他效果。

如果您的视频中有SRT字幕文件，ffmpeg可以将其转换为ASS文件，然后可以与"-vf"选项一起使用，轻松地为您的视频添加字幕。




