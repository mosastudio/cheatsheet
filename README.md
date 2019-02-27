## Cheat Sheet

This is my cheet sheet.

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
* [Website on Bitbucket](https://confluence.atlassian.com/bitbucket/publishing-a-website-on-bitbucket-cloud-221449776.html)
  * the repository name: {accountname}.bitbucket.io
* [TIOBE Index](https://www.tiobe.com/tiobe-index/), the programming language of XXXX
* [browserling, conversion, encrypt, decrypt, ..](https://www.browserling.com/tools/)
* [Epoch & Unix Timestamp Conversion Tools](https://www.epochconverter.com/)
* [Jeffrey's Image Metadata Viewer](http://exif.regex.info/exif.cgi)
* [JSON to CSV](https://json-csv.com/)
* [TCP and UDP port numbers](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
* Font
  * [IDEO fontmap](http://fontmap.ideo.com)
  * [Google Fonts](https://fonts.google.com)
* Color
  * [name that color](http://chir.ag/projects/name-that-color/)

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
       0 = 0000 0000
       1 = 0000 0001
     127 = 0111 1111
    -128 = 1000 0000
    -127 = 1000 0001
      -1 = 1111 1111
```

* shift operator

```c
    char a = 32;
    char b = -32;

    char c = a;
    char d = b;
    // c: 0010 0000    d = 1110 0000
    c = a << 1;
    d = b << 1;
    // c: 0100 0000    d = 1100 0000
    c = a >> 1;
    d = b >> 1;
    // c: 0001 0000    d = 1111 0000
```

* Other bitwise operators

```c
    ~a       // bitwise NOT
    a & b    // bitwise AND
    a | b    // bitwise OR
    a ^ b    // bitwise XOR
```

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

* const

[Hint: Read it backwards](https://stackoverflow.com/questions/1143262/what-is-the-difference-between-const-int-const-int-const-and-int-const)

| example | def. | equal to |
|-|-|-|
| int * | pointer to int | |
| int const * | pointer to const int | const int * |
| int * const | const pointer to int | |
| int const * const | const pointer to const int | const int * const |

## More
* [Git](git.md)
* [iOS App](iosapp.md)
* [JavaScript](javascript.md)
