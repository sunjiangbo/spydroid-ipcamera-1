# An amazing android app #

**The source code of spydroid is now only updated on github, [here](https://github.com/fyhertz/spydroid-ipcamera)**
### In a few words ###
  * Spydroid is a little app. that **streams the camera and microphone of your phone to your browser or to VLC !**

  * It is the most powerful tool on the market if you are looking for a way to stream audio/video from your smartphone to your PC: **H.264 is supported with resolutions up to 1080p and AAC is supported on phones running ICS or JB**.

  * It also is **an awesome app for pulling off pranks**: you can remotly trigger funny sounds on your phone or toggle its flash.

  * **Developers, start [by reading this](https://github.com/fyhertz/libstreaming) to find out how streaming is achieved in Spydroid !!**

> If you're still not convinced, check out the [feature list](https://code.google.com/p/spydroid-ipcamera/#Features) to see what Spydroid is capable of :) And If you have questions, check out the [FAQ](FAQ.md).
> If you enjoyed Spydroid, or its source code (that I've tried to make as clear as possible), [please rate the app on Google Play](https://market.android.com/details?id=net.majorkernelpanic.spydroid), I would reallllly realllly appreciate :) And if you go and like [the facebook page](http://www.facebook.com/spydroidipcamera), you will be rewarded with all my gratitude :p

### In two images ###

|![http://majorkernelpanic.com/uploads/SpydroidImg.jpg](http://majorkernelpanic.com/uploads/SpydroidImg.jpg)|<a href='http://majorkernelpanic.com/uploads/spyinterface.jpg'><img src='http://majorkernelpanic.com/uploads/spyinterface.jpg' width='420' height='240'></img></a> |
|:----------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|The stream can be read by VLC                                                                              |Or in the awesome HTTP interface                                                                                                                                   |

|<img src='http://majorkernelpanic.com/uploads/spydroidbc.png' width='110px' height='110px' />|[Get it right now on google play !](https://market.android.com/details?id=net.majorkernelpanic.spydroid)|
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|


# Features #

  * The stream can be directly read by VLC which is great because VLC is a very powerful tool, for example **you can really easily record the stream in a file**. [See the FAQ to find out how](FAQ.md).
  * You can enable/disable sound or video streaming
  * The resolution, the bitrate and the framerate of the stream can be configured... Two video encoders are available for the video streaming: H.263 and H.264. For sound streaming AMR and AAC are available.
  * The flash can be controlled remotly !
  * You can choose between the back facing camera and the front facing camera (if your phone has one)
  * Funny sounds can be played on the phone from the HTTP interface ! Awesome isn't it ? :p
  * You can make the phone vibrate remotely
  * You can see the battery level of the phone
  * You can like [the facebook page](http://www.facebook.com/spydroidipcamera), and yes this is a feature !

# Requirements #

  * Gingerbread or better (API level >=9)
  * **H.263:** should work on phones that supports h263
  * **H.264:** should work on phones that supports h264
  * **AMR:** should work everywhere !
  * **AAC:** requiers Ice Cream Sandwich

# Dear developers #

You may notice that the project has moved to **git**, the old **svn** repository is however still available [here](http://spydroid-ipcamera.googlecode.com/svn/trunk).
I also created a github clone [here](https://github.com/fyhertz/spydroid-ipcamera).


**The streaming stack used in Spydroid is available as a standalone library [here](https://github.com/fyhertz/libstreaming) with its Javadoc and explanations about how it works and how to use it. It is available under two licenses, the GPL, and a commercial licence.**

# Licensing #

**If you are interested in using the libstreaming or parts of Spydroid in a close source commercial application, you can contact me at the mail address specified below.**


_Folks, please note that i'm a french dude, so if you see something that doesn't make any sense do not hesitate to correct me :) (fyhertz at gmail dot com)._

_Enjoy_

By <a href='https://simon.guigui.us/'>Simon Guigui</a> aka fyhertz