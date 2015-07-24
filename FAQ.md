<br />


# Why would I need Spydroid ? #

Of course you need Spydroid, what a silly question :) [Download it right now from the market](https://play.google.com/store/apps/details?id=net.majorkernelpanic.spydroid) ! Spydroid is THE perfect ingredient for an infinit number of pranks, check the [feature list](https://code.google.com/p/spydroid-ipcamera/#Features) if you're not convinced :p

# How do I play the stream using VLC ? #

First, the computer that is supposed to catch the stream and your smartphone must **obvioulsy** be connected to the **same** network. If no wireless network are available, you can still turn on the wireless hotspot feature of your phone.
In three steps here is what you have to do:
  1. Start spydroid
  1. Open VLC on your pc and press Ctrl+N, in the dialog box copy out what is written in Spydroid at the bottom of the screen, it should look like this: "rtsp://xxx.xxx.xxx.xxx:8086/"
  1. Wait a little & have fun...

# How do I rotate the video in VLC ? #

You need to pass the following options to VLC, replace 90 by whatever angle you want :p You can also do this through the interface: Tools>Effects and Filters>Video Effects>Geometry

```
vlc "rtsp://xxx.xxx.xxx.xxx:8086/" --video-filter=rotate --rotation-angle=90
```

**Note that you should really use the latest version of VLC ! VLC v2 is required here**

# How do I reduce the latency in VLC ? #

Using the command line you can pass the following argument to VLC, it's also certainly feasable from the interface.

```
vlc "rtsp://xxx.xxx.xxx.xxx:8086/" --network-caching=500
```

However, the more you reduce the cache size, the more the video is likely to be choppy :/ According to my personnal experience, 400 msec is the minimum for video streaming.

**Note that you should really use the latest version of VLC ! VLC v2 is required here**

# The video stream is too choppy, what should I do ? #

  * Streaming video can be quiet bandwidth-greedy so make sure you are close enough to you wifi router. If you're not try to reduce the quality of the stream. Unfortunately some phones don't support setting a low framerate or a low bitrate and will simply silently ignore your configuration.

  * Make sure to try h263 and h264, one may work better than the other.

  * Surprisingly, **MPlayer** (another open source player) gives more satisfying results with video streaming, h263 & h264 streams both seem smoother...

# How can I record the stream #

Open VLC, click on "View" and then on "Advanced Controls". You can now see a red record button. Open the stream indicated by Spydroid, (or a [customized stream](AdvancedUse.md)) and press that red button ! The recorded video is in MPEG format. On Windows they are stored in the Documents folder labeled as VLC Record with the date and time. On linux I imagine the location may vary, on Ubuntu they are recorded in /home/you/Videos

You can modify the record directory with this option:
```
vlc --input-record-path=/home/you/something
```

# Can I stream HD video ? #

Depends on you phone ! My Galaxy SII can stream full HD video quite smoothly but only with H.264 and the back facing camera.
Just try to find out, it's easy:

**For FULL HD**
```
vlc "rtsp://yourphoneip:8086?h264=5000-20-1920-1080"
```

**For 720p**
```
vlc "rtsp://yourphoneip:8086?h264=5000-20-1280-720"
```

Or if you're afraid of the command line: start VLC press Ctrl+N, type: "rtsp://yourphoneip:8086?h264=2000-20-1920-1080" and press "Play" !

# Can I receive the stream on more than one computer simultaneously ? #

Yes, since v6.5.1 Spydroid supports multicast which is a way to deliver data to multiple peers simultaneously. All you have to do is to open the following URL on every computers: "http://yourphoneip:8080/spydroid.sdp?multicast".

  1. Open VLC
  1. Press Ctrl+N (Equivalent to Media->Open Network Stream)
  1. Open this stream: "http://yourphoneip:8080/spydroid.sdp?multicast"
  1. To stop the stream browse this page: "http://yourphoneip:8080/spydroid.sdp?stop"

All the other parameters supported by Spydroid can be combined with this option. For example, you can start a multicasted AAC stream of your phone microphone:
```
vlc "http://phoneip:8080/spydroid.sdp?aac&multicast"
```

The default multicast address used by Spydroid is 228.5.6.7 but you can change it if you want:
```
vlc "http://phoneip:8080/spydroid.sdp?multicast=228.5.5.5"
```