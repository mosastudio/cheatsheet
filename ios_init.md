* ObjC

```objective-c
// init
- (id)init {
    self = [super init];
    if (self) {
        // ....
    }
    return self;
}

// singleton
+ (instancetype)sharedInstance {
    static id sharedInstance = nil;

    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        sharedInstance = [[[self class] alloc] init];
    });

    return sharedInstance;
}
```

* Swift

```Swift
// singleton
class TheClass {
  private init() {}
  static let shared = TheClass()
}
```
