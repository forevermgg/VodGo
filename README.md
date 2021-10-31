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

# 使用
+ 现在访问是m3u8是不可以播放视频的会自动下载
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg.m3u8
https://cdn.jsdelivr.net/gh/lete114/CDN2/video/4.m3u8
+ 访问文件也是不行的会乱码
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/main/FirstVideoTest/mgg00000.ts
https://cdn.jsdelivr.net/gh/lete114/CDN2/video/4000.ts
+ 将下载的文件拖入vlc播放器播放
+ dplayer实现html播放 http://dplayer.js.org/guide.html#options

# 坑点
+ vlc可以播放的m3u8
```
#EXTM3U
#EXTM3U
#EXT-X-VERSION:3
#EXT-X-MEDIA-SEQUENCE:0
#EXT-X-ALLOW-CACHE:YES
#EXT-X-TARGETDURATION:6
#EXTINF:5.066500,
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg00000.ts
#EXTINF:5.036778,
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg00001.ts
#EXTINF:5.050422,
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg00002.ts
#EXTINF:3.350222,
https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg00003.ts
#EXT-X-ENDLIST
```
+ https://cdn.jsdelivr.net/gh/forevermgg/VodGo/FirstVideoTest/mgg.m3u8 link open 下载下里的的m3u8
```
#EXTM3U
#EXT-X-VERSION:3
#EXT-X-MEDIA-SEQUENCE:0
#EXT-X-ALLOW-CACHE:YES
#EXT-X-TARGETDURATION:6
#EXTINF:5.066500,
https://cdn.jsdelive.net/gh/forevermgg/VodGo/main/FirstVideoTest/mgg00000.ts
#EXTINF:5.036778,
https://cdn.jsdelive.net/gh/forevermgg/VodGo/main/FirstVideoTest/mgg00001.ts
#EXTINF:5.050422,
https://cdn.jsdelive.net/gh/forevermgg/VodGo/main/FirstVideoTest/mgg00002.ts
#EXTINF:3.350222,
https://cdn.jsdelive.net/gh/forevermgg/VodGo/main/FirstVideoTest/mgg00003.ts
#EXT-X-ENDLIST
```
+ 更新不及时

# 参考
https://kakawanyifan.com/90599
