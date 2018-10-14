## iOS App

## Apple
* [App Store Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
* [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
* [OS Percentage](https://developer.apple.com/support/app-store/)
* [Device Compatibility](https://developer.apple.com/library/archive/documentation/DeviceInformation/Reference/iOSDeviceCompatibility/DeviceCompatibilityMatrix/DeviceCompatibilityMatrix.html)

## Other

* [iOS Support Matrix, device, iOS version](http://iossupportmatrix.com/)
* [iPhone Resolutions](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)
* [Material icons, Google](https://material.io/tools/icons/)
* [App Icon Maker](http://appiconmaker.co/)
* [App Screenshot Maker](https://appinstitute.com/app-screenshot-maker/)

| |bounds, scale|nativeBounds, nativeScale|
|-|-|-|
|iPhone 7+|414x736, 3|1080x1920, 2.608696|
|iPhone 7+(&)|375x667, 3|1080x1920, 2.88|
|iPhone X|375x812, 3|1125x2436, 3|

&: iPhone Settings -> Display & Brightness -> View -> Zoomed

## Xcode

* Save disk space, [SO Thread](https://apple.stackexchange.com/questions/287307/reduce-size-of-the-xcode-application)
  * DerivedData
  * iOS DeviceSupport
  * Archives
  * Simulators
* Save disk space, install [DevCleaner](https://itunes.apple.com/us/app/devcleaner/id1388020431) on Mac
* check the files on an actual iOS device
  * Launch Xcode
  * Window
  * Devices and Simulators
  * Devices, select your iPhone / iPad
  * Installed App, tap your app
  * Gear icon
  * Download Container
  * Go to Finder, "Show Package Contents"
* There is error when launching app in simulator
  * quit Xcode
  * quit iOS simulator
  * backup the files in ~/Library/Developer/Xcode/DerivedData/{YourAppName}-*/

## How-to

| |iPhone|iPhone X|
|-|-|-|
|Power Off| |(1) Volume Up -> Volume Down -> Power (Keep Pressing), or (2) Volume Up + Power (Keep Pressing), or (3) Volume Down + Power (Keep Pressing) |
|Snapshot|Home + Power|Volume Up + Power|

## WWDC Sessions

## Objective-C

## Swift
