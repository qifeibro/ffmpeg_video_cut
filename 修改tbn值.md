```
ffmpeg -i input.mp4 -video_track_timescale 90000 -c copy output.mp4
```
这个命令使用了-video_track_timescale选项来直接更改视频的时间基准（tbn）为90k。-c copy参数用于直接拷贝视频和音频流而不重新编码。
