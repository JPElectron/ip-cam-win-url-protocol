# ip-cam-win-url-protocol

Allow rtsp or ax protocol URLs to be opened with wmplayer or VLC on Windows

For example, allow...

Start > Run > rtsp://<camera_ip> to open with VLC

or

HTML "a href" link such as axrtsp://<camera_ip> to open with Windows Media Player

This method of rtsp or axrtsp URL opening Windows Media Player or VLC is desirable if you want a full-screen IP camera view to launch automatically on Windows.

Useful with home or business automation, for example...

Doorbell push: IFTTT > webhook > axrtsp:// > opens wmplayer.exe /fullscreen

Package delivery: Sighthound video detects person on porch > webhook > axrtsp:// > opens wmplayer.exe /fullscreen

Using Windows Media Player, a so-called 'Ax protocol' needs to be used...
(required to have AMC from https://www.axis.com/support/tools/install-and-manage-systems/axis-media-control installed)
Note: This 'Ax protocol' can't play a Panasonic network camera RTSP / H.264 URL even when properly formatted, the video feed is simply blank


## Using VLC or Quicktime...

    rtsp://<camera_ip>/axis-media/media.amp

    rtsp://<camera_ip>/axis-media/media.3gp  (don't bother with this: https://en.wikipedia.org/wiki/3GP_and_3G2)

    rtsp://<camera_ip>/MediaInput/h264  (for Panasonic network cameras)

## Any browser still image...

    http://<camera_ip>/axis-cgi/jpg/image.cgi
    
    http://<camera_ip>/cgi-bin/camera  (for Panasonic network cameras)

## AxProtocol notes...

    axrtpm://<camera_ip>/axis-media/media.amp  = MJPEG, MPEG-4 and H.264 multicast RTP streams

    axrtpu://<camera_ip>/axis-media/media.amp  = MJPEG, MPEG-4 and H.264 unicast RTP streams
    
    axrtsp://<camera_ip>/axis-media/media.amp  = MJPEG, MPEG-4 and H.264 unicast RTP over RTSP

    axrtsphttp://<camera_ip>/axis-media/media.amp  = MJPEG, MPEG-4 and H.264 unicast RTSP streams over HTTP

    axrtsphttps://<camera_ip>/axis-media/media.amp  = MJPEG, MPEG-4 and H.264 unicast RTSP streams tunneled via HTTPS

    axmpeghttp://<camera_ip>/axis-media/media.amp  = MPEG-2 unicast streams

    axsdp://<camera_ip>/axis-media/media.amp  = MPEG-2, MPEG-4 and H.264 multicast streams without RTSP
    
    rtsp://<camera_ip>/axis-media/media.amp  = H.264 - MPEG-4 AVC (part 10) / MPEG AAC Audio (mp4a) Real Time Streaming Protocol

Note: MJPEG uses considerable amounts of bandwidth compared to other options

[End of Line]
