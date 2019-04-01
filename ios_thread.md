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
