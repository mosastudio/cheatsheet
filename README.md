## Cheat Sheet

This is my cheet sheet.

## Programming

* [Epoch & Unix Timestamp Conversion Tools](https://www.epochconverter.com/)
* [Jeffrey's Image Metadata Viewer](http://exif.regex.info/exif.cgi)
* [JSON to CSV](https://json-csv.com/)
* [TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)

## Mac OS

* [Homebrew](https://brew.sh/), The missing package manager for macOS
  * Install Homebrew
    * $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  * command line
    * $ brea update
    * $ brew install
  * ex. mongodb, nvm, wget, ..

## Other

* interview
  * [LeetCode](http://leetcode.com/)
* Code together
  * https://coderpad.io/
  * http://collabedit.com/
  * https://codeshare.io/
* Two's complement, ex. Eight-bit signed integers
```c
    0    = 0000 0000
    1    = 0000 0001
    127  = 0111 1111
    -128 = 1000 0000
    -127 = 1000 0001
    -1   = 1111 1111
```
* shift operator
```c
    char a = 32;
    char b = -32;

    char c = a;
    char d = b;
    // c: 0x 20    d = 0x e0
    c = a << 1;
    d = b << 1;
    // c: 0x 40    d = 0x c0
    c = a >> 1;
    d = b >> 1;
    // c: 0x 10    d = 0x f0
```
* 64 bit
| |ILP32|LP64 (ex. mac OS, iOS, Linux)|LLP64 (ex. Win)|
|-|-|-|-|
|pointer|32 bit|64 bit|64 bit|
|int|32 bit|32 bit|32 bit|
|long|32 bit|64 bit|32 bit|
|long long|64 bit|64 bit|64 bit|

## More
* [Git](git.md)
* [iOS App](iosapp.md)
* [JavaScript](javascript.md)
