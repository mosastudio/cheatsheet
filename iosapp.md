## iOS App

## Apple
* [Apple Developer](https://developer.apple.com/)
* [App Store Connect](https://appstoreconnect.apple.com/)
* [App Store Review Guidelines](https://developer.apple.com/app-store/review/guidelines/)
* [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/)
* [iOS Data Storage Guidelines](https://developer.apple.com/icloud/documentation/data-storage/index.html)
* [OS Percentage](https://developer.apple.com/support/app-store/)
  * iOS 12 - 50%, iOS 11 - 39%, earlier - 11% (Oct. 10 2018)
* [Device Compatibility](https://developer.apple.com/library/archive/documentation/DeviceInformation/Reference/iOSDeviceCompatibility/DeviceCompatibilityMatrix/DeviceCompatibilityMatrix.html)
* [Download](https://developer.apple.com/download/)
* [More Downloads](https://developer.apple.com/download/more/)

## Other

* [iOS Support Matrix, device, iOS version](http://iossupportmatrix.com/)
* Spec of [iPhone](https://everymac.com/systems/apple/iphone/index-iphone-specs.html), [iPad](https://everymac.com/systems/apple/ipad/index-ipad-specs.html), [iPod](https://everymac.com/systems/apple/ipod/index-ipod-specs.html)
* [iPhone Resolutions](https://www.paintcodeapp.com/news/ultimate-guide-to-iphone-resolutions)

| |bounds, scale|nativeBounds, nativeScale|
|-|-|-|
|iPhone 7+|414x736, 3|1080x1920, 2.608696|
|iPhone 7+(&)|375x667, 3|1080x1920, 2.88|
|iPhone X|375x812, 3|1125x2436, 3|

&: iPhone Settings -> Display & Brightness -> View -> Zoomed

* [OSStatus, Apple API errors](https://www.osstatus.com/)
* [Material icons, Google](https://material.io/tools/icons/)
* [App Icon Maker](http://appiconmaker.co/)
* [App Screenshot Maker](https://appinstitute.com/app-screenshot-maker/)
* [App Store Ranking](https://www.qimai.cn/rank/index/brand/all/genre/6013/device/iphone/country/us/date/2018-11-11)
* NSDateFormatter
  * [full list](https://waracle.com/iphone-nsdateformatter-date-formatting-table/)
  * [online editor](http://nsdateformatter.com)

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
* Keep crashing, when launching app in simulator
  * quit Xcode
  * quit iOS simulator
  * backup , and delete the files in ~/Library/Developer/Xcode/DerivedData/{YourAppName}-*/

## Submitting app to App Store

* UDID
  * [iTunes](https://www.igeeksblog.com/how-to-find-iphone-udid-number/)
  * [Xcode](https://www.idownloadblog.com/2018/11/20/how-to-find-udid-iphone-xs-max-xr/)
* TestFlight, "Missing Compliance" for internal testing
  * [Ref.](https://stackoverflow.com/questions/35841117/missing-compliance-in-status-when-i-add-built-for-internal-testing-in-test-fligh) info.plist, <key>ITSAppUsesNonExemptEncryption</key><false/>
* "“Invalid Bundle Structure - The binary file ‘xxxxxxxx.a’ is not permitted. Your app can’t contain standalone executables or libraries..." in Application Loader
  * the target setting => Build Phases => check "Copy Bundle Resources", the .a file or the folder, should not be listed.
* [App Center](https://appcenter.ms/apps)

## CocoaPods

* [CocoaPods](https://cocoapods.org/), it is a dependency manager for ..
* Install
  * $ sudo gem install cocoapods
* command line, ex.

```sh
# Xcode -> "Create a new Xcode project" -> name it as "temp" -> quit Xcode

$ cd temp

$ pod init
# a new file, "Podfile", is created

# edit the file

$ pod install
# a new file, "Podfile.lock", is created

$ open temp.xcworkspace

# And, some other commands
$ pod help
$ pod outdated
$ pod update

```

## How-to

| |iPhone|iPhone X|
|-|-|-|
|Power Off| |(1) Volume Up -> Volume Down -> Power (Keep Pressing)|
|Power Off| |(2) Volume Up + Power (Keep Pressing)|
|Power Off| |(3) Volume Down + Power (Keep Pressing) |
|Snapshot|Home + Power|Volume Up + Power|


## Tutorial

* appcoda
  * [Learn iOS Programming](http://www.appcoda.com/ios-programming-course/) Check the new API -> modify the sample code -> run it
  * [Documenting](https://www.appcoda.com/documenting-source-code-in-xcode/)
* [KKBOX](https://legacy.gitbook.com/book/zonble/kkbox-ios-dev/details)
  * in ARC, retain, release, autorelease, retainCount is forbidden
  * {3.1}, {3.2}, reference count, "所謂的 auto-release 其實也沒有多麼自動，而是說，在這一輪 run loop中我們先不釋放這個物件，讓這個物件可以在這一輪 run loop 中都可以使用，但是先打上一個標籤，到了下一輪 run loop 開始時，讓 runtime 判斷有哪些前一輪runloop 中被標成是 auto-release 的物件，這個時候才減少retain count 決定是否要釋放物件。"
  * {4.} retain cycle, for ex. timer -> target(self) -> timer
  * {5.}
    * "所以我們要注意，viewDidLoad 並不是 UIViewController 的 Initializer，—雖然我們在開始使用某個 view controller 的時候，一定會呼叫到一次viewDidLoad ，我們也通常會在這個地方，做一些初始化這個 view controller的事情—但 viewDidLoad 是有機會在 View Controller 的 Life Cycle 中被重複呼叫好幾遍—在建立了 view 之後，view 也可以再次指向 nil，所以 view controller 可能會被重複釋放與載入 view， viewDidLoad也會被重複呼叫。"
    * "view controller 被放到最上層時，會被呼叫到 viewWillAppear: 以及 viewDidAppear: ，離開最上層時，會呼叫 viewWillDisappear: 與 viewDidDisappear:"
  * {12}
* [The University of Chicago](http://uchicago.mobi/sessions/) Swift

* [raywenderlich](https://www.raywenderlich.com/ios/)
  * [Custom UISlider](https://www.raywenderlich.com/2715-photoshop-tutorial-for-developers-creating-a-custom-uislider)
  * [Creating a Static Library](https://www.raywenderlich.com/2658-creating-a-static-library-in-ios-tutorial)
* [NYTimes Objective-C Style Guide](https://github.com/NYTimes/objective-c-style-guide)
* [Swift, language guide](https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html)
* [Swift 2.2](https://itisjoe.gitbooks.io/swiftgo/content/)
* [Online Swift Playground](http://online.swiftplayground.run)

## Threading

* Dispatch
  * [dispatch_async](https://developer.apple.com/documentation/dispatch/1453057-dispatch_async?language=objc), async, returns immediately
  * dispatch_sync, do not call on the same queue
  * [dispatch_get_main_queue](https://developer.apple.com/documentation/dispatch/1452921-dispatch_get_main_queue?language=objc)
  * [dispatch_get_global_queue](https://developer.apple.com/documentation/dispatch/1452927-dispatch_get_global_queue?language=objc), high, default, low, background

```objective-c
    dispatch_async(dispatch_get_main_queue(), ^{
    });
    dispatch_async(dispatch_get_global_queue(DISPATCH_QUEUE_PRIORITY_DEFAULT, 0), ^{
    });
```

* NSOperationQueue
  * [NSOperationQueue]()
    * addOperation
    * maxConcurrentOperationCount
  * [NSBlockOperation](https://developer.apple.com/documentation/foundation/nsblockoperation?language=objc) / NSOperation
    * cancel
    * addDependency, removeDependency

* @synchronized() {}

* dispatch_semaphore_t
  * dispatch_semaphore_create(..)
  * dispatch_semaphore_wait(.. , ..)
  * dispatch_semaphore_signal(..)

* retain cycles

```objective-c
// cycle
    [obj theMethod:^{
        [obj doSomething];
    }];
// using __weak
    __weak typeof(self) weakSelf = self;
    [self theMethod:^{
        __strong typeof(self) strongSelf = weakSelf;
        if (strongSelf) {
            [strongSelf doSomething];
        } else {
            // ..
        }
    }];
```

## HTTP, RESTful API

ex. https://developer.apple.com:443/documentation/uikit/uiviewcontroller?language=objc

|def.|value|
|-|-|
|scheme|https|
|host|developer.apple.com|
|port|443|
|path|/documentation/uikit/uiviewcontroller|
|query|language=objc|

* request, client -> server
  * [method](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods), headers (inc. token, Content-Type), body

|method|usage|
|-|-|
|POST|Create|
|GET|Read|
|PUT|Update|
|DELETE|Delete|
|HEAD|Read, but no response body|

* response, server -> client
  * [status code](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status), headers (inc. Content-Type, Content-Length), body

|status code|def.|
|-|-|
|1xx|Information|
|2xx|Success. 200: OK, 201: Created, 202: Accepted, ..|
|3xx|Redirection|
|4xx|Client error. 400: Bad Request, 404: Not Found, ..|
|5xx|Server error. 500: Internal Server Error, ..|

* [NSURLSession tutorial](https://www.raywenderlich.com/567-urlsession-tutorial-getting-started)
  * NSURLRequest
  * NSURLSessionTask
    * NSURLSessionDataTask
      * NSURLSessionUploadTask
    * NSURLSessionDownloadTask

* Stop using NSURLConnection

* [JSON Serialization](https://developer.apple.com/swift/blog/?id=37)

## Webpage, WebView

* Webpage debugging
  * debug a webpage in the mac: Safari (Macbook) => Preferences => Advanced => "Show Developer menu in menu bar"
  * debug a webpage in the iPhone (inc. Safari, and WKWebView in app): Setting (iPhone) => Safari => Advanced => "Web Inspector"
  * check the log: Safari (Macbook) => Developer => the name of iPhone or Macbook

* "Transport security has blocked a cleartest HTTP (http://) ....." => [Ref.](https://stackoverflow.com/questions/31254725/transport-security-has-blocked-a-cleartext-http)

* Enable JavaScript
  * Enable it by iOS Conf.: Setting (iPhone) => Safari => Advanced => "JavaScript"
  * Enable it bt code: WKPreferences.javaScriptEnabled

* Disable zoom in WKWebView
  * [Ref](https://stackoverflow.com/questions/40452034/disable-zoom-in-wkwebview/41741125)

## Keyboard

* [Ref](https://developer.apple.com/library/archive/documentation/StringsTextFonts/Conceptual/TextAndWebiPhoneOS/KeyboardManagement/KeyboardManagement.html)

## UIKit

```objective-c
@interface UIViewController : UIResponder
- (void)viewDidLoad;
- (void)viewWillAppear:(BOOL)animated;
- (void)viewDidAppear:(BOOL)animated;
- (void)viewWillDisappear:(BOOL)animated;
- (void)viewDidDisappear:(BOOL)animated;
- (void)viewWillLayoutSubviews;
- (void)viewDidLayoutSubviews;
@end

@interface UIResponder : NSObject
- (void)touchesBegan:(NSSet<UITouch *> *)touches withEvent:(nullable UIEvent *)event;
- (void)touchesMoved:(NSSet<UITouch *> *)touches withEvent:(nullable UIEvent *)event;
- (void)touchesEnded:(NSSet<UITouch *> *)touches withEvent:(nullable UIEvent *)event;
- (void)touchesCancelled:(NSSet<UITouch *> *)touches withEvent:(nullable UIEvent *)event;
@end

@interface UIControl : UIView
- (BOOL)beginTrackingWithTouch:(UITouch *)touch withEvent:(nullable UIEvent *)event;
- (BOOL)continueTrackingWithTouch:(UITouch *)touch withEvent:(nullable UIEvent *)event;
- (void)endTrackingWithTouch:(nullable UITouch *)touch withEvent:(nullable UIEvent *)event;
- (void)cancelTrackingWithEvent:(nullable UIEvent *)event;

- (void)addTarget:(nullable id)target action:(SEL)action forControlEvents:(UIControlEvents)controlEvents;
@end

@interface UIView : UIResponder
@property(nonatomic,getter=isExclusiveTouch) BOOL       exclusiveTouch __TVOS_PROHIBITED;
@end

typedef NS_OPTIONS(NSUInteger, UIControlEvents) {
    UIControlEventTouchDown                                         = 1 <<  0,      // on all touch downs
    UIControlEventTouchUpInside                                     = 1 <<  6,
    UIControlEventTouchUpOutside                                    = 1 <<  7,

    UIControlEventValueChanged                                      = 1 << 12,     // sliders, etc.

    UIControlEventAllEvents                                         = 0xFFFFFFFF
};

@interface UILabel : UIView
@end
@interface UITextField : UIControl <UITextInput>
@end
@interface UITextView : UIScrollView <UITextInput>
@end
```

## Extensions

* [Limitations of custom iOS keyboards](https://medium.com/@inFullMobile/limitations-of-custom-ios-keyboards-3be88dfb694)
* [Shared User Defaults](https://medium.com/ios-os-x-development/shared-user-defaults-in-ios-3f15cd2c9409)

## Localization

* [Tutorial](https://www.raywenderlich.com/250-internationalizing-your-ios-app-getting-started)
* .lproj
  * Base.lproj
  * zh-hans.lproj
  * zh-hant.lproj
* .strings
  * Localizable.strings
  * InfoPlist.strings

## Common

* preprocessor
  * Objective-C: "Preprocessor Macros"
  * Swift: "Active Compilation Conditions"
* LaunchScreen.xib
  * O: UIImageView, UILabel, ..
  * X: custom subclass
  * X: UIWebView
  * ?: localization (not sure, there seems to be much limitation)

* Background mode
  * [Apple](https://developer.apple.com/library/archive/documentation/iPhone/Conceptual/iPhoneOSProgrammingGuide/BackgroundExecution/BackgroundExecution.html)
  * [raywenderlich](https://www.raywenderlich.com/5817-background-modes-tutorial-getting-started)
  * (related) Finite-Length Tasks, UIBackgroundTaskIdentifier
  * Xcode, Targets -> Capabilities -> Background Modes
    * Audio
    * Location updates
    * External accessory communication, for MFi devices
    * Uses Bluetooth LE accessories, act as bluetooth-central. To scan in the background, the app need to listen for particular BLE service
    * Remote notifications

* Sorting

```objective-c
NSMutableArray *array = [NSMutableArray arrayWithObjects:@"-7.1", @"23", @"12", @"3.5", @"-11", nil];
[array sortUsingComparator:^NSComparisonResult(id  _Nonnull obj1, id  _Nonnull obj2) {
    return ((fabs([obj1 doubleValue]) < fabs([obj2 doubleValue])) ? NSOrderedAscending : NSOrderedDescending);
}];
// 3.5    -7.1    -11    12    23
```

```Swift
let array = [-7.1, 23, 12, 3.5, -11]

// write a normal function of the correct type
func sortCustom(_ v1: Double, _ v2: Double) -> Bool {
    return abs(v1) < abs(v2)
}
var sorted1 = array.sorted(by: sortCustom)

// Closure Expression Syntax
var sorted2 = array.sorted(by: { (v1: Double, v2: Double) -> Bool in
    return abs(v1) < abs(v2)
})
// written on a single line
// var sorted2 = array.sorted(by: { (v1: Double, v2: Double) -> Bool in return abs(v1) < abs(v2) })

// Inferring Type From Context
var sorted3 = array.sorted(by: { v1, v2 in
    return abs(v1) < abs(v2)
})
// written on a single line
// var sorted3 = array.sorted(by: { v1, v2 in return abs(v1) < abs(v2) })

// Implicit Returns from Single-Expression Closures
var sorted4 = array.sorted(by: { v1, v2 in
    abs(v1) < abs(v2)
})
// written on a single line
// var sorted4 = array.sorted(by: { v1, v2 in abs(v1) < abs(v2) })

// Shorthand Argument Names
var sorted5 = array.sorted(by: { abs($0) < abs($1) })

var sorted6 = array.sorted(by: < )

// sorted1, sorted2, sorted3, sorted4, sorted5: [3.5, -7.1, -11, 12, 23]
// sorted6: [-11, -7.1, 3.5, 12, 23]
```

* NSLog, [format specifiers](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/Strings/Articles/formatSpecifiers.html)

| Specifier | type | Description |
| - | - | - |
| %% | | '%' |
| %@ | Objective-C object | ex. NSString * ,  NSDictionary * , NSError *|
| - | - | - |
| %d | int | signed 32-bit integer |
| %u | unsigned int | unsigned 32-bit integer |
| %x | unsigned int | printed in hexadecimal |
| %02x | unsigned char | for ex, print the bytes of NSData * |
| %f | double | 64-bit floatinf-point number |
| %c | unsigned char | 8-bit unsigned character |
| %C | unichar | 16-bit UTF-16 code unit, NSString *, characterAtIndex: |
| %s | | Null-terminated array of 8-bit unsigned characters. |
| %p | void * | printed in hexadecimal, with a leading 0x. |
| - | - | - |
| l, ll | | length modifier |
| %ld | long | |
| %lu | unsigned long | |
| %lld | long long | |
| %llu | unsigned long long | |
| - | - | - |
| %f | CGFloat | |
| %ld | (long)NSInteger | |
| %lu | (unsigned long)NSUInteger | |
| %zd | NSInteger | |
| %tu | NSUInteger | |
| - | - | - |
| %1$d, %2$@ | - | positional specifier |

```objective-c
    int intValue = 1;
    NSLog(@"%4d", intValue);       // "   1"
    NSLog(@"%04d", intValue);      // "0001"
    intValue = -1;
    NSLog(@"%4d", intValue);       // "  -1"
    NSLog(@"%04d", intValue);      // "-001"
    double doubleValue = 30.037;
    NSLog(@"%.2f", doubleValue);   // "30.04"
    NSLog(@"%8.2f", doubleValue);  // "   30.04"
    NSLog(@"%08.2f", doubleValue); // "00030.04"
```

* init methods

```objective-c
- (id)init {
    self = [super init];
    if (self) {
        // ....
    }
    return self;
}
```

* animation, using UIViewPropertyAnimator
  * [Ref](https://medium.com/@daniel_larsson/interactive-animations-with-uiviewpropertyanimator-284580951c62)

## Drawing

* [Apple, iOS Drawing Concepts](https://developer.apple.com/library/archive/documentation/2DDrawing/Conceptual/DrawingPrintingiOS/GraphicsDrawingOverview/GraphicsDrawingOverview.html)
* raywenderlich, objective c
  * [line, rect, gradient](https://www.raywenderlich.com/2746-core-graphics-tutorial-lines-rectangles-and-gradients)
  * [shadow, gloss](https://www.raywenderlich.com/2745-core-graphics-tutorial-shadows-and-gloss)
  * [arc, path](https://www.raywenderlich.com/2743-core-graphics-tutorial-arcs-and-paths)
  * [gloss](https://www.raywenderlich.com/2744-core-graphics-tutorial-glossy-buttons)
  * [pattern](https://www.raywenderlich.com/2742-core-graphics-tutorial-patterns)
  * [curve, layer](https://www.raywenderlich.com/2741-core-graphics-tutorial-curves-and-layers)
* raywenderlich, Swift
  * [part 1](https://www.raywenderlich.com/411-core-graphics-tutorial-part-1-getting-started)
  * [part 2](https://www.raywenderlich.com/410-core-graphics-tutorial-part-2-gradients-and-contexts)
  * [part 3](https://www.raywenderlich.com/409-core-graphics-tutorial-part-3-patterns-and-playgrounds)
* gradient
  * [example, SO Thread](https://stackoverflow.com/questions/20632365/draw-gradient-along-a-curved-uibezierpath)

```objective-c
    CGGradientRef gradient = CGGradientCreateWithColorComponents(/* .. */)
    CGContextDrawLinearGradient(context, gradient, /* .. */)
    CGGradientRelease(gradient);
    gradient = NULL;
```

* CGContextSaveGState() and CGContextRestoreGState()

* [Bezier Path, Shape Layer](https://www.appcoda.com/bezier-paths-introduction/)

## Audio

* WWDC, [2014, Session 501](https://developer.apple.com/videos/play/wwdc2014/501/)
* WWDC, [2014, Session 502](https://developer.apple.com/videos/play/wwdc2014/502/)
* [Categories](https://developer.apple.com/documentation/avfoundation/avaudiosessioncategory?language=objc)
* [Modes](https://developer.apple.com/documentation/avfoundation/avaudiosession/audio_session_modes?language=objc)
* [Categories and Modes](https://developer.apple.com/library/archive/documentation/Audio/Conceptual/AudioSessionProgrammingGuide/AudioSessionCategoriesandModes/AudioSessionCategoriesandModes.html#//apple_ref/doc/uid/TP40007875-CH10-SW1)
* Tutorial, [AVAudioEngine](https://www.raywenderlich.com/5154-avaudioengine-tutorial-for-ios-getting-started)
* Tutorial, [Speech Recognition](https://www.raywenderlich.com/573-speech-recognition-tutorial-for-ios)
* Tutorial, [AVAudioEngine](https://cms.35g.tw/coding/avaudioengine完成即時錄音與播放功能/)
* Sample code, [Speech Recognition](https://developer.apple.com/library/archive/samplecode/SpeakToMe/Introduction/Intro.html#//apple_ref/doc/uid/TP40017110)
* SO, [format](https://stackoverflow.com/questions/33484140/how-can-i-specify-the-format-of-avaudioengine-mic-input)
* SO, [AVAudioFIle](https://stackoverflow.com/questions/52111483/writing-avaudiopcmbuffer-into-an-avaudiofile-compressed)

## WWDC Sessions

## Objective-C

## Swift
