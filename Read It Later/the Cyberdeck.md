---
date: 2025-10-11T08:53:18+08:00
url: https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html
status: Favorite
---
[Skip to main content](https://themechanicaltype.blogspot.com/2022/02/#main)### Search This Blog

# [In Mechanica Antiqua](https://themechanicaltype.blogspot.com/)

Typewriter repair and collecting, rare books, typography, photography, and anything in between.

<iframe id="aswift_0" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame0"&gt;</iframe> 

<iframe id="aswift_1" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame1"&gt;</iframe> 

### the Cyberdeck

- Get link
- Facebook
- X
- Pinterest
- Email
- Other Apps

[![[Read It Later/attachments/020a6343c0392da2123370687ba3ae49_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhnsiA4_vQlS-DwyNMkAd1QOlyZMzMuChsJ9yidhIdw4r2iLeJnp2RImBrxwf6uZBLA3_m-OEVwGAP_zqchc_ZOGP5Ah-fZqfcxHIEVUe4AJWyCdllwHvhUpj86Cl9Lpy_1jqUD7F6IF2Tpm4IH6OpH63QcWrt5ztAcD4QhGQfmh192DubGaaFNW-qa=s8272)

I can't be the only one to find myself lost in the internet rabbit holes in an age such as ours.  Sometimes it's an uninspiring frustration, and other times you find yourself on the path to discovering something truly cool.  A few weeks ago, I stumbled upon a group of unique creators making what they called "cyberdecks."  The concept was a dystopian-esque or retro-futuristic portable computer, in part inspired by the cyberpunk movement, Blade Runner, and Fallout, though there are plenty of other sci-fi extravaganzas that employ similar devices.  The cool thing about cyberdecks is that they work, and there is no right way to create one.  There come in a variety of shapes and sizes, some in the traditional clamshell style, and others that their own entirely new concept.

I had toyed around with the idea of creating a small portable computer, and decided I would give it a shot.  I've always been a fan of the aesthetic of old computers, so I decided to try and build one into a CRT display.  My original idea was to use a Sony Watchman, but it ended up being far to small to do anything useful with.  The unit I eventually found was a Magnavox portable television/radio.  I figured it would look pretty cool as a computer.

**A CRT IS A HIGH VOLTAGE DEVICE, HANDLED CARELESSLY IT CAN SERIOUSLY INJURE OR KILL YOU.  SO CONSIDER YOURSELF WARNED, TREAD LIGHTLY, AND KNOW THAT IT IS NOT MY RESPONSIBILITY IF YOU GET HURT.**

[![[Read It Later/attachments/26b000fbf286bb0cd1ea04c412327ad0_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgHFchs7A7IJQ4EPKGm56BkM9RaIS6ixA9uEx2L__elmYtwuPcnLK-QzqX4CO1Or5sRH4MKPFPLbKocCkrILKWQxeHCZnf2OzNjeuB9IE8G8_oEbyq8SORMo8xvc8U_WB-ndKWBUTK71d8c_pTchY2aZHyiaPaWazyd-ZAcKUYwmRnwJ2gvlE7HcmPl=s4624)

first impressions

I picked the unit up off of eBay for a pretty low price, but was assured that the screen powered on.  Since the cancellation of analog broadcasting in the US, all VHF and UHF televisions are completely useless.  These units need to be hardwire modified to accept a composite video signal.  The other thing to search for was a single board computer module.  I chose the Raspberry Pi 4, a widely available unit that outputs a composite video signal and runs off of relatively low voltage.  There were a few downsides to using one of those, but I'll get to those later.  

The core design was simple, I didn't intend to modify the casing much, and wanted the radio to continue to work.  I decided I wanted mouse and keyboard to come out the front to replace the TV band tuner, and a keyboard matching in size sitting in front like the Commodore SX-64.  I saw some similar designs based around the Sears branded portable TVs after I purchased this unit, and I found those to be very cool, though I did enjoy the boxier look on mine.  Maybe another project another time.

[![[Read It Later/attachments/00e1fd747c36ac238f09ff5b2f76c347_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhCVpr8hflDmaPqXY__5S4MlZiiL27cXhxD8dAalpyTRipqENlzaM-5tbM2OfONugJF67aF3smuHmZYbq7heLSIiTVl9Jz3uB6VIUHwxIW55NQP6QerlciwSZVOUqN-ah0N0qjLEGQfQWIm3833d3jcJ-f23lDTC_mwj8T19w_Cc-gBRP3bdCJhcwTd=s2592)

a similar concept by r/drake9800 on Reddit using a Sears/Sanyo

  

As soon as I got the TV, I removed the five case screws and separated the radio unit and top lid.  The construction was rather simple, I unplugged the control, power, and audio to the radio and cut the antennae cable out.  Then I noticed that the power board was shattered into multiple pieces, the TV did not power on like I was told it would.

  

[![[Read It Later/attachments/b9a4cc6b122f5d038293ccf6529856c5_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEj7LZ0TT2khB6MHP5Fkz8OUay_bMYl-R5Y_sAt7Vt0I0l61GeBxmvp0mnbW4U7YgNBE5klPrjgSu0NXYw5KQEuQOUYjLWFwHO7TlOJhVJ94Dbbitycekb9n3D2aTBTqbq-wx7EXu3Gzf1aRHWbUVPSMSNl1iTtH5lAlCZb6E6yOvGBuan0mH11IVc3P=s4624)

  

[![[Read It Later/attachments/1e6b23eee73f0c7f6b2f01afefb9e06f_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgBzPj6SZmwfCErH_oRCyZySlktuVl9ORy2o8kKFBCNnxyeY8DWtuYSXZIsbVZxzw3fzPtptjRnWY0lVMO5CUbe8eH9FopvB-SpcwH0QaJebjBYJ5bccBjABt5RMqzE1T8tRlM83hUTVH_juFcXgpqssT9j4rTClb9mF9p-tPhOiUqLLsorS0r7PTwz=s4624)

  

It was also overall more complex than I was anticipating.  The Sony units tended to employ IC chips to convert the RF signal into composite, I imagined it would be the same here, but as it turns out the only chips on the board were a couple of 8 pin amps.  The two silver boxes on the right were the UHF and VHF tuners, which input a video signal through an IF channel.  If you followed that trace across the board, one could theoretically find the point where it turns into composite.  The first thing I noticed were seven wires in a line coming off the board and going straight to the video amp board on the back of the tube.  Turns out that one of those leads was my video signal.  I had also considered removing the tuner units, but I decided to leave them as it didn't really accomplish much other than extra work.

  

[![[Read It Later/attachments/691d260386020fc9e2b62be223ac7c61_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhmjN6npNgRjKPpWXQGHgcOHq5Iz5qE1JRYidfmCwixg9o76nMYgyll_0RKy7YE2kTSbUePFuiBWPCgZT6WFOBbGITsINwlyrH9HbeGcA9i4wdd8wVC5kpvGOq0IYrIAZPyDslbDRDpE2PrGm0l87vQJuGTu5qtv7zkU8aLvThsTvDkKX6bTUVOLvfE=s4624)

  

[![[Read It Later/attachments/be3bc291d104c8748a4f1dfe153b4c2d_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEimX-rdGP8Tf26nw-a4E7LJfTmvvwYOfU5UnAlTNjxzEs6GXHspa43VXNg7B6OvdG2yGYBkOirjnBIBUcUz66QojXPhVaeGR8-bHMlXkgxD_V3h4TAB8kF6tpS9VdsS_WoLTrkAnqdOntpZJLQRMhuUWHaAGWJgvwVFcEvKLb0dwJOAFpvV5kalmG2K=s4624)

  

The first thing I had to sort out with the unit was how to get the  CRT to power on in the first place.  The power board accepted AC, DC, and batteries, but was broken into three or four separate pieces.  The AC wires go directly to a transformer which output about 15v, and then into a simple bridge rectifier (four diodes in a square backed up with capacitors) to transform it to DC current.  This is then split through a series of components, grounded, and passed through a fuse on the other half of the board.  It took a bit of time to figure out which traces needed to be bridged with spare wire before I could get the unit to power on.

  

[![[Read It Later/attachments/eaad1d1eb2f9a0f27a01c40094f286e6_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhzClRO4qKJSJHGVSGJvq7hXrsTz54I1o7-QID3NJD-ctuHlzuMn-6sN-GJw9K3Z81wtUJHVPVEqvgXkxQrpCdmpLPj6bmEkqbJFN__WskxkXImb9m-EfqGe2lHi8fwuD6J00gP_ueBq07lOrV7j7z-rrmageJl_nt2T_VTIcniX-Pi_DF-Jyip7Kzs=s4624)

One bridge from the DC input to who knows where

  

[![[Read It Later/attachments/c477e3481a6d5c317b1945c5e30f9443_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjaZX0XGYBcs9dVhyPVaESzHr_56-5GxswY8Nal4J16GEITiKlbfNvucvxuKeljEE7mXo8uom7QCTkH4glGbZGwEKaXLK9epifwij3KIbYDy2IBMO5gNU0xhso22g9wb-V9w4RSkWQfzAbgDiCGiWWeKNnlOLNiVlHUHsO9a4q2poTR6_NyFUMHQecl=s4624)

the bridge rectifier

  

[![[Read It Later/attachments/c97c645f6c85b67d9bcf73eb863197fe_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEinepluLxxAk3I2Ktyjb6cHHENjsYazOAW7Azq2OHYc6Fd-57cHUR9_PUF28RQZHMxfp1k-L4Oo50gX5hlIkkUqzk9NRvUbAlHokNcLigQADfnzCaDS7aqgAT68wrv02_NUCYaavm_P_yuPjD-gedMrgm3VioAdzq5vdHnmqT8x9F5OL3hS5hfaggx-=s4624)

The second larger bridge

  

[![[Read It Later/attachments/ab58adec3cfd07efabc8bef80b9c4e0d_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjOdxI5VFdM0-sACMiplm9PlesUi_AcFnTFBNqHjCH1I6OgQhbPohe-VyQPkjG05LQqpZNyYS9oJyRWY-uEau9s9BQG5FjcTjlp7YWCyI5OcrTVhSEzs5Za9sIXr9G3dHSazV5fSRNTv30usS0F_ocydnXuaDCSmG_4YCTwoW5xMtaSn4-w6cD_gbjV=s4624)

  

[![[Read It Later/attachments/52daf69fbea443c6f9120a997140fcba_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjxAPB2nN-WqRBnv1JqLA8C30fVrdXpXKcg7QIm7M-b8MGivJSWDxqk-NvLkJH2y01omXaE2vrGoingzywbUK6dMnAn5viqz0xlLeiUu7jfVCtnWbpOJXKuKD1MBy-qoS0srZtPSFv-afFCPTjtgRzrS-_5CDglBZGYgUiiiRO93tTtMY-XAoFYOjTC=s4624)

and power to the tube!

  

I placed a mirror in front of where I was working so I could both access the board and see the screen.  Once I had power to the tube, I was able to extend the ground wires to a common ground point and begin probing the bottom of the board.  Rather than use an Oscilloscope, I decided to use a VHS camcorder.  I cut an RCA lead, grounded it to the TV, and used the end of the signal wire to locate the video path.  All in all, it was a lot easier than I thought.  The audio was grounded to the same point, and soldered into the board.  It worked, but sounded terrible.  That circuit was more complex strangely enough, but since I had no intention of using it for a whole lot of audio stuff, I decided to leave it as is.

  

[![[Read It Later/attachments/27fdd462bec8ef219226d1b18c2ee6e5_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEiki_8wkwGmEzD6u55ByE-zz_QtJWqhoC_LOM03hmx5yW4Bu9vveu9b0ibjzBeXi0akCBZ7vncmAAEE9iG4qh7r4Qk8rbjQra1NRkoKlIC9-7--JXzWBq9k5WzN7PcFWkipMNfvIRKiTWy4qF6r4jIHhwg4J-6lhFVH1GgTglzf9uv9E-jA2QpwdGqx=s4624)

my poorly placed audio lead

  

[![[Read It Later/attachments/ebcdfc8fb1e0888d9828a51687b033a4_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhuyWRnFkfq0EPBEgtSRkAKsHm6XGUiQgJRejzL3WXMrhIoqY8UISyXjjBrk1Ezly2d-K8dCBIw_TNxZZjguUEgmQxD6IvOnxrMtNSC2Nn-NCy8fjx5YOVXbbvR_QPstQ13-FB6bOtjucusp7LbHRbSuCC0DJXEB-OYl-f9uur06UwpfIIsX3xskuCl=s4624)

a 12v to 5v step down USB adapter

  

[![[Read It Later/attachments/d58a56985cdb1532322c6842a4108d67_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhDxSuwcSPRCL6RWYrDoEFAZc_JNn0X-m9HJGawN17FvTgumqxX2MsclHX8mrsm-kJK-UxuMpCJ3MUJGWxFsYVb3yPFbBw48XokQsNA4Ubjdv1XArJgKM80Ww2c4UjHTOBR6C5MTaiBpamdA3P8nYipwAyLu4HJRKnmrorQr_5bEXIrnuESrAweBUk-=s4624)

working video

  

The next step after video was to install the Raspberry Pi.  I downloaded a copy of the basic OS onto an SD card and made sure the program booted.  Output to composite had to be configured, as it is generally disabled by default in favor of HDMI cables.  I also ended up spending way too much money on wires, half of which were not used in this project.  

  

The Pi draws power through a USBC plug which I wired in through a step down transformer on the main board.   Composite came from the headphone jack, and the four USB ports would be used for data transfer, mouse, and keyboard.  I used JB weld to attach two L brackets to a USB extension cable and screwed it into the front of the unit.  That was the keyboard connection.  The mousepad was manufactured by a company called Ergo Touchpads, and this was their smallest model.  It was a PS2 only mouse, so I also needed to put a PS2 to USB converter inside.  The touchpad was mounted to the viewing window where the UHF and VHF channel selector was originally displayed.  

  

[![[Read It Later/attachments/12005d94dcffbb47eccbb43afed2b19a_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEiIu5zTEfxen4Elb7lICWO9HafvUSvbbUPgfhBG-cFcxMPSQtEAlcIRbNNAjiWbOJUsYyEJFMxbFe4jgRdBuWmWYAAEzF0bcv1eryiJt-d5_kzCOfOHS7ZXA2PCowPbgEgYBGhSkunUI5kGBQw98LfcNVxJmx7mb1a2t2k9aOj3NdZkWgS9DuOww-d_=s4624)

I scratched off the RF labels and taped in one of my own

  

[![[Read It Later/attachments/edcf068837ba09de38898c42bdb2fad0_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEh6gIeYroMWTGonjxXrHUZ12JqA1qvjjQEvmU7WfjAN-AzaJ7UV43jCJMPQ94aLH5j02Dus0SyYGXbJvvOHVyYW3KAZ-5KCRUopSo_-AUrMQgNl1CPxqxgTDsh6EtnU4FIJ70JoWPhwzTPQpFIBly5rv2Tk0nOodhMwsbMdbTZReg9wR4KwEKiZZ4B7=s4624)

Filed a slot in the side for the wire

  

[![[Read It Later/attachments/037f1bb07457dcb7e80821c03121f8aa_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgTZbgXW_CJsD0BQn_KouzYcvw7qsCEnRuO9foeBABIugH3yD43QDJVkdykxzkI_HngYVZmTF8FXzpP6tIpVvg_GFqANYJu0nL-T0XROj9sqg3lyAk_XFtixX7saGvwdbfjK0FW1VyOKDVpvPM4U_wx6CY-30d62sS5mDqyQSQRKZvAjh6DicmB2cpy=s4624)

and here it is mounted

  

Once the keyboard, mouse, and power were installed, I then had to figure out composite output.  The cable I ordered ended up not fitting within the confines of the TV case.  I assumed there would be enough room inside for everything, but that was not the case.  The Pi fit right beside the CRT tube, I bolted a plastic plate to it so nothing would short out, and ended up having to use a right angle headphone jack from a pair of broken earbuds.  It didn't take long to figure out which wires went to what, and everything was grounded and soldered.  At this point, the unit was basically working.

  

[![[Read It Later/attachments/064b782b3c8ffd0d9f133dc01107958b_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEg5v7TfYKkidarqk52rMVzInIO180bmlZBJy1XQsb4jYtiYLVGVIrZNR4n2rKYzypjkJQ3VqMHGPiI-ccckf9GKVRvTIa0oyamncilSDbkto_77zTcKofLk_4nOcK8c1q8Plc0bjpKxKNUEfid4WLJS9VcqBWs0VhoWWvi1w-52hngE5NSXwXqSnuKn=s4624)

The backplate 

  

[![[Read It Later/attachments/85c73e3f9c4bc1d29ae15422a0a715b5_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEiqfno8-khCUx7rOu5XDrooScH4BZxUszOZpVQ0128BQPZagGE-hdEehIzFyg2evjNai2Cs6yp0Hq5oDHNQQjhAZBYDLTZ3GOeeUMOsk3-niRXjqxHa-BpQ2WsVtnu2R_8M_eieRfzIHZbVLuzerDqXnWlTaPqcLgD-09nltwG-wB5_PHnPRa2H84ke=s4624)

a simple GPIO fan mounted to the board

  

[![[Read It Later/attachments/4dcb0ee3946683849e4172d8dff8d1fb_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgv-pbNk8TauqGfX2DJqL8q7tu9vyGtsuT2lOlZ2PqJ-GqRiLBD3Z8nr1HF_1euVDB2PP_ZNk44pK8OfrBwuLKmqV9vrnD8TWXrTnS1h6HeInCTRA24YO5Z1GkYAng91yEWseD2D_ZeGyX2SNwhLgbvXG0IjXARgkp2aBujEYDT5NpuaLWF0hBiS2k5=s4624)

the mess of cables (it gets worse)

  

[![[Read It Later/attachments/5ca0643fd3ec9e573de82873c21b7faa_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEiYLq53QQ4_TGGGldJsHwkrq2B6N_VJ6ev4O4EHZMFQH0hd2rxECJy09bFq1IOFH4aiD6-DKCXMxmdx0E2GTJUV_LxwPDiPAysJ7P1GJrbIklWzTfOtMgbzoy2UdzVEKK1Ic_028GyrqjFXECizsP8GS6apfWe3d8yM-DmfRWP6f8YD-npReQivOfgs=s4624)

The braided headphone cable, and my attached leads.

  

[![[Read It Later/attachments/ee9e15763b7f3ae75de43fe24566e2e0_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjPUHkHfaeDeLtcGVgdWW8TkzRmXtxPClH8f7lPnCvcMK4hHJKEez1MdHXTFGEDx5fIjxHvGTyiN90G9PCE3Ii4KZUgtLWY3AqQ0ZDi_fW97q7viFwC0Tp40juPIc4Zoftio7tmXztcB_SkT9y4wJRUjPZapX2lFDVogwK4Mr90Ut2hJyfehm_pfXwm=s4624)

the desktop boots!

  

It took a little bit to get the desktop to display right.  It still hangs off the edge of the display on the right, but I was able to configure it in such a way that the taskbar is evenly cropped and displayed across the bottom.  I ran some tests on the unit and all seemed to work well.  The only thing I had left to do was to install the USB 3.0 connections, and a separate power switch.

  

Now for the downsides.  The Pi operates off a Linux based system, and an SD card.  Both of which are very sensitive to sudden loss of power.  They need to be securely shut down from the software side to avoid data corruption.  The other downside is slow wifi but whatever.  I decided to mount a power switch that would boot the Pi independently of the unit itself, so I could not only control when it shut off, but also use the radio without worrying about data loss.  This also meant that the unit could remain plugged in or have batteries installed without the Pi booting up.  I cut all the holes and soldered all the wires in the span of a couple hours, though when I ran a battery test, I ended up having to resolder the 5v power supply since it was drawing power from the wrong trace.  The battery bay connects to the power board further along than the DC from the bridge rectifier.  

  

[![[Read It Later/attachments/a7113f987c7be670995884b073f42267_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEigUoXczvanPockVfohG5fyM0CW00G7M7LWkwXb2sIUP4gFok3LuHWfWFKNRjP1bkZowzQ-6rIeezk1_x9erhHtPrEsVLlcjMFXH0HjgxqXRtnOE2gIWs02PvYDEdYPjEmPivcJthHzJESzebSpt7dbEjgDlGH_1S8eYi22qJ3nOSU6haBgCDWF6Jd2=s4624)

testing

  

[![[Read It Later/attachments/5c6321946695ee8474072bfbffde8cb6_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjT_Qq3CRD7AwBhJoOHGqjI88K_K4zW2VOrSpdZADPkufmhAhYLk4hMq_-bj-AkMydghLkg8SfSAGkOkdqe8WCR0aJX6mAdUlDV_3IwWmIBNfhE3sEaaT1i6rmjDS4TXUVpIyQcLQG_RppAX2AUjupFPAthdXqc-cCKiKuNqhiyy6GXDa0cBNxbF3Sx=s4624)

the ports

  

[![[Read It Later/attachments/a000bcf61d6c445b1cd5aab877dab06a_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEjS2FxuTCEXQ_hGra_Ij7-cOplGhW7DvDY73C52azdGrvahoedLWQHT3ANxuRU8-ReBM917AdBBOIFaSu4yyWshIkt2Y1Rti6FQu8nMF7PjYfZRfMZ664NEM_lsqnVEDTutO2VHm7pqPSeDbfFs7g31qCrXPrQL7BYaBoW_SOF7dQ9GMVO4IFrv3HRT=s4624)

more testing/redditting

  

[![[Read It Later/attachments/839262ddc498f73c1b1815bd9800adc6_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEi5DrKCPqB8zqOI5sxmFkXwfJ2gkcgVuKRexiY6_fS3wDinkkeqL9S8IZCuuBTAigYknjE8kggWR4y2EihRSwGXGxMlDUHSGosFNG6gag5px7p0Hl55-JH4OhxRTta3-HQ_B1RF2w2WVkR8IngHRJt9DlhudaHzecgLcOrtlxu-kUrJvu0JQ__28AC_=s4624)

home stretch

  

[![[Read It Later/attachments/c5b27f1d64707869c32bfafc1243e242_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhCex-gHqy2QH9l9QO9Wnbbc31zk1pvqiawJQtT0_9yzZ-kkJBTSZ67zsrvJHeApMBY2yGaY9-ReNUEnNATRYWyax94V9CnczI84UmfsBWVWkVKCfOSfim_lfIEsR8UwCnz5JOlODzziXl-9rdWslS11e5vQbol4MNs8TZmeEkdebn9uE1QORmOy6yu=s4624)

the wrong power connection, see the red wire far left on the

bottom of three traces

  

[![[Read It Later/attachments/46960a9263ed961bebbc3a7a72905893_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEi0Oumu5VFcBzzj_H4K1PheR77-4IFUeXT09Zeb15oNLbtTYiyXlIDYfL9MIjxCIJD-sT4ryAjxCxNWiTnvl3yQsTOa9ykKv2fEcov1gtXPhjZ5qadPWarUzuJP5u9T6Sn8CbY_1nMKmXDlZOEny7uF9slFWu9BgJ9IYWs4NOYit-1_jTYFQgCZ7vK9=s4624)

fixed, and insulated with duct tape.  Those are the switch leads

  

[![[Read It Later/attachments/266ae7e6936441e95a212f0dfed9c008_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEg3bhUc22ukQpeF0c41gSwD5XuVTt881offhFQEQ1yC3wd1c8hK2Ae3ZBEkgi4ThAR_Iwvg2Sou_a1eJpAKOp6ElBDP37uBF_O7ozGa7CLkGZTrlTpd9KGr5MZ1mP1izalGqqnLV6i8hrCcCaGBBlYwArh3VXcFPAx7-oBZaTxDA3R1W-Z0YyhGWRsT=s4624)

Mounted is the switch, facing down, and the keyboard

connector cable screwed in firmly

  

[![[Read It Later/attachments/9f1883eda90404f211ebfde3bc1da26c_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgs3Rb4pVQAvq5-9TMq3bxmrDq24UpKCPM5QqhJKnpRccIV4MoXTF8gm21UPnp73fAvUySTvg0AIDJPhknnJnjnRU67cMMjJxJjMYpb4C2TdP-wxZgQgDrZDlWA6LhhPDvd1J31LMCXW-GT8eNONfsL-7eJQrDzu5kM255q_QdC2AP_WXdx9y48ASOQ=s4624)

Two rear mounted USB 3.0 panels, removed the internal

speaker to access them.

  

[![[Read It Later/attachments/c038cfa4a441e939c60501d91b0fec6c_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhCCLkcIFAeEe08fjXfWu8d2skfRmfFjPZLBkRua25I5-g9ym0All4YszgLqi1vGLsq5PE1NbQd1S-iBwJvKwJWuFuGfyqfgVfiiByQK513_tOFahOkilCT-aaRyvOtewQChxq0FyrsgjNAXcDcYXvS9bHsRIAK_nrKPVYp5UEI6QqB0eZp9VDSTbgm=s4624)

All the components together.  Had to cut one of the

support posts out to fit the USB wires.

  

It ended up being a very long project, long but rewarding.  It is probably one of the coolest things I've built, or at least it is to me.  I do intend to hook up a rechargeable battery pack at some point, that would solder into the battery compartment.  I also want to stitch some leather saddle-type bags to hold extra cables and the keyboard, which is a custom built 60% layout with arrow keys.

  

[![[Read It Later/attachments/2d5960bf162ff8168ed4e9cde5e765d9_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEi79oxPIUrbDfY-VLkFA64TJOZMilOF4i_Grns1iM0AbarlkRkf1vLxcJvjb9nRoWai_EuLylEQXPELVuQc-lFzBdRekh_KFxMTb9jrdj6wgn3TcCG0lw_NbENohZyuoOzN5u-83Lai4BVD01moHKJNaQfzQ1o7RCtQba3nWLlvNaz5MCIyWQvtKz29=s4624)

the portability test on 9 D cell batteries

  

The keyboard features Gateron Silent Brown switches.  I needed something quiet for late typing sessions, and I wanted a nice aluminum case.  Turns out the PCB actually bowed and shorted on the back of the case, so I needed to support and insulate that with paper towels and cardboard.  Super high tech, I know.

  

  

[![[Read It Later/attachments/b4998aa41e830e3c649329fa0eea58a2_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEiiNAwbmiTLcqvx-zCNtZSCNCVvwKRIOyx9t7SVdlHNsdKKVkGrfoY4a_gRAfy4qhtzyuk9Jz-ZFvj3eQdGJo1lPzgsdd94e9IYDf9PZRohtrw4CgeS004xd2absbWhOBl_qgipnNbN1kZ6w1xdm52U79JywRxwh5Ytjis64tL9SHMT9sVkynqYAgLS=s4624)

Nothing says pro-keyboarding like paper towels and cardboard

  

And that was the last step.  I may work further to try and create some onboard storage for keyboard portability.  As of now, the build is officially basically done, and I am very happy with it.  It is not the most powerful little thing, but how much do you expect to do on a 5 inch black and white CRT screen?  I did notice some poor edge sharpness, and some V hold issues, but overall I am very impressed with how well the unit works.  I guess we will see how long lasting this thing will be, but the simplest things are often the ones that last the longest.  Maybe this will survive a nuclear fallout, who knows?

  

[![[Read It Later/attachments/839262ddc498f73c1b1815bd9800adc6_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEhGwGyT-1bbDpG_kKjF0F7iLjGGAAD_fJaDICoNFGMLgJUEAoumoowg-LrbyOLQqomYXDuJibGDzBQoQVrPo-8GlYmPdaJzrDfXC-xrnnx8B7swoGLbJ5aOPGa8FedA_OYFXHB58KKNmdfb_9Iwoz5tOU51bhIuJW4zuKYPNG43Yyo-Mr8RHiNVCZ2Y=s4624)

  

[![[Read It Later/attachments/fc26b871cd08a29e6247c89f30d02623_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgqKVfVhdVJv1bc7IWxVqkBXNCz8uQ4scL5I-kd3HPv8OplxqWxT4GTTmR3mnC3u7y_VV1h26t4Dr0H3KEQQnCMY_FgMZF4JpdZrg0jhpn2P-Dl9MwzhJYStmbZM7sPRYXqlXEGdFH8No_5fe4PqbzI0Z3vPn_n3jPC61COMJzrkIY8SMLQXs5VrkQp=s4624)

  

[![[Read It Later/attachments/2a8c5868efaba72db6de2f902d919206_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgQktQp_RVayKpDYNDParnFwCOGQ4d1fH3iQOPa9l5MGdPFMBqKv8bbtek2Fyap3Nr3FmxW9uAKj2XARBIWULxL1TqxMCn8AhHtZifLNw-UknUppRegxyIaMMRqd7C_nHb76CyuIEDOin0Kec0i7H0PjKBef8BQPiF9imTDOUkDhgfepbqmnlrSM_-Z=s4624)

  

[![[Read It Later/attachments/0324d8de72bb75979e21711fcd0ea5c4_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEh6y4GPW2Qy_N4mpulkbAFFkCtGh7J436KIcc0tY8ApmnXop0kLOnzMur-7tgZ0qKTXE9i9M0hqhY0QPG_d5jstJM9EP3vQ9iuU6g0myQh7zik2GsLY18tDiz7Z33ffYmU8_UN8ut34tESh8s8zRlYTDLCHoBKNJK6_V1B9Ho6s-WLULGyNsw1Z1rh1=s4624)

Taking that cover photo :)

  

[![[Read It Later/attachments/8806f77fedaf21393004c8510b9e07eb_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgKy2yHMmTSTbP-4w5ZIYjyPkRUhLpNfJZ4max0W8Yy3HqRzfvE701xd532_5dHbm-nSIYh4lck0-sUxOPHoSWQrtJEfUsUWG_jfEFK8iQbx_Glm8G2Ob94u9uJ4RSNX3CwfdGy-1cDHtrRZk0RUDEW-6cJIsqDZiYeLXNck8aek3RD1dDA4qkDDUKV=s8272)

  

[![[Read It Later/attachments/7cdec1d417dc3dd1c5e2a16904d7849e_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEg0R1R60ld0PzqL3gDmmFpduT7AsdhwrOGiMTAlt_72LO2zN9Ivk9YUueywT3rk8YdrAccwMuuj1tEt1s7aOttv9XQerR_OWi5BCHezAqjfsrOhDQOvQtJGIEyyVxhkbN380uE9epxx8RDPTp3KGPFyXFW2PmsFwBzP1JMBykSIlXff6rDlFMHxPrbo=s8272)

  

[![[Read It Later/attachments/020a6343c0392da2123370687ba3ae49_MD5.jpg]]](https://blogger.googleusercontent.com/img/a/AVvXsEgjxAHe3-_qDQtzcRfqh2RE8wqStmIwByDHKzUherI3IwSziZUgJhviowNzD9ydKww-r_11UivKcYjVkK8kR49b-MsxZf9VQE1CrNkZnLq99ash73CZ56-ndK1hGy6yLFeG4PXwyuR-CJmOk9JRvxhqwdyI2rNHhpvEBs9Rwk7CMc5NmpbfpEx144t5=s8272)

  

  

  

Enjoy!

  

Here is a [VIDEO!](https://www.youtube.com/watch?v=Ty9pPNabPpQ)

  

- Get link
- Facebook
- X
- Pinterest
- Email
- Other Apps

### Comments

 

1. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[SteveK](https://www.blogger.com/profile/14844619655382811941)[February 24, 2022 at 4:26 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1645748763347#c5189328943993136839)
	Creative.. we're gonna need people like you come the apocalypse! ;D
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/5189328943993136839)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
2. ![[Read It Later/attachments/5a5f658d578d54dde553ab635b9a3a4f_MD5.jpg]]
	[Ted](https://www.blogger.com/profile/16774432656602082311)[February 25, 2022 at 8:53 AM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1645807980844#c1540021632698887829)
	Super Fun! I suppose we should enjoy CRTs while they still work. There will come a day when they're all gone, but personally, I tossed every hi-voltage CRT in the house the minute flat panels started showing up in thrift stores for lunch money. Well, except for the ones in my luggables (Osborne 1 & TRS-80 4p). Very well done project (:
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/1540021632698887829)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	- ![[Read It Later/attachments/51b5633ef2b1477fff4e5a3fcbabb660_MD5.jpg]]
		[Lucas Dul](https://www.blogger.com/profile/06562560826600046579)[March 4, 2022 at 9:31 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1646458266633#c5946400464109586952)
		Thanks Ted! We recently threw out our massive Sony, the largest CRT they ever built. Me and my brother almost broke our backs getting that beast out. I do miss it, but it simply took up WAY too much space. A lot of fond memories of Blockbuster VHS and Wii games.
		[Delete](https://www.blogger.com/comment/delete/8221059337769683965/5946400464109586952)
		[Replies](https://themechanicaltype.blogspot.com/2022/02/)
		[Reply](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
3. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[Buford Sides](https://www.blogger.com/profile/14704616014590108095)[February 25, 2022 at 9:47 AM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1645811228503#c834877269933420345)
	If only I had your skills....  
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/834877269933420345)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	- ![[Read It Later/attachments/51b5633ef2b1477fff4e5a3fcbabb660_MD5.jpg]]
		[Lucas Dul](https://www.blogger.com/profile/06562560826600046579)[March 29, 2022 at 9:19 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1648613987510#c7483539396286350389)
		Hey, I'm not particularly skilled :)
		[Delete](https://www.blogger.com/comment/delete/8221059337769683965/7483539396286350389)
		[Replies](https://themechanicaltype.blogspot.com/2022/02/)
		[Reply](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
4. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[Buford Sides](https://www.blogger.com/profile/14704616014590108095)[February 25, 2022 at 9:55 AM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1645811712319#c7730606388332649077)
	I have a 21-year-old RCA 19-inch CRT color television in our guest room that is still receiving over-the air broadcasts with a SDTV Tuner/analog to digital converter.
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/7730606388332649077)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
5. ![[Read It Later/attachments/ced8bf48208ff615fd12d6cfe31ded4d_MD5.jpg]]
	[Robin Heilschild 【蓋面】](https://www.blogger.com/profile/03429820251341371094)[February 27, 2022 at 8:36 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1646023007028#c950938100268450615)
	I have a very similar device:  
	  
	https://www.youtube.com/watch?v=UDU-SyqXwQE  
	  
	Alas, the geometry of the screen still is a disaster. I had to do a lot of research in order to learn how to avoid what are the dangerous parts of a CRT screen (the anode), and how to calibrate the geometry and convergence of a 5½-in black-and-white TV set. At least the whole picture can enter the screen, with no overscanning. The deformation remains near the upper part, though. As far as I could figure this out, the whole device needs new capacitors, and I'm like: Oh, if I just knew how to handle a soldering iron...  
	  
	There is a (probably a Mexican) guy called Artemio Urbina, who found a way to write programs that actually are emulations of Super Nintendo games (SFC and SMC files). His most known project is the "240p Test Suite", useful for calibrating geometry and convergence of CRT screens. Not sure if ZSNES is able to run in a Raspberry Pi (it's compatible with Linux distributions, though, but it's becoming hard to use and find as the last version is for x-86 architectures, and they are obsolete already), but it would be useful for you.  
	  
	I use my small device as an auxiliary loud speaker (using the "Mic" and "Aux" plugs), and since it uses separated VHF and UHF plugs for antennas (80's device), I got them united by a pair of matching transformers, plugged in to a RF divider. And then, I plugged a single coaxial wire... first, to a Betamax VCR (It used to work, but not anymore... I wish I could find spare parts, though), and then to a digital-to-analog TV converter (here in Mexico we use ATSC, and used to use NTSC). Believe it or not, it worked. All what I have to do is to tune the "channel 3" (tuning it like an old radio, with a knob), and the picture is there!  
	  
	Then, I went extreme, and I got an HDMI-to-RCA converter on AliExpress (for less than 4 USD's), and a RCA-to-RF converter (I used to use a VCR as a temporary RCA-to-RF converter). Despite the bad geometry of the screen, the result is astounding. Now I can use my small TV as an auxiliary monitor, which is actually great. It'd be much greater if I could improve the definition and the geometry of that poor screen, but I'd need to get a same-size tube from an old computer monitor or video monitor (like Sony's PVM and BVM models) first.  
	  
	So, besides mechanical typewriters, I love CRT screens.
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/950938100268450615)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	- ![[Read It Later/attachments/51b5633ef2b1477fff4e5a3fcbabb660_MD5.jpg]]
		[Lucas Dul](https://www.blogger.com/profile/06562560826600046579)[March 4, 2022 at 9:30 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1646458212403#c738682771219281604)
		CRTs are pretty awesome. I didn't want to end up using an RF converter, so I was glad I was able to input composite instead. The screen you've got looks pretty good. I was not able to adjust horizontal overscan on my unit, so the right end of the frame cuts off. There is notable edge distortion with mine as well, that might just be the pitfall of small CRTs, I see it on a lot of them. The larger CRTs are big enough that the last quarter or so inch of screen is really quite trivial.
		[Delete](https://www.blogger.com/comment/delete/8221059337769683965/738682771219281604)
		[Replies](https://themechanicaltype.blogspot.com/2022/02/)
		[Reply](https://themechanicaltype.blogspot.com/2022/02/)
	- ![[Read It Later/attachments/ced8bf48208ff615fd12d6cfe31ded4d_MD5.jpg]]
		[Robin Heilschild 【蓋面】](https://www.blogger.com/profile/03429820251341371094)[March 5, 2022 at 11:21 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1646551314982#c5842641631456149117)
		Indeed, they are.  
		  
		Yes, it looks great.  
		  
		Try out adjusting the convergence rings, at the yoke of the tube.  
		  
		I see...  
		  
		Interesting.  
		Thanks for the information. I'll consider getting a 29-in CRT TV set some day.
		[Delete](https://www.blogger.com/comment/delete/8221059337769683965/5842641631456149117)
		[Replies](https://themechanicaltype.blogspot.com/2022/02/)
		[Reply](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
6. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[Jason S.](https://www.blogger.com/profile/18314537499518537004)[March 16, 2022 at 3:39 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1647470384612#c6508330552600097607)
	Is that outputting as 480i? Did you have to do much customisation to the OS/desktop environment to make it display content well?
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/6508330552600097607)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	- ![[Read It Later/attachments/51b5633ef2b1477fff4e5a3fcbabb660_MD5.jpg]]
		[Lucas Dul](https://www.blogger.com/profile/06562560826600046579)[March 16, 2022 at 4:13 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1647472424041#c8307954750945177943)
		It is I believe. It hangs off on the right end a bit, but I was able to configure the size of the task bar to all fit
		[Delete](https://www.blogger.com/comment/delete/8221059337769683965/8307954750945177943)
		[Replies](https://themechanicaltype.blogspot.com/2022/02/)
		[Reply](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
7. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[Aaron](https://www.blogger.com/profile/01262263971345544013)[June 5, 2022 at 6:34 PM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1654479268222#c6835229857346750604)
	I have the same model portable tv and I'm trying to make an analog input for it. I'm having trouble with tracking down the video signal input on the video amp board. I tried your method of splicing an RCA cable to probe it out with no luck.
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/6835229857346750604)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)
8. ![[Read It Later/attachments/f90a4ef3ab115c13d2343520b35037f9_MD5.png]]
	[restaurantes en Querétaro](https://www.blogger.com/profile/13265343030578126505)[January 21, 2025 at 9:55 AM](https://themechanicaltype.blogspot.com/2022/02/the-cyberdeck.html?showComment=1737482146492#c3819595963797531047)
	A Cyberdeck is a unique and versatile tech project that can serve a variety of functions. Whether you want to build a custom machine for programming, hacking, or just as a cool, portable computer, a cyberdeck offers flexibility and creativity. While building one can take some time and effort, it's a rewarding project that combines electronics, coding, and creative design. If you're interested, there are plenty of guides and resources to get started! I can recommend you a site [sell laptop near me](https://www.gadgetsalvation.com/sell-laptop)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)[Delete](https://www.blogger.com/comment/delete/8221059337769683965/3819595963797531047)
	[Replies](https://themechanicaltype.blogspot.com/2022/02/)
	[Reply](https://themechanicaltype.blogspot.com/2022/02/)

[Add comment](https://themechanicaltype.blogspot.com/2022/02/)

<iframe allowtransparency="allowtransparency" class="blogger-iframe-colorize blogger-comment-from-post" frameborder="0" height="85px" id="comment-editor" name="comment-editor" src="https://www.blogger.com/comment/frame/8221059337769683965?po=1425554499311020110&amp;hl=en&amp;saa=85391&amp;origin=https%3A%2F%2Fthemechanicaltype.blogspot.com&amp;skin=contempo&amp;blogspotRpcToken=3174959" width="100%" style="display: block;" data-resized="true"></iframe>

Load more...

#### Post a Comment<iframe id="aswift_2" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame2"&gt;</iframe> 

### Popular posts from this blog

### [The Blog](https://themechanicaltype.blogspot.com/2019/09/a-brief-introduction-to-insanity.html)

[![[Read It Later/attachments/e38a8e851254ac0b8bf6932ea74dc7f6_MD5.jpg]]](https://themechanicaltype.blogspot.com/2019/09/a-brief-introduction-to-insanity.html)

A blog by a typewriter repair tech, for typewriter people. Embracing Analog. Is it time to update the introduction to this blog?  I think so.  I want you to close your eyes and imagine a massive library, vast and expansive in the knowledge it covers.  Please note that I don't actually want you to close your eyes, because then you wouldn't be able to read this.  Just close your mind's eye...your...pineal gland?  Anyway, imagine that big beautiful library has a catch.  Not a single dot of information in all those volumes has any practical use.  Now I also want you to imagine that most of the shelves are dry-rotted and the books appear in huge heaps all over the place without the slightest, faintest illusion of order.  As if it were ground zero of the "nuke of knowledge," the hazy aftermath of a several literary-megaton violent enlightenment that created this monumental catastrophe.   That library is me.  Well, no, I am not a ...[Read more](https://themechanicaltype.blogspot.com/2019/09/a-brief-introduction-to-insanity.html "The Blog")

### [The “Charming?” Yet awful Typecast Typewriter (updated)](https://themechanicaltype.blogspot.com/2017/12/the-charming-yet-awful-typecast.html)

[![[Read It Later/attachments/03a8b2ceae2d4fc3ac8ee9736d6407a6_MD5.jpg]]](https://themechanicaltype.blogspot.com/2017/12/the-charming-yet-awful-typecast.html)

A couple of years ago, the Michaels craft store began to sell a machine made by “We Are Memory Keepers.”  It is the Typecast Typewriter, and it costs about $170. Let me cut to the chase: this machine is awful.  The construction is flimsy and cheap, the action is stiff, and the alignment is the worst ever.  So if you wanna buy it, click below!!! https://www.michaels.com/we-r-memory-keepers-typecast-typewriter-mint/10507749.html I am not alone in my views, as many other enthusiasts share my stance.  This machine gives the typewriter a bad reputation among many people, especially craft people, who enjoy bearing the name “key chopper” for cutting the keys off of machines a hundred years old just to make a piece of jewelry.  When they are done, the rest of the machine is thrown away.  I really truly despise the lack of respect given to these historical artifacts, and the Typecast only seems to mock them, by perpetuating the inaccurate stere...[Read more](https://themechanicaltype.blogspot.com/2017/12/the-charming-yet-awful-typecast.html "The “Charming?” Yet awful Typecast Typewriter (updated)")

[Powered by Blogger](https://www.blogger.com/)

<iframe id="aswift_3" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame3"&gt;</iframe> 

### Magic Searcher Box Thing

<iframe id="aswift_4" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame4"&gt;</iframe> 

[![[Read It Later/attachments/8a57075c20e9845e4a57c8d0da5f8a90_MD5.jpg]]](https://www.blogger.com/profile/06562560826600046579)

[Lucas Dul](https://www.blogger.com/profile/06562560826600046579)

Typewriter Repair Guru, and Avid Reader.

[Visit profile](https://www.blogger.com/profile/06562560826600046579)

<iframe id="aswift_5" style="height: 1px !important; max-height: 1px !important; max-width: 1px !important; width: 1px !important;">&lt;iframe id="google_ads_frame5"&gt;</iframe> 

### Archive

- [July 21001](https://themechanicaltype.blogspot.com/2100/07/)
- [June 20231](https://themechanicaltype.blogspot.com/2023/06/)
- [April 20231](https://themechanicaltype.blogspot.com/2023/04/)
- [December 20221](https://themechanicaltype.blogspot.com/2022/12/)
- [November 20222](https://themechanicaltype.blogspot.com/2022/11/)
- [May 20221](https://themechanicaltype.blogspot.com/2022/05/)
- [March 20222](https://themechanicaltype.blogspot.com/2022/03/)
- [February 20221](https://themechanicaltype.blogspot.com/2022/02/)
- [January 20221](https://themechanicaltype.blogspot.com/2022/01/)
- [October 20211](https://themechanicaltype.blogspot.com/2021/10/)

- [July 20213](https://themechanicaltype.blogspot.com/2021/07/)
- [June 20211](https://themechanicaltype.blogspot.com/2021/06/)
- [April 20211](https://themechanicaltype.blogspot.com/2021/04/)
- [February 20215](https://themechanicaltype.blogspot.com/2021/02/)
- [January 20211](https://themechanicaltype.blogspot.com/2021/01/)
- [December 20201](https://themechanicaltype.blogspot.com/2020/12/)
- [October 20201](https://themechanicaltype.blogspot.com/2020/10/)
- [July 20204](https://themechanicaltype.blogspot.com/2020/07/)
- [May 20201](https://themechanicaltype.blogspot.com/2020/05/)
- [April 20201](https://themechanicaltype.blogspot.com/2020/04/)
- [March 20201](https://themechanicaltype.blogspot.com/2020/03/)
- [February 20202](https://themechanicaltype.blogspot.com/2020/02/)
- [December 20191](https://themechanicaltype.blogspot.com/2019/12/)
- [November 20191](https://themechanicaltype.blogspot.com/2019/11/)
- [October 20195](https://themechanicaltype.blogspot.com/2019/10/)
- [September 201911](https://themechanicaltype.blogspot.com/2019/09/)
- [August 20195](https://themechanicaltype.blogspot.com/2019/08/)
- [July 20192](https://themechanicaltype.blogspot.com/2019/07/)
- [June 20191](https://themechanicaltype.blogspot.com/2019/06/)
- [April 20192](https://themechanicaltype.blogspot.com/2019/04/)
- [March 20192](https://themechanicaltype.blogspot.com/2019/03/)
- [December 20181](https://themechanicaltype.blogspot.com/2018/12/)
- [September 20181](https://themechanicaltype.blogspot.com/2018/09/)
- [July 20181](https://themechanicaltype.blogspot.com/2018/07/)
- [June 20182](https://themechanicaltype.blogspot.com/2018/06/)
- [April 20184](https://themechanicaltype.blogspot.com/2018/04/)
- [March 20184](https://themechanicaltype.blogspot.com/2018/03/)
- [February 20184](https://themechanicaltype.blogspot.com/2018/02/)
- [January 20183](https://themechanicaltype.blogspot.com/2018/01/)
- [December 20178](https://themechanicaltype.blogspot.com/2017/12/)

Show more Show less

### Labels

- [1920s Underwood 5](https://themechanicaltype.blogspot.com/search/label/1920s%20Underwood%205)
- [1923 Underwood 3 bank](https://themechanicaltype.blogspot.com/search/label/1923%20Underwood%203%20bank)
- [1930 Royal Portable](https://themechanicaltype.blogspot.com/search/label/1930%20Royal%20Portable)
- [1950 Smith-Corona Silent 5](https://themechanicaltype.blogspot.com/search/label/1950%20Smith-Corona%20Silent%205)
- [Lego Typewriter](https://themechanicaltype.blogspot.com/search/label/Lego%20Typewriter)
- [maintenance](https://themechanicaltype.blogspot.com/search/label/maintenance)
- [Repair](https://themechanicaltype.blogspot.com/search/label/Repair)
- [Royal Model 10](https://themechanicaltype.blogspot.com/search/label/Royal%20Model%2010)
- [Royal Portable](https://themechanicaltype.blogspot.com/search/label/Royal%20Portable)
- [Typewriter](https://themechanicaltype.blogspot.com/search/label/Typewriter)

- [Typewriters](https://themechanicaltype.blogspot.com/search/label/Typewriters)
- [Underwood Portable](https://themechanicaltype.blogspot.com/search/label/Underwood%20Portable)

Show more Show less

### [Report Abuse](https://www.blogger.com/go/report-abuse)

❌ 未收藏