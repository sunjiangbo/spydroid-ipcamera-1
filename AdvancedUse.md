# Introduction #

**Here are some advanced examples of use of the built-in RTSP and HTTP servers of Spydroid.**

# Examples of use #

### RTSP Server ###

Since v3.2, you can pass sophisticated URIs to the RTSP server to remotly configure Spydroid. Here are some example of what you can do:

**Enable video streaming & with H.264 and turn flash on !** (H.264 is a standard for video compression)
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h264&flash=on"
```

**Enable video streaming of the front facing camera !**
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h264&camera=front"
```

**Enable video streaming with H.263 and sound streaming with AMR and turn flash on !** (H.263 is also a standard for video compression and AMR is a standard for audio compression)
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h263&amr&flash=on"
```

**Enable video streaming and set bitrate to 200kb/s**
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h264=200"
```

**Enable video streaming and set bitrate to 500kb/s and framerate to 20fps**
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h264=500-20"
```

**Enable video streaming and set bitrate to 500kb/s / framerate to 20fps / resolution to 320x240px**
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?h264=200-20-320-240"
```

**Enable aac streaming (introduced in v3.3): this is very experimental and it requieres ICS**
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086?aac"
```

**You can of course still use the following basic URI.** Spydroid will then use a default configuration, that you can modify in the option menu !
```
vlc "rtsp://xxx.xxx.xxx.xxx:8086/"
```

### HTTP Server ###

**If you don't want to use the RTSP protocol, you can also start/stop streams using only the HTTP server** You can use any of the options presented for the RTSP server ! The HTTP server will respond with a Session Descriptor.
```
vlc "http://xxx.xxx.xxx.xxx:8080/spydroid.sdp"
```

**Because you're not using the RTSP protocol, streaming won't stop when you quit VLC. You have to GET the following URL:**
```
curl "http://xxx.xxx.xxx.xxx:8080/spydroid.sdp?stop"
```

**You can start up to two streams with the HTTP server** You can specify a stream id to distinguish the streams.
For example:
```
vlc "http://xxx.xxx.xxx.xxx:8080/spydroid.sdp?id=0&h264&flash=on"
```
```
vlc "http://xxx.xxx.xxx.xxx:8080/spydroid.sdp?id=1&amr"
```
```
curl "http://xxx.xxx.xxx.xxx:8080/spydroid.sdp?id=1&stop"
```