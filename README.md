# VodGo
视频床
# 切片
> 将 mp4 切片，并生成 m3u8 文件
+ output.mp4 需要切片的视频文件
+ playlist.m3u8 待生成的 m3u8 文件名
+ 5 切片时间，表示隔几秒进行切一个文件
+ output%03d.ts 生成切割ts文件名，output%03d.ts 代表生成 output001.ts、output002.ts 这样的格式，03d 可以随意修改，占位符
**ffmpeg -i VID_20200819_175113.mp4 -c copy -map 0 -f segment -segment_list mgg.m3u8 -segment_time 5 mgg%05d.ts**
# 链接
https://cdn.jsdelivr.net/gh/GitHub用户名/库名/文件目录/playlist.m3u8
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg.m3u8
https://raw.githubusercontent.com/forevermgg/VodGo/FirstVideoTest/mgg.m3u8
