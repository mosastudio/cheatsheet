## Cheat Sheet

This is my cheat sheet.

[URL and shortcuts](shortcut.md)

## In detail

* [iOS App](iosapp.md)
* [JavaScript](javascript.md)
* [C++](https://github.com/mosastudio/cppexample)
  * [macOS, Visual Studio Code](https://www.youtube.com/watch?v=zIIYN_PyUAM)
  * [macOS, Visual Studio Code, official guideline](https://code.visualstudio.com/docs/languages/cpp)
* [macOS](macos.md)
* [Git](git.md)

## Programming

* Firebase
  * [Document](https://firebase.google.com/products/)
  * [Console](https://console.firebase.google.com/)
  * [Privacy Policy Generator](https://app-privacy-policy-generator.firebaseapp.com/)
  * AdMob
  * "Upload missing dSYMs to see crashes from 1 versions", if failed to upload dSYM automatically
    * go to "App Store Connect" -> theApp > Activity > theBuildNumber > Download dSYM
    * Firebase console, upload it
* Facebook
  * [Developers](https://developers.facebook.com/)
  * [Facebook Audience Network](https://developers.facebook.com/docs/audience-network/)
* [TIOBE Index](https://www.tiobe.com/tiobe-index/), the programming language of XXXX
* View, Convert
  * [browserling, conversion, encrypt, decrypt, ..](https://www.browserling.com/tools/)
  * [Epoch & Unix Timestamp Conversion Tools](https://www.epochconverter.com/)
  * [JSON to CSV](https://json-csv.com/)
  * [Audio Converter](https://online-audio-converter.com/tw/)
* [TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
* Image
  * [Jeffrey's Image Metadata Viewer](http://exif.regex.info/exif.cgi)
  * [pixlr editor](https://pixlr.com/editor/), Chrome, with Flash enabled
* Font
  * [IDEO fontmap](http://fontmap.ideo.com)
  * [Google Fonts](https://fonts.google.com)
* Color
  * [name that color](http://chir.ag/projects/name-that-color/)
  * [coolors](https://coolors.co/)
* Icons
  * [Material icons, Google](https://material.io/tools/icons/)
* ASCII
  * [wiki](https://en.wikipedia.org/wiki/ASCII)
  * mac shell, check the binary file, $ od -t x1 -N 32 'filename.ext'

## System Configuration

* Delete old Google profile photo
  * [Ref.](https://support.google.com/photos/thread/143925?hl=en)
  * go to: https://get.google.com/albumarchive

## OpenCL

* [OpenCL Programming Guide](https://www.amazon.com/OpenCL-Programming-Guide-Aaftab-Munshi/dp/0321749642)
  * [Installation](https://code.google.com/archive/p/opencl-book-samples/wikis/Installation.wiki)
  * [Samples](https://github.com/bgaster/opencl-book-samples)
    * [HelloWorld](https://github.com/bgaster/opencl-book-samples/tree/master/src/Chapter_2/HelloWorld)
    * [OpenCLInfo](https://github.com/bgaster/opencl-book-samples/tree/master/src/Chapter_3/OpenCLInfo)

## Web, frontend

* w3schools
  * [Responsive image grid](https://www.w3schools.com/howto/howto_css_image_grid_responsive.asp)
  * [Image grid](https://www.w3schools.com/howto/howto_js_image_grid.asp)

* [Website on Bitbucket](https://confluence.atlassian.com/bitbucket/publishing-a-website-on-bitbucket-cloud-221449776.html)
  * the repository name: {accountname}.bitbucket.io

## Other

* interview
  * [LeetCode](http://leetcode.com/)
  * [Companies in Taiwan](https://www.twincn.com/)

* Code together
  * https://coderpad.io/
  * http://collabedit.com/
  * https://codeshare.io/

* 64 bit

| |ILP32|LP64 (ex. mac OS, iOS, Linux)|LLP64 (ex. Win)|
|-|-|-|-|
|pointer|32 bit|64 bit|64 bit|
|int|32 bit|32 bit|32 bit|
|long|32 bit|64 bit|32 bit|
|long long|64 bit|64 bit|64 bit|

* Endianness

int32_t	longVar	= 0x0a0b0c0d;

| memory at offset | Big-Endian | Little-Endian |
|-|-|-|
| +0 | 0a | 0d |
| +1 | 0b | 0c |
| +2 | 0c | 0b |
| +3 | 0d | 0a |
